# Music Tutorial
music_tutorial aims to (TBC)


## Prerequisites:

### Linux:
Installation of musescore (for scoring) and timidity (for MIDI playback).  For most distributions using apt, the following command will install these:

`sudo apt-get install timidity musescore`

### macOS:
Installation of musescore (for scoring) and VLC (for MIDI playback).

Musescore: [https://musescore.org/en/download]

VLC: [https://www.videolan.org/vlc/]

### Windows:
Installation of musescore (for scoring) - Windows Media Player is used for MIDI playback and is installed by default on Windows.

Musescore: [https://musescore.org/en/download]

## Installation:

Clone the repository:

`git clone [https://github.com/geokala/music_tutorial.git]`

Use pip to install the requirements included in the requirements file (currently music21)

`pip install -r requirements.txt`

## Usage:

`m210run <filename> <mode>`

where

`filename` - the music_tutorial file to run (such as 1/scale1.py)

`mode` is one of:

* `midi` to hear a MIDI version of the file
* `score` to see the score
* `text` will show the python objects that the file generates

`m210run 1/scale1.py midi` 

### MIDI (midi)
When using the MIDI mode, music_tutorial will generate a MIDI file in a temporary directory, and then launch the appropriate system MIDI player to allow the user to hear it, currently:

* Timidity on linux
* Windows Media Player on Windows
* VLC on macOS

Timidity or VLC need to be installed prior to using them (see prerequisites section).

### Score View (score)
When using score mode, music_tutorial will generate a musicXML file in a temporary directory, and then launch musescore to allow the user to view, edit and play it.

Musescore needs to be installed prior to using it (see prerequisites section).

### Python Object View (text)
When using the object view, music_tutorial will output the objects to stdout, allowing inspection of the music21 objects that have been generated.
