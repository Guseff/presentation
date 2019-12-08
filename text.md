Hi, Ladies and Jens.
My name is Vasily. 

1. Today I'm going to tell you about WebGL (Web Graphics Library) and Three.js.
What WebGL is?

1.1. WebGL is a JavaScript API for rendering interactive 2D and 3D graphics
within any compatible web browser without use of plugins.
WebGL is designed and maintained by the non-profit Khronos Group.

1.2. WebGL is fully integrated with other web standards.
It allows GPU-accelerated usage of image processing and effects as part
of the web page canvas.
WebGL elements can be mixed with other HTML elements and composited
with other parts of the page or page background.

1.3. WebGL programs consist of control code written in JavaScript and shader code
that is written in OpenGL ES Shading Language (ESSL),
a language similar to C or C++. Shader code is executed
on a computer's graphics processing unit (GPU).
Automatic memory management is provided implicitly by JavaScript.

2. Like OpenGL ES, WebGL does not have the fixed-function APIs.
This functionality, if so required, has to be implemented
by the end-developer by providing shader code.

2.1. First, the JavaScript code gets a 3D context from an HTML5 canvas element.
Than it registers a set of shaders.

Shaders in WebGL are expressed directly in GL Shader Language and passed to the WebGL API
as textual strings.
The WebGL implementation compiles these shader instructions to GPU code.
This code is executed for each and every vertex sent through the API.

Vertex array is transferred to GPU buffer with array of vertex indexes,
that needs for control conversion vertexes to triangles. 
Vertex shaders in GPU calculate position for each vertex.


2.2. GPU converts vertexes to triangles. 
Then it makes rasterization, and represents image as pixel fragments.
Fragment shaders calculate color for each pixel. Additionally shaders calculate textures and lights.
Than GPU transfers pixels in frames buffer.

2.3. Frames buffer is a last step. The result of this work is an image at the screen. 

3. The low-level nature of the WebGL API, allows to produce 3D graphics very quickly.
3.1. But it's not convenient to write shaders manually. So it's necessary to create some
libraries that could be used to build 3D graphics easily.
Basic tasks such as loading scene graphs and 3D objects also can be abstracted by the libraries.
A number of such libraries has been developed for this purposes.
One of the libraries that provides many high-level features is three.js.

4. So, let's talk about it.
4.1. Three.js is a cross-browser JavaScript library and Application Programming Interface (API)
based on WebGL and used to create and display animated 3D computer graphics in a web browser.
It allows create and render 3D animations using JS language only.

5. Three.js includes the following features:

 - Scenes: allow add and remove objects at run-time.
 - Cameras: perspective and orthographic;
 - Objects: meshes, particles, sprites, lines, ribbons, bones and more - all with Level of details
 
 - Geometry: plane, cube, sphere, torus, 3D text and more
 - Animation: forward kinematics, inverse kinematics, keyframes and others
 - many various Effects.

 - Lights sources can be ambient, direction, point and spot; shadows: cast and receive
 - Materials: colors, textures and more
 - Data loaders: for binary, image, JSON and scene
 
 - Support includes API documentation, public forum and wiki in library's web page
 - Over 150 files of coding examples plus fonts, models, textures, sounds and other support files
 - Debugging represented by WebGL Inspector and Three.js Inspector

6. Now I want to show a small code example

6.1. First we have to include The Three.js library within a web page by linking to its copy. 
It can be a local copy or a remote one.

6.2. Let's make new Scene. 
We need at least one camera. 
Then We have to pass Camera and Scene as parameters in Renderer to draw scene in canvas DOM Element.
Main unit to draw an object in Scene is Mash. It gets an geometry (may be box, sphere or more complex)
and material (color or texture) as parameters. In our example mesh is a cube with image as texture.

6.3. So, we add our cube at the scene. Set camera position.
And set a cube position change between animation frames.

6.4. And now you can see the result of our example.
It's pretty good isn't it? Less then 20 code lines.

7. In conclusion I want to give a links to WebGL and Tree.js sites.