1. Why do we present _Customer Bills of Rights and Responsibilities_, and to whom would they be presented?

    > We present these two documents (which are only _hints_) to all stakeholders involved in the requirements process. In particular
    we present these to the _customers_ and the _developers_ so that we can create an environment in which both parties trust each
    other. These are, in some sense, reverse images of each other. The _bill of rights_ is what the customer can expect from other
    stakeholders, where the _bill of responsibilities_ is what the other stakeholders expect from the customer. Setting these as
    the ground rules can greatly improve relationships among the various stakeholders.

2. What does Brooks mean when he describes _accidental_ difficulties and in what way(s) does this related to _essential_ difficulties?

    > Accidental difficulties are those software development process issues which can be improved through tooling and other
    external interactions. Essential difficulties are those that are inherent to the process as a whole. An essential difficulty must
    be actively addressed and usually requires _soft_ work to correct. One can think of accidental processes as those that self-correct
    as the tooling (hardware, software, languages, etc.) improves over time.

3. Describe the four phases of requirements development. What are they, how do they relate, and who are the primary actors involved in each?
    
    > * Elicitation - the process of discovering the stakeholder's needs, wants, pains, and desires in order to provide a solution 
    that "solves" those problems
    > * Analysis - the process of understanding, classifying, and clarifying the tasks and solutions from elicitation
    > * Specification - formalizing, by writing down, the requirements (think user stories or use cases) such that developers
    can begin to design and implement solutions
    > * Validation - confirmation, via prototypes, conversations, and other interactions that you have the _right_ requirements

    > In general this is a left-to-right process from elicitation -> analysis -> specification -> analysis. However, it's also the
    framework in which a highly iterative and "looping" process can be constructed. That is, it's always possible, and expected,
    to return to any previous step in order to fill in gaps, clarify assumptions, and get customer feedback.
    
    > Actors in the various stages:
    > * Elicitation: customers, business analyst, users, developers, testers, etc.
    > * Analysis: primarily a business analyst process, but will involve development (developers and testers)
    > * Specification: primarily a business analyst process, but will heavily involve development and testers (can it be built
    and do we have the correct acceptance criteria)
    > * Validation: primarily a development process (developers create designs, testers create acceptance tests, both look for problems)

4. Describe the overall requirements elicitation process. There are four phases, what are they, and how do you know you’re done?

    > This starts with the "Three P's" and adds in input classification as the fourth step.
    > * Planning - plan the project objectives (where _project_ is the elicitations process), choose techniques, identify participants,
    identify source materials, and hunt down the risks (mainly to the elicitations process)
    > * Prepare - plan the session (or other technique) scope, prepare any physical resources, learn about your stakeholders, build
    any necessary "straw man" models, prepare the (core) questions (for the stakeholders)
    > * Perform - educate the stakeholders (on what's going to happen, why we're doing this, and your approach), write everything down,
    get everyone involved (if they're in the room make sure they're heard and don't let any one stakeholder control the meeting)
    > * Classify - determine: business requirements, technical requirements, user requirements, important business rules, external rules
    and constraints, functional / non-functional requirements, any data requirements, proposed "solutions"
    
    > You can assume you're done when no _new_ data / requirements / scenarios are raised, or that any new requirements / scenarios
    don't lead anywhere (or fit the current scope). Watch for distance (in time) and scope issues. Pay attention to developers,
    when they stop asking clarifying questions they might have enough information to proceed.

5. What are some of the characteristics that define the _Product Manager_ and _Product Owner_ roles? In what ways are they similar and
    in what ways are they different (and why)?
    > The product manager and product owner are very similar roles. Both manage a backlog, both manage iterations, and both have projects.
    However, they differ in the organization level in which they operate and the timeframes over which their respective teams
    "release" product. The product owner operates at the lowest level of the (three layer) Leffingwell model (the team) and runs smaller
    development teams. Those teams have shorter iterations and their work is fed "up" into the second (the program) level. It's at
    this level that the product manager operates by combining the smaller teams work into larger "potentially shippable iterations".
    These iterations are likely longer (our text uses 4 or 5 two-week iterations plus a stabilization iteration at the team level
    which combine to produce a quarter-long release).

6. (bonus) How is a _Vision Statement_ similar to a _User Story_ and in what ways are they very different?
    > We can look at two aspects here.
    
    > The first is that both describe, in essence, a story targeted to a various stakeholder
        group. The _vision statement_ is the long-term product definition. It's meant to survive several releases of a
        product and should be considered the (pick your favorite resilient thing here) stable point at which all
        decisions about scope are made. The _user story_ describes a specific task that a user needs / wants to perform and
        is used to guide the developers in their work.

    > The second aspect is that they are both structurally similar. A user story takes the following form:
    
    > "As a [role], I want to [do something] so that [some business objective] and I'll know this is done when [acceptance criteria]"
    
    > The vision statement can take the form:
    
    > "For [our customer] who [statement of need] the [name of product] is [product category] that [does ...] unlike [our competition] our product [differentiating factors]"
    
    > They are very different in terms of timeframe and work scope. The vision should last several releases. The user story is
        useful for one iteration. One guides the product as a whole, one guides a single aspect of the product.
