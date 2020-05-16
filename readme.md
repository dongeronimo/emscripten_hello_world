#Hello Emscripten

Demonstrates how to use emscripten to compile a simple hello world c++ program to 
javascript

##setup:
###emscripten:
Pull it from the repo then go to it's directory. Then
``` 
$ ./emsdk install latest
$ ./emsdk activate latest
$ source ./emsdk_env.sh
```
That will set emscripten and put it's programs in the shell's path.

###cmake:
Using the cmakelists.txt in this project I will create a build directory and
change to it. Then...
```
$ emcmake cmake ...
$ emmake make
```

The final result is a javascript and an index.html scaffolded by emscripten to use 
that js file. The js file will use the .wasm that was generated.

###Running:
Assuming that the machine has python3 installed I run, inside the build directory:
```
$ python3 -m http.server
``` 

That will start a quick and dirty http server with the contents of the current directory,
at 127.0.0.1:8000
