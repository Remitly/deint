# Data Engineering Interview

There are two parts to this interview, and we're targeting a level of work product that should require somewhere around 3 - 6 hours.

## Architecture Design

For the first part of this interview, we'd like to see a proposal for a batch processing subsystem that is responsible for daily ingesting data from a variety of data sources (an OLTP database, log data, and a variety of third party APIs), having a graph of processing tasks that operate on this data, and finally loading it into a variety of targets (a Data Warehouse, pushing to APIs, and publishing to an event broker).

The main concerns we'd like to see addressed are that we have at least a few data sources in the 10 TB order of magnitude, and that an excellent developer experience is paramount - a new developer should feel comfortable creating a new job or modifying existing ones, and be as confident as possible that errors have not been introduced. (For example - how will the developer test his or her changes?)

There are a lot of other tradeoff decisions that can be made in a batch processing subsystem, so please feel free to treat the problem as a typical case, and make any tradeoffs that you think would be reasonable.

## Coding Exercise

Given the batch subsystem that's been architected, please write a library that will allow someone to express the graph of tasks in a computational workflow while maintaining all of the core properties that were desired.  It should be carefully noted what we're not expecting: a) Any specific business logic, or b) an execution engine to actually run the tasks.  It's *just* the DSL that allows someone to specify a workflow.

There's a lot of flexibility in the design which will dramatically differ depending on the requirements - we're happy to let you dictate the tradeoffs as long as we're within the bounds of what would reasonably be expected for a batch processing subsystem.

Once done, please describe how your workflow description language would be capable of expressing a workflow for your architected subsystem, and how it would meet all of the core properties that you've included.
