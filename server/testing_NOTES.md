cannot run the make clean command

````bash
server git:(fcserver_only) ✗ make clean
fatal: No names found, cannot describe anything.
rm -f src/*.d src/*.o src/httpdocs.cpp libwebsockets/lib/*.d libwebsockets/lib/*.o fcserver
````

but this is the results of closing and reopening it!! WORKING!!

the error happens if you unplug it and plug back in again when the server is running - closing and running the sever again solves it!!

*not tested with a dmx fixture but i trust it as i can see the onboard flashing showing it's working*

````bash
➜  server git:(fcserver_only) ✗ ./fcserver /Users/richmaskey/badness/fadecandy/server/test/config.json
[1723533595:6526] NOTICE: Server listening on *:7890
USB device Enttec DMX USB Pro (Serial# EN190102) attached.
^C
➜  server git:(fcserver_only) ✗ ./fcserver /Users/richmaskey/badness/fadecandy/server/test/config.json
[1723533603:2281] NOTICE: Server listening on *:7890
USB device Enttec DMX USB Pro (Serial# EN190102) attached.
[1723533625:7421] NOTICE: New Open Pixel Control connection
[1723533638:0153] NOTICE: New Open Pixel Control connection
Error submitting USB transfer: Other error
USB device Enttec DMX USB Pro (Serial# EN190102) removed.
Error opening Enttec DMX USB Pro: Resource busy
^C
➜  server git:(fcserver_only) ✗ ./fcserver /Users/richmaskey/badness/fadecandy/server/test/config.json
[1723533647:0361] NOTICE: Server listening on *:7890
USB device Enttec DMX USB Pro (Serial# EN190102) attached.
[1723533647:0873] NOTICE: New Open Pixel Control connection
^C
````
