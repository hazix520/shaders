# Shaders

[Video Link](https://youtu.be/bp3CmpvxUL8)

# Code

'void main () {'
    
    vec2 uv = uv();
    
    vec3 c = black;
    
    
    float x = noise(uv);
    float y = vrmf(rotate(uv, vec2(0.2,0.2), time), 2);
    
    c += sin(blue * sin(time) * x * 10./(y * sin(time /4.)));
    c+= sin(red * y * sin(time) * 2.);
    
    
   'gl_FragColor = vec4(c,1.);'
}
