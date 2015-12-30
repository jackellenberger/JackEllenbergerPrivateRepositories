# JackEllenbergerPrivateRepositories
A description of some of the private repositories that are not available to the public, but may be useful code samples to those that ask

This repository is a menu for all the projects that are private on github or offline that are available to potential employers or friends as work samples and homework help respectively. I'm keeping the contents private because in many of them there are code stubs written by professors which will be reused in future years. I'm not keen on giving away answers to future years (but if you want help just ask), so I'm going to keep the code unsearchable, and if someone is interested in a project I can add them as a collaborator or just zip up a copy of the codebase. Just comment on this README or send me an email.

Cheers
Jack Ellenberger


## Projects

#### CS237 Computer Graphics : OpenGL Graphics Final Project
_With Partner [Jaime Arana Rochel](https://github.com/aranarochel)_

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
* [Basic Rendering](https://github.com/jackellenberger/JackEllenbergerPrivateRepositories/blob/master/Graphics/basic_rendering.pdf)
* [Shading, Lighting, and Texturing](https://github.com/jackellenberger/JackEllenbergerPrivateRepositories/blob/master/Graphics/shading_lighting_textures.pdf)
* [Blinn-Phong and Bump Mapping](https://github.com/jackellenberger/JackEllenbergerPrivateRepositories/blob/master/Graphics/advanced_lighting_bump_mapping.pdf)
* [Deferred rendering pipeline, spot and point lights, specular mapping](https://github.com/jackellenberger/JackEllenbergerPrivateRepositories/blob/master/Graphics/deferred_rendering.pdf)
* [Terrain Rendering with chunked LOD](https://github.com/jackellenberger/JackEllenbergerPrivateRepositories/blob/master/Graphics/terrain_rendering_lod.pdf)

#### CS230 Operating Systems : PintOS kernel project
_With Partner [Henry Riordan](https://github.com/hriordan)_

-----
A general introduction to PintOS can be found [here](https://web.stanford.edu/class/cs140/projects/pintos/pintos_1.html), and a more advanded look into how the seed code is laid out can be found [here](https://web.stanford.edu/class/cs140/projects/pintos/pintos_6.html). I unfortunately didn't think to copy the project descriptions back when I took the class, but stanford runs the same project has graciously agreed to save them for me. The projects covered:
* [Threads, including a totally fair priority queue](https://web.stanford.edu/class/cs140/projects/pintos/pintos_2.html)
* [basic virtual memory allowing for sandboxed user programs, user vs kernel memory](https://web.stanford.edu/class/cs140/projects/pintos/pintos_3.html)
* [advanced virtual memory with paging, intelligent disk swapping, memory mapping](https://web.stanford.edu/class/cs140/projects/pintos/pintos_4.html)
* [Hierarchical inode based file system with caching](https://web.stanford.edu/class/cs140/projects/pintos/pintos_5.html)
#### CS233 Networks and Distributed Systems : chiTCP, chiIRC, chiRouter
-----
More information conveniently available [here](http://uchicago-cs.github.io/cmsc23300/syllabus.html), with program outlines [available](https://github.com/uchicago-cs/chitcp) thanks to [Professor Sotomayor](https://github.com/borjasotomayor). We implemented the majority of the TCP and IRC protocols to RFC spec, as well as some IP packet routing for the router project. 

#### Uchicago App Challenge : oGrocer.apk
-----
I am currently (as of 12/30/15) a semifinalist in the [uchicago App Challenge](https://appchallenge.uchicago.edu/page/2016-phase-1-winners) with an idea for an app that lets users plan their shopping trips to maximize efficiency parametricly, balancing their time and their budget depending on their needs. For example, it may be $40 cheaper to buy food at a farmers market 90 minutes away, and on a lazy saturday that might be worth it. On a busy work day, however, it might be worth $40 just to have something to cook at home and not have to worry about grocery shopping further away than next door. oGrocer aims to give the consumer complete information about food prices and availability in order to allow for economic efficiency in busy families.
