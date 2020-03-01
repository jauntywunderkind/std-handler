# std-handler

> Conventions for delcaring handler behavior up front

# Handler Symbols

## `Scheduling`

Expects value of:

`synch`
`async` (or alias, `microtask`) - scheduled as a microtask after the invoker, like a promise. 
`task` - scheduled as per a normal tick

## `WaitFor`

`true` - delay completion until after this handler runs

## `WaitUntil`

`true` - this function will potentially make use of `waitUntil` to attach sub-processes to handler executions.

This function will make use of waitUntil to declare any continuation of the work of the promise that it wishes to complete.

## `Phase`

`capture` - handler expects to work in capture phase
`bubble` - handler expects to work in bubble phase

## {Pre,Post,Final} {Resolve,Reject,Settle}

Lifecycle bound sub-listeners that run at points in execution life-cycle.
