# Expo Camera Preview Render Issue

This repository demonstrates a bug in the Expo Camera API where the camera preview fails to render correctly on initial mount. The preview might appear black or display a distorted image. This issue seems to be related to asynchronous operations during camera initialization and configuration.

## Bug Description
When using the Expo Camera with custom controls and the `onCameraReady` prop, the initial preview often doesn't render correctly.  The issue is particularly prominent when other UI elements are present that depend on camera initialization.

## Reproduction
1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the app using `expo start`.
4. Observe the camera preview on initial mount. It will likely be black or distorted.

## Solution
The solution involves ensuring that the camera preview is only rendered after the camera is fully initialized and configured. This is achieved by using state management to control the rendering of the camera preview based on the `onCameraReady` callback.