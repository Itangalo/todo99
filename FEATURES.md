# Desired features

* Possible to add, delete and mark tasks as done.
* Possible to show tasks in Google Calendar.
* Possible to set advanced rules for recurring tasks (such as "10 days after last completion" or "every Wednesday"). This could be done programmatically – no advanced graphical configuration planned. Possible to both "check and reschedule" and "check and disable" tasks.
* Possible to set points awarded for completing tasks.
* Possible to set (advanced) rules for how points change when deadline for a task has passed.
* Possible to show tasks in priority order (as described by points).
* Possible to set task size
* Reasonable default behaviour for task points.

## Ideas for implementation

* Implemented as a Google script.
* Base class/whatev for tasks, with reasoable default behaviour. More complex task types extend this class.
* When new tasks are created, task type (class) is chosen. Parameters are given depending on task type.
* Data is stored in a Google spreadsheet. Tasks are stored with serialized parameters.
* Spreadsheet is also used to present tasks in priority order.
* Time based trigger processes (active) tasks regularly and updates points/whatev.
