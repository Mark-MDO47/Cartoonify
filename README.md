# Cartoonify
NVIDIA Jetson Nano implementation of Dan MacNish brilliant "Draw This" camera.
Apologies to Dan if I didn't capitalize the name correctly...
https://github.com/danmacnish/cartoonify

Dan and others have been busy! check out this area for a demo of what Dan's version can do
https://www.kapwing.com/cartoonify

Planning to use the new NVIDIA Jetson Nano to implement this with a few cosmetic enhancements

https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-nano/

https://smile.amazon.com/NVIDIA-Jetson-Nano-Developer-Kit/dp/B07PZHBDKT

$99, 5-10 watts, 4GB RAM, Jetson Nano module installed (NVIDIA Maxwell™ architecture with 128 NVIDIA CUDA® cores). This has an astonishing 472 MegaFlops of 16-bit floating point.

# 2019-07-07

Just took the nVidia "Hello AI World. Meet Jetson Nano." webinar - it was great! Makes me realize I might not need to install the full TensorFlow package although that is theoretically possible. When I actually tried it I kept running into the same configuration issues I have on the PC when using GPUs: it is extraordinarily picky about exactly which version of everything.

Also started the "Getting Started with AI on Jetson Nano" course (free) and did initial training of the ThumbsUp/ThumbsDown model, which is pretty fun!

I am thinking I may implement Cartoonify in C language; that seems pretty do-able on this platform.

# History

I had previously attempted this project with a Raspberry PI 3 but ran into lack of RAM (1GB maximum).
Also lots of configuration changes gave issues, what with Google TensorFlow updating so quickly and requiring changes to the NVIDA CUDA library and Microsoft Visual Studio to match it - don't get me started on overhead of keeping tools in sync!

I considered the Google Coral Dev Board, but ultimately its 1GB RAM (and my PC with an NVIDA GTX-1080 card) pushed me the other way.
https://coral.withgoogle.com/products/dev-board

Planning to use ResNet
https://github.com/tensorflow/models/tree/master/official/resnet
... recently moved:
https://github.com/tensorflow/models/tree/master/official/vision/image_classification

Okay, maybe SimpNet instead, but it only has CIFAR-100
https://arxiv.org/abs/1802.06205
https://github.com/Coderx7/SimpNet
