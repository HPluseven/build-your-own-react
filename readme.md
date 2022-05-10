# Build your own React

- Easy react. Includes:

  1. The createElement Function

  2. The render Function

  3. Concurrent Mode

  4. Fibers

  5. Render and Commit Phases

  6. Reconciliation

  7. Function Components

  8. Hooks

- We didn’t include a lot of React features and optimizations. For example, these are a few things that React does differently:

  1. In Didact, we are walking the whole tree during the render phase. React instead follows some hints and heuristics to skip entire sub-trees where nothing changed.
  2. We are also walking the whole tree in the commit phase. React keeps a linked list with just the fibers that have effects and only visit those fibers.
  3. Every time we build a new work in progress tree, we create new objects for each fiber. React recycles the fibers from the previous trees.
  4. When Didact receives a new update during the render phase, it throws away the work in progress tree and starts again from the root. React tags each update with an expiration timestamp and uses it to decide which update has a higher priority.
  5. And many more…



[1] [Build your own React](https://pomb.us/build-your-own-react/)



