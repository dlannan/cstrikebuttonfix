Counter Strike 1.6 Button Click Fix
-----------------------------------

If you are a Win10 user and have enjoyed playing CS 1.6 in 
the past on Win10, and now you are finding:
1. Left clicks of the mouse result in weird problems like:
  - Cannot click more than once in the exact same direction (not moving mouse)
  - Clicking seems to unload your entire clip.
2. Right clicks of the mouse result in:
  - Continual adding and removing of silencer for guns
  - Weird throwing of grenades
Then this is the fix for you. The above drove me nuts.
And, after searching and searching, I could not find a solution
that worked. It turns out the 2017 Xmas update changed some windows
messaging in the kernel. Apparently a fix is coming.. yet to see it tho.

-----------------------------------
Build or Release.

Release
I have put up a 64bit release build in a zip. 
Rename the file to an exe and run it as admin. Dont worry its, clean,
and if you dont trust me, just build it yourself.

You need to run it as Admin so it catches all mouse click calls.

Build
Just build with your favourite Visual Studio edition. 
There is nothing fancy in there, and it should build 
on most versions of VS. 

-----------------------------------
Notes:
Its not perfect. It does lose clicks every now and then. 
The current "Jigger" hack to make Halflife register a click and 
not keep clicking is 1 pixel. You might need to change this if
it doesnt seem to work. 
Additionally adding sleeps in the WindowProc loop can reduce the
overhead of the app, but I found this also effects the mouse
movement for some reason. So change code at your own risk.

-----------------------------------
License - MIT

Copyright (c) 2018 David Lannan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE. 

-----------------------------------
Oh. And if you havent debugged kernel hooks before, just
be careful - you can lockup your PC easily. Which might need a
reset. Read MS documents about doing this.