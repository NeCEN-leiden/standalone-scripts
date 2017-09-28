


delayed_move.py
==

Copies a directory tree from source to target,
moves the files in that tree from soure to target 
once it has not changed size or modification time for a while (~2 minutes).

This was written to keep the K2 readout PC's fast RAID from filling up with the frames.

If you use it for other purposes, consider the behaviour interval with which it checks mtime/size,
this shold probably be higher for some tomography softare (because they tend to preallocate,
and might spend a few minutes between acquires)




makestacks-k2epu
==

Quick and dirty script that groups frames with the same basic (EPU-based) name, and runs newstack on it.

One-time, so run this as part of your processing of a complete dataset, and not while creating/transferring data.
It e.g. doesn't check whether the result already exists, doesn't check whether it's a complete set.

There's a fancier variant of this code in the live processing app, which may well replace this script, once I get to it.


