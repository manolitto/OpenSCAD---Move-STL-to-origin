# OpenSCAD---Move-STL-to-origin
Makes a library tailored to an existing STL file. Move it to the origin in OpenSCAD.

Uses a modified version of a Python script, stldim.py, by Jamie Bainbridge. His version can be found at:
  https://www.reddit.com/r/3Dprinting/comments/7ehlfc/python_script_to_find_stl_dimensions/

I often edit STL files to customize, improve, or repair them I find that sometimes the object is placet well away from the OpenSCAD origin, and I have to guess at what translation to use to put it at the origin, then fiddle with the translation to fine tune the position. This program will place the object in one of 5 different places, each one touching the origin (where the x, y and z axes meet). You have the choice of placing it in the center or adjacent to the origin, determined by compass directions, NE, NW, SW, SE.

The python script, **stldim.py**, when run in the directory of a file you want to place, will generate a file that may be used as a library. It will contain, as well as the code to place the object, comments showing the max and min x, y, and z values (a bounding box), as well as the x, y, and z size of the object (handy for woodworkers laying out cuts for lumber or plywood).

It may be used stand-alone, or as a library.

Usage:
  Place the **stldim.py** file where you keep your Python executable scripts.
  On a command line, CD to the directory containing the STL you wish to move, and redirecting the output to the library filename (see the example).
  Run the script, giving it the name of the STL file as an argument.

Example:
  To use the example, place Hook.stl and Hook.SCAD in the same directory.
  Using a command line, CD to the directory and run the python script.
     **stldim.py Hook.stl >lib_2origin.scad**
  Load the Hook.scad file
  Previewing Hook.scad will show the object in all 5 positions. Putting an exclamation mark before one of the obj2origin(xx); lines will just display one of the results.
  
