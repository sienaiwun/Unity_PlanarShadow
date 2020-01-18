# Unity_PlanarShadow
In Unity's Scriptable Rendering Pipeline(SRP) framework, MonoBehaviour.OnRenderObject() is deprecated. However, there are always some needs to add custom per-mesh or per-object drawing besides their own materials' rendering drawing calls. For example, the planar shadow call is a very cheap and efficient way to add a shadow on a plane, it needs a custom additional drawing to the objects which casts shadow.

![planer_shadow](https://github.com/sienaiwun/publicImgs/blob/master/imgs/planer_shadow.gif?raw=true)

In this demo, we restore OnRenderObject() in the Universal Rendering Pipeline using SRP.  We give a demo to add custom draws - which are the planar shadow drawing call- to a mesh (the sphere) and a prefab (the props). We can also specify the drawing's order in the drawing script.

To Do:
Batch the custom draw calls.
