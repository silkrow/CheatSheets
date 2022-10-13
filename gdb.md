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
