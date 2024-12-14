# Expo ImagePicker: Intermittent undefined uri

This repository demonstrates a bug in Expo's ImagePicker component where the `uri` property of the selected image sometimes returns `undefined`, even when image selection is successful. This inconsistency can lead to application crashes or unexpected behavior.

## Bug Description

The issue is not directly related to user actions but likely stems from asynchronous operations within the ImagePicker component. The `uri` property becomes `undefined` intermittently, making it unreliable for further image processing.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an iOS or Android device or simulator.
4. Select an image using the ImagePicker.
5. Observe that the `uri` property may or may not be defined, even with successful image selection.

## Solution

The solution involves adding error handling and checking for the existence of the `uri` property before processing the image. See the `bugSolution.js` file for the corrected code.