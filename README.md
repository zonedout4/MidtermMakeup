# MidtermMakeup

## Reflection Shader
<img width="1714" height="1320" alt="image" src="https://github.com/user-attachments/assets/644bd00f-6603-4222-80f1-c09a2408cfa3" />
My Reflection Shader is a modification of the cubemap reflection shader shown in class. This shader is different in that it maps all the reflected light to an additional Texture2D (dubbed ReflectionShader). It multiplies the cubemap reflection by the texture, then multiplies it by a Strength float, then by a tint to control the color of the reflected light, and finally outputs to the Emission slot. The shader also has modifiable inputs for the object's base texture and base color tint, which output to the Base Color slot. I applied this texture to the player, since the frog looks like a slimy shiny guy, and having adjustable reflection textures and colors will make it easy to adapt this shaders to levels with different environments.

## Texture Tiling Shader
<img width="2012" height="1282" alt="image" src="https://github.com/user-attachments/assets/71522147-6be5-482e-b004-ec8590d28b96" />
My Texture Tiling Shader simply maps a Tiling Variable to both the X and Y axis of a UV tiling and mapping node. This allows the tiling to be modified on both axis simultaneously in editor for uniform scaling. This is useful to replicate the retro aesthetic of the tiled floor in the original game with minimal effort in-editor.

## Multiple UVs Shader
<img width="2128" height="1206" alt="image" src="https://github.com/user-attachments/assets/255044ef-f6a4-4e07-b384-2d69d8bd7bbd" />
My Multiple UV Shader uses a sine node with time as an input, then checks if the result is above 0. If it is above 0, it uses UV(0), otherwise it uses UV(1). This means that the UVs will switch in approximately even intervals. There is an input to adjust the speed. I used this for the fireball to make it seem like the fire is flickering.

## General Shader
<img width="1726" height="1288" alt="image" src="https://github.com/user-attachments/assets/b7497c63-b4c5-47e4-9723-4b996138651a" />
The general shader is simply a default lit shader graph with a modifable Base Texture and Base Color Tint. This uses Unity's default parameters for metallic and roughness and applies the default implementation of diffuse and ambient lighting. This is useful for simple, static objects that don't need complex materials. I applied this to the pillars, since they are made of stone and all they do is fall downs, so they don't need anything custom or dynamic.

## Texture Offset Wave Shader (Additional Shader of my Choice)
<img width="2294" height="1228" alt="image" src="https://github.com/user-attachments/assets/33152e02-876c-46a5-b374-c27b262d69ee" />
I used a similar method to the Texture Tiling Shader to have the X offset of a texture move according to a sine wave over time. There is an input for speed and strength. This gives the texture the effect of a moving wave, so I applied it to the lava to make it feel more fluid.
