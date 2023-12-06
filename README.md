# analyze.py

A simple Python script to analyze the performance of a Blended-Wing Body aircraft.

For use during the MIT 16.100 Final Project.

# Usage

```
python3 analyze.py [AVL-file] [cylinders-file] [conditions-file]
```

## AVL File

A *metric* AVL file is required.

## Cylinders File

A *metric* cylinders file is required.

A sixth column must be included to specify the classification of each tank.
A `0` in this column indicates a passenger cabin, and a `1` indicates a fuel tank.
No other values are permitted.

## Conditions File

See `conditions.txt` for an example of this file format.

`conditions.txt` contains five values:
- Propulsion system type (`int`).  This is `1` for a turbine engine and `2` for a fuel cell.
- Cruise mach number (`float`).
- Local speed of sound (`float`, meters per second).
- Free-stream density (`float`, kilograms per cubic meter).
- Kinematic viscosity (`float`, square meters per second).

Note that all lines beginning with a hash (`#`) in a flight conditions file will be ignored. 

# Setup Instructions

## Windows

Before using `analyze.py`, you'll need to set it up.

1. Open `analyze.py` in your favorite code editor.
2. Change the variables `AVL` and `XFOIL` to the location of AVL and XFOIL.  If both of these are in the current
directory, change these to `./avl.exe` and `./xfoil.exe` respectively.

## Linux

`analyze.py` is already set up for you.  Copy AVL and XFOIL into this directory and you're ready to go.

## macOS

Unfortunately, I don't know how to use macOS well enough to provide instructions.

# Changelog

**v0.1.0**: Initial commit.

# Thanks

Thanks to MIT Professor Qiqi Wang for:
- `design.py`
- `graph.py`
- `vehicle.py`
- `*.dat` airfoils

Thanks to MIT Professor Mark Drela for:
- AVL (not included)
- XFOIL (not included)