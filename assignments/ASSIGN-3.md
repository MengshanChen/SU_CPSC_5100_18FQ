# Assignment #3

This assignment is due in my inbox by the end of class (20:05) on 03 December. You may use any materials that make sense
to you, but I ask that you provide links to references you use from the web. The following is the captured requirements
for a sales tax calculation system. You are to provide any analysis models that makes sense such that ambiguities
in this description can be addressed by the team.

You should consider class diagrams, sequence diagrams, state transition diagrams, decision trees / decision
matrices, API specifications, activity diagrams, and pseudocode as potential models.

**This assignment is worth 15 points.**

## Overview

In the computation of sales tax several jurisdictions provide input into how that tax is calculated, how
the tax revenues are distributed, and how those sales and associates sales taxes are reported. The
most local tax authority is responsible for setting the local taxes, typically based on the customer
classification, a number of addresses (including the shipped-from, shipped-to, order-received, order-billed,
and manufactured-at addresses), the product or service sold, and other special tax holidays and special
tax jurisdictions (for example, a local transportation improvement region). The statute authority
is responsible for defining and enforcing (as well as granting special overrides) tax law. The
administrative authority has responsibility for collecting sales tax revenues, receiving tax return
forms, and disbursing the tax revenues to the various associated receiving jurisdictions (the local tax
authority).

Periodically, a statute authority will grant tax collection rights to a given tax authority. As of that
time (or an effective time defined by the authority) the system should begin calculating and recording
the relevant tax revenues based on sales invoices received. At any point a customer may request that the
system recalculate the relevant tax responsibilities as of one of the point-of-sale time, the reporting
time, or the current time.

A simple algorithm for computing sales tax is as follows:

1. Determine the important sales locations present in the sales invoice
2. Compute the set(s) of involved tax authorities
3. Determine which product(s) or service(s) are being purchased, and in what quantity
4. Compute any applicable customer discount
5. Compute any relevant sales tax on a per-item basis based on combination of 
   { customer, product / service, and address }
6. Compute any relevant sales tax on a per-invoice basis based on { customer, 
   tax holidays, shipping and other discounts }
7. Return the itemized invoice with line item-level taxes and with invoice-level taxes

If, at any time, the system is unable to determine the customer class, it should assume a customer responsible
for remitting sales tax. If the system is unable to determine the product or service it should return an error
to the calling system. Finally, if the system is unable to determine the relevant tax authorities from the
addresses (where applicable), it should mark those addresses and invalid and return the invoice to the caller.

Once per month the system should collect all sales tax due calculations for each customer, itemized by purchaser
class, product or service category, and tax authority, and provide a sales tax return document along with
tax funds due to each administrative authority due sales tax revenues.
