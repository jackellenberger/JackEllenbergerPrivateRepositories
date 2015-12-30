# JackEllenbergerPrivateRepositories
A description of some of the private repositories that are not available to the public, but may be useful code samples to those that ask

This repository is a marquee 
## Projects

#### CS237 Computer Graphics : OpenGL Graphics Final Project
With Partner Jaime Arana Rochel
-----
An amalgamation of interesting graphics ideas thrown together with an extreme lack of polish. A very fun and stressful project, and the probable focus of future developement when I have some time. The readme is as follows:
```
README for project 6

jellenberger & aranarochel

Controls
	- D	- toggle diffuse lighting & texturing
	- S - toggle skybox
	- W - toggle between wireframe and flat color mode
	- R - toggle Reppy mode
	- V - toggle Vegitation visibility
	- T - toggle Time based lighting / sun rotation
	- G - toggle GUI visibility
	- X - toggle Horizon mode
		- , - push horizon down
		- . - push horizon up
		- / - toggle between cylindrical world and spherical world
	- F - toggle Fog mode
	- Left mouse click and drag - Camera look controls
	- Right Click - Teleportation
	- Shift + Right Click - plant vegitation
	- Arrow Keys - camera movement
		- + Shift - move at 10x speed
		- + Alt - move at 100x speed
	- H,J,K,L - vim camera look controls

Project Components
	- Skyboxes (Jaime) can load in either normal mode or in reppy mode by pressing the S key, and S followed by R respectively. Skyboxes are automatically added in vegitation mode for visual interest.
	- Vegitation (Jaime) can load arbitrary textures and load them anywhere in the terrain. Our current repository has three kinds of tree and a grass image. 
	- Time based lighting (Jack) - rotates the direction of the sun based on the time, as well as changes the sun and ambient color depending on time of day (orangey red at sun up and sun down, blueish at night). Also, the night is half as long as the day because the night is kind of visually boring.
	- GUI (Jack) a simple texture is rendered to the screen quad, then we interpret where the mouse is clicking and choose the texture based on the quadrant. The current GUI allows you to select the season of the trees that are being rendered, as well as the time of day. There may be a secret button on the UI as well...
	- Horizon mode (Jack) - Instead of seeing the terrain all the way to the far plane, Horizon mode curves the terrain depending on the distance from the viewer so hills roll in over the horizon in the way that some Final Fantasy games do, as well as Animal Crossing. By increasing the horizon angle, the terrain can curve up above the view plane, giving a Halo like effect. / will toggle between cylindrical (everything comes at you at an even rate) and spherical (the edges of the screen curve the terrain as well) modes.
	- Left Click camera controls (Jack) - simple click and drag operation. Not smooth or damped or anything, just nice controls.
	- Frustum Culling (Jaime) - as specified in the project 5 description, we finally got this working.
	- Right Click to teleport (Jack) - right clicking somewhere on the map will blast the camera to that position smoothly, first turning the camera in that direction, then going to the point that was clicked. It does this by reversing the projection * modelViewMat * position operation, taking the x and y of the mouse, then multiplying through that operation in reverse order with inverse matrices. Because the terrain height is not readily available, we find the z point to teleport to by doing a ray plane intersection with the plane that is at the average height of the terrain, then translates that point back up the -direction of the ray from camera to point clicked by a length dependent on the angle of that ray from the plane. This gives us more accurate locations to teleport to without going under the map. 
	We also integrated a shader we found online to give a  "warp speed" effect. We made alterations to it to ensure that we can see where we're teleporting to, as well as changing the color depending on the state of the teleport. 
	- Shift Right Click to plant foliage (Jaime)- this works the same way as right click to teleport, the difference being that we place a new foliage texture at that location. Note that Vegitation mode (V) must be on to see them.

Usage
	- currently, vegitation doesn't work with horizon mode, because horizon effects are all calculated in the shader. 
	- D, V, Shift+Right click enables textures, skybox, vegitation, and places a tree
		- clicking G will bring up the gui and allow you to choose the vegitation type
	- D, S, X, / enables textures, Skyboxes, horizon mode, then switches the horizon to a sphere.
```
Also available are 5 other Graphics projects, from my first openGL triangle to a deferred rendering pipeline:
* 
#### CS230 Operating Systems : PintOS kernel project
-----
#### CS233 Networks and Distributed Systems : chiTCP
-----
More information conveniently available [here](http://chi.cs.uchicago.edu/chitcp/), with program outlines [available](https://github.com/uchicago-cs/chitcp) thanks to Professor Sotomayor
#### Uchicago App Challenge : oGrocer.apk
-----
