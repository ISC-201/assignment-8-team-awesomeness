# Assignment 8
In this assignment we will pave the way for a formal rendering engine using OpenGL's programmable pipeline. We will start with some improvements to the code used in class to render simple polygons.

- [ ] If you haven't already please create a release for version **v0.0.1**. It should represent your work for Assignment 7.
- [ ] Create a new `Renderer` base class, this will be used to render "renderable" objects.
  - [ ] Create a new specialized `OpenGLRenderer` class.
    * Design the renderer class interface as you see fit. Start by moving VAO, VBO, and EBO logic into it. We will expand on this further down the road.
- [ ] Update the rendering code to use VBO indexing. Read more about this [here](http://www.opengl-tutorial.org/intermediate-tutorials/tutorial-9-vbo-indexing/).
- [ ] Create a new `Shader` type to hold your shader related data. From uniforms to the actual resulting program.
  - [ ] Your `Shader` type should be receive a pair list containing the file path and a shader type as part of it's program composition. Each shader in the list should be loaded and attached to a program.
  - [ ] Your `Shader` should be aware of all of its available **attributes**. (See `glGetProgramiv`)
  - [ ] Your `Shader` should be aware of all of its available **uniforms**. (See `glGetProgramiv`)
  - [ ] Your `Shader` have an accessor that returns the Id of an existing uniform and a *-1* if the requested value does not exist.
  - [ ] In case of errors, if on Windows and using MSVC++, display the compilation errors on a message box. When compiling from Linux or MacOS `cerr` should be used.
    * Errors should be very descriptive, you should provide:
      * the file name, 
      * the file line, 
      * the error message, 
      * the current OpenGL version, 
      * the registered version of GLSL on the shader program,
      * the raw error message
- [ ] Add utility functions and classes as you see fit. 
- [ ] Adds debugging tools like switching between wireframe view and regular view, gl error checking with file and line reporting, etc.

### Notes
* Code should look clean and design should allow for scope creep and growth. Feel free to do whatever you see fit to achieve this.
* After our class discussions, please, improve your matrix code as much as you can. It will play a critical role further down the road.
* If you haven't already use folders and namespaces to organize your code and physical files properly.
* **HINT:** At the end of this assingment your `App` class should only know about the `Renderer` class.
