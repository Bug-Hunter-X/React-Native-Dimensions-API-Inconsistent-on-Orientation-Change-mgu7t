# React Native Dimensions API Inconsistent on Orientation Change

This repository demonstrates a common issue in React Native development where the `Dimensions` API fails to update correctly when the device orientation changes. This can lead to layout issues and visual glitches in your app.

## Problem

The `Dimensions.get('window')` method returns the screen dimensions. However, this value isn't automatically updated when the device is rotated. This means that components that rely on these dimensions for their layout might render incorrectly after an orientation change.

## Solution

The solution involves using the `Dimensions` API's `addEventListener` method to listen for changes in screen dimensions, thus ensuring that the component re-renders with updated dimensions after the screen rotation.