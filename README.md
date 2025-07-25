# Rasterization-occlusion-anti-aliasing with Eigen (computer graphics) 
My solution to Games101 exercise 2

antialiasing with 2 * 2 MSAA

<img width="451" height="361" alt="Screenshot from 2025-07-12 02-02-04" src="https://github.com/user-attachments/assets/3e1188c2-c031-4033-a7c2-2800ad295119" />

<img width="590" height="425" alt="Screenshot from 2025-07-12 02-03-19" src="https://github.com/user-attachments/assets/df616632-5a0b-4cb5-b6ce-02f3af6fd692" />

There're two triangles with different z depths. The goal is to display the yellow triangle in front of the blue one.

The main task
1. implement insideTriangle() to check if a point is in a triangle
2. implement rasterizer::rasterize_triangle() to paint the triangle and do occlusion
3. Use MSAA to do anti-aliasing

The triangle is applied with
viewing transformation
- model transformation
- view/camera transformation
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
