# Project 1

## My Approach:
- Keep receiving FIND messages and sending COUNT  mesages until BYE message is received from to server.
- To get complete FIND messages, keep receiving from the server and append the received chuncks until a new line character is seen.

## Challenges I Faced:
- When I run the script, sometimes I was getting the flags correctly, sometimes I wasn't and script terminated me showing a FIND message. It turns out that I was checking for 'BYE' substring anywhere on the received line, not just the correct place for the fields (right after ex_string). Since server sends random strings, sometimes FIND message contained 'BYE', resulting my script to end early. It took me a while to figure out what was going on.

## How I Tested My Code:
I used print() statements to check:
- The complete FIND messages that client receives from the server
- The complete COUNT messages the client builds as a reponse
