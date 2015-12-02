# blender opengex-exporter for [ Tesla Game engine ](https://github.com/fulhax/tesla)

mostly the same as the official [ opengex exporter ](http://opengex.org) just added tangents+binormal-signs

to get the correct result do this calculation in the fragment shader
Binormal = binormal-sign * cross(Normal, Tangent);
Normalout = normalize( normalTexture.x * Tangent + normalTexture.y * Binormal + normalTexture.z * Normal );
