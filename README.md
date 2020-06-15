# Computer Graphics – Final Competiton

My final competition is based on A3 Ray Tracing for galaxy plane and some sphere planets with their own simple texture mapping.

First I set all the shading material pararmeters ka, kd, ks, km to 0 for all objects, but except the phong exponentials has their own specific value in `src/creative.json`. According to the phone exponentials, it can be clearly identified each planets and the galaxy plane. For each different object I applied corresponding textures repectively. Therefore I modified `src/raycolor.cpp` and add 3 files, `src/rgba_to_rgb.cpp` from A1, `src/raycolor_shading.cpp` and `src/bp_color_shading.cpp`.

I read each texture .png files for each objects with `read_rgbs_from_png.h` from A1 and then converted rgba to rgb for eah object with `src/rgba_to_rgb.cpp` from A1.

In `src/raycolor.cpp`, I set different rgb to each different objects based on their phong exponentials, and set with its own texture rgb. With the updated rgb, I did the raycolor shading with ambient shading one more time using `src/raycolor_shading.cpp` and `src/bp_color_shading.cpp`, which are similar to `src/raycolor.cpp` and `src/blinn_phong_shading.cpp` but without the texture phong exponential checking and it based on the update colour rgb. 

The result ppm is `final.ppm`.

