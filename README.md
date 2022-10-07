# raytracing_notes
Bounding Volume - A box/some other shape that goes around an object in a scene. Ray tracing intersections first check if the ray passes through the bounding volume, and then only iterates through all the triangles in the object if it hits the volume. Optimization to reduce redundant intersection calculations.

BVH (Bounding Volume Hierarchy) - Have bounding box for all objects, and partition into smaller and smaller trees with less objects in each. Boxes can overlap each other. Recursive binary tree of boxes. Typically split at midpoint of volume, or sorted to have half of objects on each side, or uses another modeling hierarchy. Hierarchy construction tends to exploit Z buffer (according to NVIDIA blog)
