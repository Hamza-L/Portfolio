# Portfolio
*Where my semi-finished kind of presentable projects reside!*

## Table of Contents
* [ArcBall](#arcball)
* [BirdFlock](#birdflock)
* [Subdivider](#subdivider)
* [SierpinskiTriangle](#sierpinskitriangle)

## [ArcBall](https://github.com/Hamza-L/ArcBall)
Here is the ArcBall UI allowing the user to move about an object in 3D space using only the mouse. This project builds on the VulkanTesting repo, where I test various Vulkan features and implement my own pseudo-engine.

<img src="https://github.com/Hamza-L/ArcBall/blob/master/Arcball.gif?raw=true" alt="ArcBall" width="1100"/>

### Features!* 

1. 3D & 2D geometry
1. Texture from files
1. UV Normal textures form files
1. Scene graph, allowing objects to become part of a parent objects, sharing on local coordinate
1. specular highlight (bling-phong lighting)
1. User input
1. Scroll to zoom! makes use of perspective zoom rather than move the camera.

### How it works!
This implementation builds upon the **Ken Shoemake**'s paper _ARCBALL: A User Interface for Specifying
Three-Dimensional Orientation Using a Mouse_. Mouse coordinates are converted
vectors form the center of a fictional unit sphere. The starting mouse position and the ending mouse position allow us to establish an axis or rotation. Matrix accumulation allows us the compute rotation at very low cost.

<p align="center">
  <img src="https://github.com/Hamza-L/ArcBall/raw/master/kenShoemaker.png" alt="ArcInterpretation"/>
</p>


_Shoemake, K. (1992). ARCBALL: a user interface for specifying three-dimensional orientation using a mouse._

### Dependencies:
- glfw (window)
- Vulkan (graphics api)
- glm (math library)
- stb_image.h (for importing images: https://github.com/nothings/stb/blob/master/stb_image.h)

*_This repo includes features from the VulkanTesting repo, my very own engine._

## [BirdFlock](https://github.com/Hamza-L/BirdFlock)
A graphics program simulating bird movements. Makes use of the Vulkan API.

<img src="https://github.com/Hamza-L/BirdFlock/blob/master/boid.gif?raw=true" alt="Boid" width="1100"/>

### Features!
1. collision avoidance
1. controllable red bird
1. resizing of the window increases/decreases the area of available flight space
1. no limits on window edges (birds fligh from a window edge to the other)
1. trail on red bird can be toggled

### How it works!
This projects builds upon the boid paper. Allowing for bird flight only necessitates 3 types of behavior; Separation, Alignment, cohesion. With these three implemented, you have yourself a pretty convincing bird flight simulator.

<p align="center">
  <img src="https://github.com/Hamza-L/BirdFlock/blob/master/boids.png?raw=true" alt="Boid"/>
</p>

_Craig W. Reynolds. 1987. Flocks, herds and schools: A distributed behavioral model. SIGGRAPH Comput. Graph. 21, 4 (July 1987), 25–34._

### Dependencies:
- glfw (window)
- Vulkan (graphics api)
- glm (math library)


## [Subdivider](https://github.com/Hamza-L/Subdivider)
Code that subdivides various geometric shapes using its vertices (for the sphere) or using its scene graph properties and recursion. Makes use of the Vulkan API

### The making of a sphere!
The algorithm starts with an icosahedron and subdivides its triangles and normalizes the newly generated points such that they line up with a unit sphere. The icosahedron has a convenient property which allows it to be easily defined with points of length 1.

![Icosahedron](https://raw.githubusercontent.com/Hamza-L/Subdivider/master/Icosahedron.gif)


### Subdivided Cube:
The algorithm starts with a cube attached to a node. the node is recursively assigned as a child of itself with transformation such that the position of the cubes remain evenly spaced appart


![Cube](https://github.com/Hamza-L/Subdivider/blob/master/cube_subdiv.png?raw=true)

### Dependencies:
- glfw (window)
- Vulkan (graphics api)
- glm (math library)


*This repo is kept simple as it serves a starting point for other vulkan projects. The features listed can be found in these repo.

## [SierpinskiTriangle](https://github.com/Hamza-L/SierpinskiTriangle)
A simple program making use of the Vulkan API which procedural generates a Sierpinski triangle, a fractal subdivision of a basic triangle.

![alt text](https://raw.githubusercontent.com/Hamza-L/SierpinskiTriangle/master/images/img1.png "Sierpinski Triangle")

