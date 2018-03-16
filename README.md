# CS350 OS/161 Script
Script that makes working with CS350 and OS/161 easier.

## Note
1. This script is designed to work on UWaterloo linux servers. You may be able to change the directories at the top of the script to get things working locally, but it won't do those corrections by itself.
2. This script uses tmux for things like debugging / looping + debugging. Get familiar with tmux [here](https://hackernoon.com/a-gentle-introduction-to-tmux-8d784c404340)

## Smarts
1. Hides gross output from building kernel, leaving only errors that are causing a compile fail.
2. All loops are automatically logged!
3. Split your terminal into multiple panes and loop different tests on each one.
4. Debug kernel without needing different terminal windows or connecting to a specific server.
5. If you have a 1/200 bug that causes a panic, you can use loop + debug. When the panic happens, the loop pauses and you can use gdb.

## Command List
```
help                    Show this page
set ano <num>           Set Assignment Number to <num>
set do                  Set commands that will run when using "350 do"
set loop                Set commands that will run when using "350 loop"
ano                     Show Assignment Number
loop <count>            Loop <count> times
loop -d <count>         Loop <count> times. Attach to gdb on every iteration and break on panic
run                     Run last compiled kernel
make                    Compile kernel
find <phrase>           Search all code for <phrase>
open <pattern>          Vim into first filename that matches <pattern>
do                      Similar to run. Will automatically execute commands given via "350 set do"
make run                Make + Run. If make fails, nothing happens.
make do                 Make + Do. If make fails, nothing happens.
debug                   Runs kernel and attaches debugger automatically (uses tmux)
submit <target>         Submit Assignment to <target>. Similar to "cs350_submit <target>"
log                     Vim into last log created
log -o                  Output last log created (useful for piping into grep)
```
