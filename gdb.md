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
#### > break <*where*> if <*condition*>
	Break at the given location if the condition is met.
	Conditions may be almost any C expression that evaluate to true or false.
#### > info breakpoints
	Show information of all breakpoints.
#### > maint info breakpoints
	Show the breakpoints you set, and those GDB are using for internal purposes.
## Watchpoints
#### > watch <*where*>
	Set a new watchpoint.
#### > delete/enable/disable <*watchpoint#*>
	Delete/enable/disable a watchpoint.
#### > watch <*where*> if <*condition*>
	Watch at the given location if the condition is met.
	Conditions may be almost any C expression that evaluate to true or false.
## Stack
#### > backtrace
	Show call stack
#### > backtrace [*n*]
	Show call stack, of n innermost frames if n > 0, outermost if n < 0.
#### > backtrace full
	Show call stack, also print the local variables in each frame.
#### > frame <*frame#*>
	Select the stack frame to operate on.
#### > info args
	Print arguments of the selected frame.
#### > info locals
	Print local variables of the selected frame.
#### > info reg
	Print register values of the selected frame.
## Stepping
#### > step
	Go to the next instruction(source line), diving into function.
#### > next
	Go to next instruction (source line) but donʻt dive into functions.
#### > finish
	Continue until the current function returns.
#### > continue
	Continue normal execution.
## Variables & Memory
#### > print/*format* <*what*>
	Print content of variable/memory location/register.
#### > display/*format* <*what*>
	Like "print", but print the information after each stepping instruction.
#### > undisplay <*display#*>
	Remove the "display" with the given number.
#### > enable display <display#>
	Enable "display" with the given number.
#### > disable display <display#>
	Disable the „display“ with the given number.
#### > x/*nfu* <*address*>
	Print memory.
	n: how many units to print(default 1).
	f: format character(like "print").
	u: unit, one of b, h, w, g
		b: byte
		h: half-word(two bytes)
		w: word(four bytes)
		g: giant word(8 bytes)
---
## *format*
#### a
	Pointer.
#### c
	Read as integer, print as character.
#### d
	Integer, signed decimal.
#### f
	Floating point number.
#### o
	Integer, print as octal.
#### s
	Try to treat as C string.
#### t
	Integer, print as binary.
#### u
	Integer, print as unsigned decimal.
#### x
	Integer, print as hexadecimal.
## <*where*>
#### function_name
	Break/watch the named function.
#### line_number
	Break/watch the line number in the current source file.
#### file:line_number
	Break/watch the line number in the named source file.
## <*what*>
#### expression
	Almost any C expression, including function calls (must be prefixed with a
	cast to tell GDB the return value type).
#### file_name::variable_name
	Content of the variable defined in the named file (static variables).
#### function::variable_name
	Content of the variable defined in the named function (if on the stack).
#### {*type*} address
	Content at address, interpreted as being of the specified C type.
#### $register
	Content of named register.
