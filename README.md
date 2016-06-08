# MTKView-ContentScaleFactor
A simple category to support the MTKView.contentScaleFactor property on OSX

On iOS the UIView class provides the property contentScaleFactor

This is useful when using an MTKView to change the scale factor to trade image quality for rendering performance.

This property is not supported on OSX NSView, when writing cross platofrm (iOS and OSX) metal apps it means adding conditional blocks around contentScaleFactor.

This category adds contentScaleFactor propety to an MTKView when building for OSX

