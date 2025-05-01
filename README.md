# Shaders

# Video
[Video Link](https://youtu.be/bp3CmpvxUL8)

# Code

    void main () {
    
    vec2 uv = uv();
    
    vec3 c = black;
    
    
    float x = noise(uv);
    float y = vrmf(rotate(uv, vec2(0.2,0.2), time), 2);
    
    c += sin(blue * sin(time) * x * 10./(y * sin(time /4.)));
    c+= sin(red * y * sin(time) * 2.);
    
    
    gl_FragColor = vec4(c,1.);
    }

# Explanation
For this shader assignment my goal was to procedurally generate interesting colors using different types of noise. The Force has some built-in noise functions that I played around with before doing my recording specifically noise() and vrmf(). vrmf() produced voronoi noise. I did this by changing the color using a sin wave that was multiplied by the noise function.

Throughout the recording there were some changes that drastically changes the output. While not intended I think this is one of the appeals of live coding. It documents the "happy accidents" you would never see if the process wan't recorded. In the video it's funny to see when I mess around with a variable and something cool happens. After I made the two noise variables mixing them around is really fun and created some interesting, unintended outputs.

