# Data Engineering Interview

The expectation is a level of polish commensurate with roughly 3 hours of effort.

## Contextual Information

Purely for convenience, the problem statement will reference AWS services, but you may feel free to substitute them for any appreciably similar piece of technology - they are merely illustrative of the general requirements.

We're interested in building a batch processing system that will need to ingest data on a daily basis from a variety of data sources (an OLTP database, log data in S3, and a variety of third party APIs), transform this data in a variety of ways (both transforming single sources and potentially joining sources together), and finally load it into a variety of targets (Redshift, DynamoDB, and third party APIs).  We might call a group of these jobs a "workflow".

## Coding Exercise

Given such a batch processing system, please implement a library in any language of your choice that developers will use to *define the workflows*.  Please then use this library to demonstrate the definition of an example toy workflow.  To be very clear about scope: We are not expecting the implementation of any specific business logic, nor are we expecting you to implement an execution engine to actually run these tasks.

Additionally, there are a wide range of tradeoffs available in a batch processing system, and a wide range of features that can be implemented in such a DSL.  *Please feel free to make any tradeoffs you feel would be reasonable, and to implement features that you think would be interesting or relevant* - we only ask that you document these decisions in a README.  To seed you with some ideas for features, I've made a small list below (not a checklist, purely meant to be illustrative):

- What is the mechanism for extending a job and defining business logic?
- Are jobs parameterizable? At runtime?
- What is the desired execution model of a workflow, and what structure does this impose on the workflow definition?
- Can tasks be executed recursively or iteratively?  Conditional branching?
- Does your choice of workflow semantics affect the testability of eventual business logic implementation?

## Output

The expected output is a link to a VCS remote from which we can view the:

- code implementing the DSL
- README explaining the decisions made.
