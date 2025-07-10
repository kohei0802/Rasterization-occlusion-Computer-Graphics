# Rasterization-occlusion-Computer-Graphics
My solution to Games101 HW2 

Eigen library. 

There're two triangles with different z depths. The goal is to display the yellow triangle in front of the blue one.

The main task
1. implement insideTriangle() to check if a point is in a triangle
2. implement rasterizer::rasterize_triangle() to paint the triangle and do occlusion
3. Use MMSA to do anti-aliasing

The triangle is applied with
MVP transformation
- model transformation
- view/viewing transformation
- perspective projection transformation
- viewport transformation

# Build
You need OpenCV and Eigen library locally to build this project. 

If you're on Ubuntu, run 
1. sudo apt install libeigen3-dev
2. sudo apt install libopencv-dev

then, go into ./build/ directory or create one if it's not there and run
1. cmake ..
2. make
3. ./Rasterizer image.png 
or 
3. ./Rasterizer
