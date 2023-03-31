# Blockscript

##### what is bkscript (blockscript)?

Blockscript is an open standard file format for storing a region of a Minecraft world for the purpose of serialization and storage of the region in plain-text.

## what does it look like?

Blockscript is a **list** of different instructions seperated by a comma (Example: `step-1,step-2`).

### Single Block

```
x:y:z=namespaced_id
```

This instruction represents a single block in the Minecraft world.
The `x`, `y`, and `z` values represent the coordinates of the block, and the `namespaced_id` represents the type of block (Example: `minecraft:dirt`). To specify multiple blocks, separate each block with a comma.

### Fill blocks

To save resources, the `fill` syntax can be used to fill multiple blocks with the same type of block. The schema for the `fill` syntax is as follows:

```
x1:y1:z1>x2:y2:z2=namespaced_id
```

This instruction represents a rectangular area of blocks with the same type.
The `x1`, `y1`, and `z1` values represent the coordinates of one corner of the rectangle, and the `x2`, `y2`, and `z2` values represent the coordinates of the opposite corner of the rectangle.
