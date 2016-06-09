# MTKView-ContentScaleFactor-OSX
A simple category to support the UIView.contentScaleFactor property on OSX (currently MTKView only)

On iOS the UIView class provides the property contentScaleFactor

This is useful when using an MTKView to change the view scale factor to trade image quality for improved rendering performance. By reducing the contentScaleFactor the Metal shader will be passed a smaller texture to render to reducing the processing requirement, the view will then scale the texture back up to full resolution. 

This allows an application to maintain a desired FPS (frames per second).

This property is not supported on OSX NSView, when writing cross platofrm (iOS and OSX) metal apps it means adding conditional blocks around code calling contentScaleFactor.

On OSX it is still possible for the GPU to take too long to render a frame to maintain FPS.

This category adds the contentScaleFactor propety to an MTKView when building for OSX.

