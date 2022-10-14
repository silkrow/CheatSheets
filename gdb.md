# GDB
## Execution
#### gdb <program>
	Start GDB(with optional core dump).
#### gdb --args <program> <*args...*>
	Start GDB and pass arguments.
#### > set args <*args...*>
	Set arguments to pass to program to be debugged.
#### > run 
	Run the program.
#### > kill
	Kill the running program.
## Breakpoints
#### > break <*where*>
	Set a new breakpoint.
#### > delete [breakpoint number]
	Remove a breakpoint.
#### > clear 
	Delete all breakpoints.
#### > enable [breakpoint number]
	Enable a disabled breakpoint.
#### > disable [breakpoint number]
	Disable a breakpoint. 
#### > info breakpoints
	Show information of all breakpoints.
#### > maint info breakpoints
	Show the breakpoints you set, and those GDB are using for internal purposes.
## Watchpoints
#### > watch <*where*>
	Set a new watchpoint.
#### > delete/enable/disable <*watchpoint#*>
	Delete/enable/disable a watchpoint.
## <*where*>
#### function_name
	Break/watch the named function.
#### line_number
	Break/watch the line number in the current source file.
#### file:line_number
	Break/watch the line number in the named source file.
