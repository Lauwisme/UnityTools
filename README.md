UnityTools
==========

A collection of scripts that I've written for my silly prototypes, including:

* `Inp` to handle touch and mouse input the exact same way. Use the `Inp.ut` singleton to access the stuff, and make sure to put the `Inp` class before anything else in Edit > Project Settings > Script Execution Order.
* `ColliderToMesh` to add a mesh to Unity’s 2D polygon collision so that you can use Unity’s collider editor to quickly ‘draw’ a mesh.
* `DynamicPositionAnimation` for when you want to animate the position of something through code rather than the set values that Unity’s Mechanim uses.
* `AccelerationInput` to get the rough acceleration over an X amount of frames, or to subscribe to an acceleration trigger. Use `AccelerationInput.Sample(sampleFrameAmount)` to sample a bunch of frames, or `AccelerationInput.SetTrigger(YourFunction, triggerForce)` to subscribe a trigger event when there is enough force. Note that my class uses `FixedUpdate()` and works with the `UnityEngine.Input.acceleration` variable, which doesn’t give you as much precision as `UnityEngine.Input.accelerationEvents`.