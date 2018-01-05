
# MOS VR BUILD DOCUMENTATION

## IMPORTANT PROJECT SETTINGS

The Unity project must run on Unity 5.5.3. ANY OTHER VERSIONS WILL POTENTIALLY BREAK THE PROJECT.

## SCENE STRUCTURE

The project contains 3 scenes under the SCENES folder, they need to be added to Build Settings in sequence for the project to work correctly.
No need to change anything here unless the project is being modified, it is already setup.

## BUILD SETTINGS 

To build a project, each build needs to contain the right computer information and player ID.
The projects settings are setup directly using an Editor Script for AvatarController.

### TO BUILD 

Select Game manager in the Start scene and find AvatarController object. Using the dropdown, select the player
you would like to build. 

Build the project to an external folder with the naming scheme as follows

#### SETITOFF_player{playernum}.exe 
for example SETITOFF_player3.exe

Upload to build to the right VR machine inside the Desktop/FinalBuild folder

Restart the computer and it will start automatically in 30 seconds

### Scenes

1. INTRO - All application logic is created here
2. ELEVATOR - Elevator scene + opti track initialization
3. VOID - The full experience.

### Important Classes

1. SceneManager: 
Scene operations for scenes in section above
2. AvatarController: 
All avatar related operations including heights, ik, player settings
3. SocketIOManager: 
socket connection layer to the server
4. Audio manager: 
Audio related operations
5. OptitrackStreamingClient: Optitrack transform data processing


## 3D printed Objects

There are 2x 3d printable objects used in the piece. The gloves and the trackable object. They are designed to hold Optitrack LED's in the LED slots.
3D models are included in the repository.

### Gloves 
The LED's distributed randomly in the LED holes in the 3d object. The glove itself clamps without requires adhesive.

### Trackble object

1. The are the parts used to mount the piece together are included in an image in the github directory.
2. The LED's distributed randomly in the LED holes in the 3d object. 

### Optitrack setup

After LED's are attached, and the objects are powered. Please follow optitrack rigid body instructions to register the object with Optitrack software.


