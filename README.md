# playing with openGL
---
OpenGL is a API that is in your graphics card and lets you to send information to graphics card. It provides set of functions that you can pass parameter to it and graphics card will render it on screen.

`install GLFW`

**GLFW** - its a library that let you create application window ( so you don't scratch head before even starting learning openGL *~kind of HEAD START*). Then you can render things on the screen.


>create **symlink** to the different project folder as i did it in linux [pop os] ( *thats why there's nothing inside the GLFW folder* ) . It can be done in windows too but with more hardwork that i didn't understood.

After that, enter this in your **task.json** file
```
"args": [
            "-g",
            "-std=c++17",
            "-c",
            "main.cpp",
            "&&",
            "g++",
            "main.o",
            "-o",
            "main.exec",
            "-lGL",
            "-lGLU", "-lglfw" ,"-lX11" ,"-lXxf86vm", "-lXrandr" ,"-lpthread" ,"-lXi" ,"-ldl", "-lXinerama", "-lXcursor",        
        ],
```
>its just terminal command that compiles and run you code ( *you can write this in your terminal also and it work same* ) but do look **"-lglfw"** in args as may create some problems, if it does change it to **"-lglfw3"**

After that, run it.

>If the program compiles and you can see main.exec & main.o file in the folder but it doesn't launch, edit the **launch.json** file, inside configuration edit this line

```
"program": "${fileDirname}/${fileBasenameNoExtension}.exec",
```






