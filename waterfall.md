# Ray Tracing, A Waterfall

[back to home](/index.md)

This is my Ray Tracer that I created for the final project of CS 488: Computer Graphics at the University of Waterloo in the Spring 2019 term. I recieved the bronze medal. 

My goal was to create a scenic scene of a waterfall, attempting to model water and textures.

My final paper can be found [here](waterfall-images/finalpaper.pdf) with details on theory and implementation along with references.

### Objective 1: Extra Primitives - Cylinder and Torus
<img src="waterfall-images/objective-cylinder.png">

<img src="waterfall-images/objective-torus.png">

### Objective 2: Antialiasing (super sampling)
Original:
<img src="waterfall-images/all-primitives-no-anti.png">

With anti-aliasing:
<img src="waterfall-images/all-primitive-anti.png">

### Objective 3: Depth of Field
Original:
<img src="waterfall-images/objective-dof.png">

With depth of field:
<img src="waterfall-images/objective-no-dof.png">

### Objective 4: Glossy Reflection
Mirror reflection: (previously completed)
<img src="waterfall-images/objective-glossyreflection1-off.png">

Glossy reflection:
<img src="waterfall-images/objective-glossyreflection1-on.png">

--

Mirror reflection:
<img src="waterfall-images/objective-glossyreflection2-off.png">

Glossy reflection:
<img src="waterfall-images/objective-glossyreflection2-on.png">

### Objective 5: Refraction
No refraction:
<img src="waterfall-images/objective-refraction1-off.png">

Refractive index = 1, fully transmissive:
<img src="waterfall-images/objective-refraction-1.png">

Refractive index = 1.5:
<img src="waterfall-images/objective-refraction-1.5.png">

### Combining Reflection and Refraction
Only reflection:
<img src="waterfall-images/objective-refractreflect-reflect.png">

Only refraction:
<img src="waterfall-images/objective-refractreflect-refract.png">

Both reflection and refraction:
<img src="waterfall-images/objective-refractreflect-both.png">

### Objective 6: Soft Shadows
Original:
<img src="waterfall-images/objective-softshadows-off.png">

With soft shadows:
<img src="waterfall-images/objective-softshadows.png">

### Objective 7: Texture Mapping
<img src="waterfall-images/objective-texture.png">

### Objective 8: Bump Mapping
<img src="waterfall-images/objective-bump.png">

### Texture Mapping vs Bump Mapping
The differences between texture mapping and bump mapping are subtle, and one single image could be either. The difference is that when the light source moves, the texture mapped image remains the same as it is just an image applied. However, on the bump mapped image, the highlights and shadow shift as we are simulating bumps on the surface of the object.

This can be seen in the comparison of two gifs:

<img src="waterfall-images/texture-gif.gif">
<img src="waterfall-images/bump-gif.gif">

### Objective 9: Perlin Noise

<img src="waterfall-images/objective-perlin.png">

Perlin noise can also be difficult to differentiate from bump and texture mapping, as a texture or bump map could have a static perlin noise image. Therefore, I can show that with slight variations in provided coordinates, the perlin function can change slowly and show that it is being generated using Perlin noise:

<img src="waterfall-images/perlin-gif.gif">

### Bonus: “Mist” (Volumetric Material)

<img src="waterfall-images/bonus-mist.png">

To achieve this, the intersection point t was computed, and then a random distance was added according to a set density value. (from Ray Tracing: The Next Week, Peter Shirley)

### Final Scene
<img src="waterfall-images/final-scene-image.png">

<img src="waterfall-images/final-scene-gif.gif">
