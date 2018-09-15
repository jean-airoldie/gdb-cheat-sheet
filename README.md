# gdb-cheat-sheet
Various helpfull gdb commands.

## Terminal Gui
I highly recommand using [gdb-dashboard](https://github.com/cyrus-and/gdb-dashboard)
as opposed to the default `gdb -tui` mode.

## Talks on the Subject
* [Greg Law](https://www.youtube.com/watch?v=-n9Fkq1e6sg)

## Normal Commands
* backtrace ('ba') full -- Complete backtrace with local variables
* up, down, frame -- Move through frames
* watch -- Suspend the process when a certain condition is met
* set print pretty on -- Prints out prettily formatted C source code
* set logging on -- Log debugging session to show to others for support
* set print array on -- Pretty array printing
* finish -- Continue till end of function
* enable and disable -- Enable/disable breakpoints
* tbreak -- Break once, and then remove the breakpoint
* where -- Line number currently being executed
* info locals -- View all local variables
* info args -- View all function arguments
* rbreak -- Break on function matching regular expression
* print -- Print value of expression
* whatis -- Print data type of expression
* record --  Record a log of the process execution to replay it later
[(more info)](https://sourceware.org/gdb/onlinedocs/gdb/Process-Record-and-Replay.html)
## Reversed Direction (~50k times slower execution)
[(more info)](https://sourceware.org/gdb/onlinedocs/gdb/Reverse-Execution.html#Reverse-Execution)
* reverse-continue ('rc') -- Continue program being debugged but run it in reverse
* reverse-finish -- Execute backward until just before the selected stack frame is called
* reverse-next ('rn') -- Step program backward, proceeding through subroutine calls.
* reverse-nexti ('rni') -- Step backward one instruction, but proceed through called subroutines.
* reverse-step ('rs') -- Step program backward until it reaches the beginning of a previous source line
* reverse-stepi -- Step backward exactly one instruction
* set exec-direction (forward/reverse) -- Set direction of execution.
## Conversion
* p/d 0x10 -- gives decimal equivalent of 0x10
* p/t 0x10 -- binary equivalent of 0x10
* p/x 256 -- hex equivalent of 256
