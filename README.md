# What this fix does

This fixes the problem with squares instead of letters in dialog boxes like Open and Save As for LightTable (on Linux).

# How it works

For those of you who can find LightTable in the /opt/LightTable folder after installation, just CLONE the two files (readme is not needed, obviously) in this repo and copy them into the mentioned folder. This will for example work for Arch Linux, likely Manjaro and similar too.

For instances installed via Ubuntu Make (umake), the installation folder can typically be found at ~/.local/share/umake/ide/lighttable.

For those of you who do NOT have LightTable in the mentioned folders after installation (for example, distros with apt/dpkg package management), do the following: head over to  [lighttable.com](http://lighttable.com/) and download the 64Bit binary. You'll receive a tarball. Extract it. The extracted files will be in a new folder next to the tarball. Now CLONE the files in this repo and add it to the folder, next to the extracted files. If you haven't already, go to the folder and start LightTable. Make sure you use ./LightTable, not just the command "LightTable". First will start LightTable from the according folder, second will start the installed version from your system. So, in second case the problem will appear not to be solved. So, don't miss the dot-slash. Does it work? Well, then remove the non-working thing and just link to the downloaded LightTable in your /usr/bin (ln -s /path/to/LightTable /usr/bin/LightTable) to make your system own it ;)

# IMPORTANT

Do NOT download the 2 files one by one using the explicit file links. For some reason experience suggest, that this will render one of the files useless and cause an error. You have to CLONE the two files (and copy or move them).

# Notes

This solution has been presented first in January. It has been tested on both, Arch Linux, as well as Ubuntu 18.04. And it works the same and has been working since January.

NO, the solution is NOT related to electron, gitcraken or whatever else has been GUESSED over time and still is brought up in new complaints today.

Also, unsubstantiated ASSUMPTIONS expect the problem to solve itself with newer versions (for example of electron). Interesting though is, that the issue has NOT been solved in the master since reported first in Jun 2017 (at least in issue 2343). Actually, the issue hasn't even been assigned! As a matter of fact, parts of LightTable are like 3 or 4 years old. So, assuming it will work with even newer versions and libraries than already present, while theoretically possible, based on present evidence does not make any sense at all.

NO this is NOT IN THE official MASTER! And it hasn't been added since January.

Aside from that, recently there has also been a bug report for artifacts in the font. I did NOT encounter this problem on Arch Linux until this day. However, I have found it to be present during my test on Ubuntu 18.04.
