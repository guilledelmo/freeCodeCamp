---
title: Creating GUI's in Python 3
---

## Popular ways for developing GUI's in Python 3

Python provides various interfaces for creating Graphical User Interfaces (GUIs). Several popular tools are listed below:

**1. Tkinter**

It is the standard builds of Python include an object-oriented interface to the Tcl/Tk widget set, called tkinter. This is probably the easiest to install and use (since it comes included with most binary distributions of Python).

**2. wxPython**

It is an open source, portable GUI class library written in C++ that provides a native look and feel on a number of platforms, with Windows, Mac OS X, GTK, X11, all listed as current stable targets. Language bindings are available for a number of languages including Python, Perl, Ruby, etc.
 
**3. Qt**

It has bindings available for the Qt toolkit (using either PyQt or PySide) and for KDE (PyKDE4). PyQt is currently more mature than PySide, but you must buy a PyQt license from Riverbank Computing if you want to write proprietary applications. PySide is free for all applications.

**4. Kivy**

It is a cross-platform GUI library supporting both desktop operating systems (Windows, macOS, Linux) and mobile devices (Android, iOS). It is written in Python and Cython, and can use a range of windowing backends.

Kivy is free and open source software distributed under the MIT license.

**5. Gtk+**

The GObject introspection bindings for Python allow you to write GTK+ 3 applications.
The older PyGtk bindings for the Gtk+ 2 toolkit have been implemented by James Henstridge.

## Resources

 * [Tkinter](https://docs.python.org/3/library/tk.html)
 * [wxWidgets](https://www.wxwidgets.org)
 * [Qt]( https://www.qt.io/qt-for-python)
 * [Gtk+](http://www.pygtk.org)


### A simple GUI with Tkinter
Let's look at an example of a GUI using Tkinter. Since tkinter is already included in the Python Standard Library, you do not need to install anything to get started.
The first thing we will do is create an empty window with a title:
```py
import tkinter as tk

win = tk.Tk()
win.title("Simple window with Tkinter")

win.mainloop()
```
In the first line, we imported tkinter as tk to make it easier for us to use later in the code and be able to able to refer to it as `tk`.
After that, we created a window. In Tkinter you must create a window and put it in a variable. This is useful for applications that change their main content frequently or for pop-ups. You create a window with the method `Tk()`.
The next line defines the title of the GUI window and in the last line the `mainloop()` method is called, which allows the Tkinter window to render and show in the user's screen.

### Adding labels
In order to add some text to our window, we must use labels.
