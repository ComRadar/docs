# Matrices

Some short guide here about matrices in general.

---

## Matrix Manipulation

Stormworks provides a limited set of matrix functions that are useful for transforming positions of objects in scripts:

### matrix.multiply

Multiply two matrices together.

```lua
out_matrix = matrix.multiply(matrix1, matrix2)
```

Very useful in combination with matrix.translation when you need change or randomize matrix.

```lua
local old_transform = server.getVehiclePos(vehicle_id)
local new_transform = matrix.multiply(old_transform, matrix.translation(0, -2, 0))
```

### matrix.invert

Invert a matrix.

```lua
out_matrix = matrix.invert(matrix1)
```

### matrix.transpose

Transpose a matrix.

```lua
out_matrix = matrix.transpose(matrix1)
```

### matrix.identity

Return an identity matrix.

```lua
out_matrix = matrix.identity()
```

Return a rotation matrix rotated in the X axis.
out_matrix = matrix.rotationX(radians)
Return a rotation matrix rotated in the Y axis.
out_matrix = matrix.rotationY(radians)
Return a rotation matrix rotated in the Z axis.
out_matrix = matrix.rotationZ(radians)
Return a translation matrix translated by x,y,z.
out_matrix = matrix.translation(x,y,z)
Get the x,y,z position from a matrix.
x,y,z = matrix.position(matrix1)
Find the distance between two matrices.
dist = matrix.distance(matrix1, matrix2)
Multiplies a matrix by a vec 4.
out_x, out_y, out_z, out_w = matrix.multiplyXYZW(matrix1, x, y, z, w)
Returns the rotation required to face an X Z vector.
out_rotation = matrix.rotationToFaceXZ(x, z)