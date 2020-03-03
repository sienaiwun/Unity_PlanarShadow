# Unity_PlanarShadow
In the Unity's Scriptable Rendering Pipeline(SRP) framework, MonoBehaviour.OnRenderObject() is deprecated. However, there are always some needs to add custom per-mesh or per-object drawings besides their own materials' rendering drawing calls. For example, the planar shadow call, which is a very cheap and efficient way to add a shadow to a object, needs a custom drawing to the objects which casts shadow.

![planer_shadow](https://github.com/sienaiwun/publicImgs/blob/master/imgs/planer_shadow.gif?raw=true)

In this demo, we restore OnRenderObject() in the Universal Rendering Pipeline using SRP.  We give a demo to add custom draws - which are the planar-shadow drawing calls- to a mesh (the sphere) and a prefab (the props). We can also specify the drawing's order in the drawing script.

## Cons:
1. Command buffer draw calls cannot be batched very easily.
2. Custom culling or disableing this draw call is needed if this draw does not contribute to the final view.

