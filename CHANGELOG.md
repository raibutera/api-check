# 4.0.0

- Fixing the way the `enums` shortType looks.
- Adding child checker to `func` called `withProperties` which is basically just a `shape` on a function.
- Making an adjustment to how `location` works in `shape`. This makes it more readable.
- Adding the ability to specify a `help` property string/function(val) on custom checkers. This (or the result of the invoked function) will be appended to the error message.
- Adding more strict type checking for custom checkers.
- Adding the ability to specify whether you want `shape` to check if it's an object first (pass `true` as the second parameter, and it will not check whether it's an object first).
- Adding `apiCheck.config.verbose`.
- type checkers can now control how much data they output based on whether `apiCheck.config.verbose` is true or not. If they specify their `type` as a function, that will be invoked and what is returned is used for the type for display. ([#5](/../../issues/5))
- `shape` taking advantage of the new `.type` function api to show where exactly in the object the error occurred and whether it was a result of a missing field that was required or a field that failed type validation.

# 3.0.4

- Fixing oneOfType's `type`

# 3.0.3

- Bug fix. The argTypes should be an object, not stringified ([#3](/../../issues/3))

# 3.0.2

- Missed a console.log :-/ Should probably put in a checker for that...

# 3.0.1

- Quick breaking change, hopefully nobody will be impacted because it was literally minutes. Now returning an object instead of just a string message. This make things much more flexible.

# 3.0.0

- Seriously improved how the messages are formatted. There's a lot more there, but it's awesome.

# 2.0.1

- Returning the message from apiCheck.warn/throw. Though, if an error is actually thrown, then any responding code to the returned message will not run...

# 2.0.0

- Major internal api changes. All checkers now return an error like React's `propTypes` and the messaging has been improved.

# 1.0.1

- Updating readme

# 1.0.0

- Initial release. Enjoy :-)