# Exercise-06d-Shaders
Exercise for MSCH-C220, 19 April 2021

I didn't want the semester to end without giving you a change to play with shaders in Godot. Included in this repository are a haphazard collection of open source Godot shaders (from a variety of sources, listed below). This exercise should give you a chance to see how shaders work.

Fork this repository. When that process has completed, make sure that the top of the repository reads [your username]/Exercise-06d-Shaders. *Edit the LICENSE and replace BL-MSCH-C220-S21 with your full name.* Commit your changes.

Clone the repository to a Local Path on your computer.

Open Godot. Import the project.godot file and open the "Shaders" project.

In res://Game.tscn, I have provided a scene contains a camera and three 3D meshes (cube, sphere, and cone). There is also a ColorRect that appears in a UI Control node.

In each of the four instances (cube, sphere, cone, and ColorRect), I have applied Shader materials and with the following parameters.

These are the steps I followed:

Select the Cube and in the Inspector, create a new Shader Material. Edit that material, and in Shader parameter, Load res://Shaders/spatial/force_field1.tres. Then adjust the Shader Param fields as follows:
 * Base Color: #8ce99a
 * Hex Tex: New Noise Texture
  * Noise: New OpenSimplexNoise

Next, select the Sphere, and create a new Shader Material. Edit that material, and in the Shader parameter, Load res://Shaders/spatial/water_3d.shader. Then adjust the Shader Param fields as follows:
 * Deep Color: #1c7ed6
 * Shallow Color: #4dabf7
 * Foam Cutoff: 0.55
 * Foam Color: #e7f5ff
 * Depth Distance: 20
 * Refraction Noise: New Noise Texture
  * Noise: New OpenSimplexNoise
  * As Normalmap: On
  * Bump Strength: 20
 * Foam Noise: New Noise Texture
  * Noise: New OpenSimplexNoise
 * Displacement Noise: New Noise Texture
  * Noise: New OpenSimplexNoise

Next, select the Cone, and create a new Shader Material. Edit that material, and in the Shader parameter, Load res://Shaders/spatial/dissolve.shader. Then adjust the Shader Param fields as follows:
 * Albedo: #000000
 * Emission Color: #ffffff
 * Emission Amount: 0.2
 * Burn Size: 0.5
 * Dissolve Amount: 1
 * Dissolve Texture: New Noise Texture
  * Noise: New OpenSimplexNoise

Finally, select the UI/ColorRect, and under Material->Material create a new Shader Material. Edit that material, and in the Shader parameter, Load res://Shaders/canvas_item/Fire.shader.

Save the scene, and Run the current scene. See how the shader materials interact with each of the objects.

Quit Godot. In GitHub desktop, add a summary message, commit your changes and push them back to GitHub. If you return to and refresh your GitHub repository page, you should now see your updated files with the time when they were changed.

Now edit the README.md file. When you have finished editing, commit your changes, and then turn in the URL of the main repository page (https://github.com/[username]/Exercise-06d-Shaders) on Canvas.

The final state of the file should be as follows (replacing the "Created by" information with your name):
```
# Exercise-06d-Shaders
Exercise for MSCH-C220, 19 April 2021

An exploration of canvas_item and spatial Shaders in Godot.

## Implementation
Built using Godot 3.2.3

Shaders collected from the following repositories:
 * [GDQuest/godot-shaders](https://github.com/GDQuest/godot-shaders)
 * [gamedevserj/Godot-Shaders](https://github.com/gamedevserj/Godot-Shaders)
 * [curly-brace/Godot-3.0-Noise-Shaders](https://github.com/curly-brace/Godot-3.0-Noise-Shaders)
 * [curly-brace/godot_force_shield_shader](https://github.com/curly-brace/godot_force_shield_shader)
 * [IINinja/Godot.3.2.2-Ported-Shaders](https://github.com/IINinja/Godot.3.2.2-Ported-Shaders)
 * [Deep-Fold/PixelPlanets](https://github.com/Deep-Fold/PixelPlanets)
 * [CaptainProton42/SkyAquarium](https://github.com/CaptainProton42/SkyAquarium)

## References
[Godot Docs Shader Tutorial](https://docs.godotengine.org/en/stable/tutorials/shading/your_first_shader/index.html)

[The Book of Shaders](https://thebookofshaders.com/)

[ShaderToy](https://www.shadertoy.com/)

Excellent Godot Shader (2D) examples are avaiable at:
 * [Deep-Fold/PixelPlanets](https://github.com/Deep-Fold/PixelPlanets)
 * [Deep-Fold Spaceship Generator](https://deep-fold.itch.io/spaceship-generator)
 * [Deep-Fold Kurzgesagt Star](https://deep-fold.itch.io/kurzgesagt-star)

## Future Development
None

## Created by 
Jason Francis
```