# Yak Stacker

An app for tracking your Yak Stack during programming sessions.

## Usage

Click the `Start` button to begin a new session. This will automatically stop any existing active session with an indeterminate end time.

When you're starting a new task, provide a description in `What Are You Doing?` and (click `Start Task`/press `Enter`).

If you get sidetracked with another task directly related to what you're working on, click the task's (`Stack` button/some sort of shaving icon) and provide a description in `What Are You Doing Now?` and optionally provide some notes in `What Do You Need To Remember Later?`

Click the `I'm Done With This` button on any task stack once you're done with it. All nested tasks will also be considered done.

If you're conciously stopping working on a task and have some context you need to remember later, click its `Stop` button and optionally provide some notes in `What Do You Need To Remember Later?`

If you're conciously stopping working on a session click its `Stop` button. This is primarly a psychological device intended to help you go to bed because you can't continue the same session without manually hacking Yak Stacker's persisted state.

## Design Questions

- Should tasks you're not done with automatically move to a new session when it's started? This isn't a TODO list, it's a aide-mémoire, so an `I'm Still Working On This` button on open tasks (or some other UI for moving tasks over, e.g. autocomplete open tasks in `What Are You Doing?`) from previous sessions might be more appropriate.

## Tech

- React, Inferno or Preact; easy to switch with nwb
- Just use `localStorage` initially
- PWA, as it needs to work offline ([`stack.push(Add Progressive Web App support to nwb)`](https://github.com/insin/nwb/issues/203))
