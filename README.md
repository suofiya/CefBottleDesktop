##CefBottleDesktop

Every since I heard that Steam and Github for Windows were using Embedded Chromium, I thought I want to try my hand at using it for a GUI. I am tired of learning the GUI language of wxWidgets or GTK just to get things done. And that knowlege will only be used there, when I rarely create desktop apps. This was put together in less than a few hours after I thought of it, so it is only a beginning.

Basically the idea is to create an app in Python using bottle.py and use cefpython as the frame for the gui. A sort of open source Adobe Air type desktop platform. Now the gui itself could be bottle serving both json and template and using javascript to load the data or using Python for everything. Still considering which direction to go.

The strangest part of the app is how the bottle server gets shut down. It serves it's own PID so the browser part can grab it to shut it down before the browser shuts down.

And cefpython is supposed to have a major update next week, so kind of waiting on that to see what I can do then.

This runs on windows only currently, but if you are handy compiling C (I try to stay away from it myself), you can compile the cefpython project on your OS and the rest should work. 

So it uses:

* [cefpython](http://code.google.com/p/cefpython/)
* [bottle.py](https://github.com/defnull/bottle)

##Instructions

After cloning this repository: 

    git clone https://github.com/eristoddle/CefBottleDesktop.git

Update the submodules: 

    cd CefBottleDesktop
    git submodule init
    git submodule update

Everything should be ready to run. launch.py uses python.exe and launch.pyw uses pythonw.exe if you don't want a console hanging around. Now to build an app, just add more to the bottleserver.py file or even get crazy and add templates and the like. Pretty simple to figure out.


