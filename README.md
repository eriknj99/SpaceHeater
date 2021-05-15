# SpaceHeater
Render Blender Cycles animations using ALL of your rendering devices!

![clip5](https://user-images.githubusercontent.com/11905989/118059176-dd3c9e80-b35d-11eb-8bef-98654a534c9d.png)

This script dispatches individual frames to the selected rendering devices and displays the progress in a neat way. 
This approach allows blender to use multiple graphics APIs and the CPU to render a single animation. 

# Usage

		Change the output of your animation to an image sequence rather than a video. 

		Example Usage 

    SpaceHeater --blendFile demo.blend --startFrame 5 --endFrame 10 --device CUDA --device OPENCL --device CPU

    -Required Arguments-
    --blendfile <filename>  : The blender file to render.
                                    The render settings from the file will be used except for start frame, end frame, and render device 
    --startFrame <frame>    : The start of the animation (Inclusive)
    --endFrame <frame>      : The end of the animation (Inclusive)
    --device <device>       : Add device to the list of rendering devices. 
                                    Options: CPU CUDA OPTIX OPENCL
                                    You must configure these devices in blender before you can use them 

    -Optional Arguments-
    --color <true/false>    : Enable colored output
    --help                  : Display this text


Only tested on Linux 
