# Magic Sand
Magic Sand is a software for operating an augmented reality sandbox developed by Thom Wolf. The original repository can be found [here](https://github.com/thomwolf/Magic-Sand). This repository contains a modified version of Magic-Sand, used in the course TFE4850 at NTNU. 

## This fork's goal
The original Magic-Sand software is currently being used by Andøya Space at their visitor center. We were proposed a task from Andøya Space to further develop this software, by adapting space-themes into Magic-Sand, as well as incorporating a physical control panel that can be used by the educators at Andøya Space' visitor center. 

We intended at first to attempt to compile Magic-Sand to the Raspberry Pi, thus creating a fully stand-alone system for running the software. Unfortunately, we were unable to succeed in this. Generally, compability problems connected to OpenGL prohibited us from succeeding. The addon ofxDatGui uses OpenGL calls which are not natively supported by the Pi. 

## How this version differs from the original
We have added a TCP-server into Magic-Sand that spins up when the progam is started. This is to provide a communication layer between the control panel, which runs on a Raspberry Pi and the Magic-Sand software. Messages that are recieved by the server are analyzed, and if the message corresponds with any of the pre-set commands, code will execute. For example, sending numerical values will change the vertical offsett etc. These changes are applied in the file ofApp.cpp

We included some more maps, which makes the educators able to select between the Earth, Mars and the Moon by pressing buttons on the control panel. 

## The control panel
Developed a HAT that goes ontop of a Raspberry Pi 4B. Has 5 buttons and a potentionmeter (which also has a button). The code running on the Pi can be found [here](https://github.com/Sunhome22/TFE4850_Duck_Island_Space_Control_Panel).

### Acknowledgements
We would like to thank Andøya Space Center, especially Ørjan H. H. Vøllestad for presenting the idea and aiding us by answering our questions. We would also like to thank course leader Amund Gjersvik and the facilitators for guiding us throughout this course.


Thanks!
- Group 2, 2024
  - Bjørn Kristoffer Trydal Solheim
  - Magnus Svendsen 
  - Martin Heim
  - Mikael Mjelde
  - Sigurd Skeide

