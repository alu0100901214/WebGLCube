# WebGLCube

The parameters changed in this practice were the data about the cube vertexes, the cube indexes and the colors.

In order to render each side of the cube with a color, I needed to define separately each of the sides of the cube, 6 in total with 4 vertexes each.

```
private static readonly float[] cubeVertices =  {
        // TOP
        -1.0f,1.0f,-1.0f,
        -1.0f,1.0f,1.0f,
        1.0f,1.0f,1.0f,
        1.0f,1.0f,-1.0f,
        // LEFT
        -1.0f,1.0f,1.0f,
        -1.0f,-1.0f,1.0f,
        -1.0f,-1.0f,-1.0f,
        -1.0f,1.0f,-1.0f,
        // RIGHT
        1.0f,1.0f,1.0f,
        1.0f,-1.0f,1.0f,
        1.0f,-1.0f,-1.0f,
        1.0f,1.0f,-1.0f,
        // FRONT
        1.0f,1.0f,1.0f,
        1.0f,-1.0f,1.0f,
        -1.0f,-1.0f,1.0f,
        -1.0f,1.0f,1.0f,
        // BACK
        1.0f,1.0f,-1.0f,
        1.0f,-1.0f,-1.0f,
        -1.0f,-1.0f,-1.0f,
        -1.0f,1.0f,-1.0f,
        // BOTTOM
        -1.0f,-1.0f,-1.0f,
        -1.0f,-1.0f,1.0f,
        1.0f,-1.0f,1.0f,
        1.0f,-1.0f,-1.0f
    };
```

The same happens with the indexes that represent the triangulation of each of the sides, 2 triangles per side in a total of 6 faces.

```
private static readonly int[] intCubeIndices =  {
        // TOP
        0, 1, 2,
	0, 2, 3,
        // LEFT
        5, 4, 6,
	6, 4, 7,
        // RIGHT
        8, 9, 10,
	8, 10, 11,
        // FRONT
        13, 12, 14,
	15, 14, 12,
        // BACK
        16, 17, 18,
	16, 18, 19,
        // BOTTOM
        21, 20, 22,
	22, 20, 23
    };
```

And for the colors I have defined a different color for each of the vertices of the 6 faces. Making sure that on each side of the cube the vertexes have the same color.

```
private float[] cubeColors= new [] {
    // TOP (Yellow)
    1f, 1f, 0f, 0.8f,
    1f, 1f, 0f, 0.8f,
    1f, 1f, 0f, 0.8f,
    1f, 1f, 0f, 0.8f,
    // LEFT (Orange)
    1f, 0.6f, 0f, 0.9f,
    1f, 0.6f, 0f, 0.9f,
    1f, 0.6f, 0f, 0.9f,
    1f, 0.6f, 0f, 0.9f,
    // RIGHT (Blue)
    0f, 0f, 0.75f, 1f,
		0f, 0f, 0.75f, 1f,
		0f, 0f, 0.75f, 1f,
		0f, 0f, 0.75f, 1f,
    // FRONT (Pink)
    1.0f, 0.0f, 0.5f, 1f,
		1.0f, 0.0f, 0.5f, 1f,
		1.0f, 0.0f, 0.5f, 1f,
		1.0f, 0.0f, 0.5f, 1f,
    // BACK (Green)
    0.0f, 1.0f, 0.5f, 1f,
		0.0f, 1.0f, 0.5f, 1f,
		0.0f, 1.0f, 0.5f, 1f,
		0.0f, 1.0f, 0.5f, 1f,
    // BOTTOM (Light Blue)
    0f, 0.5f, 1f, 0.6f,
		0f, 0.5f, 1f, 0.6f,
		0f, 0.5f, 1f, 0.6f,
		0f, 0.5f, 1f, 0.6f
};
```


Screenshot of the rendered cube:

![img](./img/WebGLCube.PNG)


GIF of the rendered cube:

![gif](./GIF/WebGLCube.gif)


