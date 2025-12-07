# SteadyRead - Hand Tremor Stabilization

A proof-of-concept React web app designed to help people with hand tremors read text on their mobile devices by compensating for screen movement through motion stabilization.

## Overview

This POC demonstrates the core stabilization mechanics using a simple ball physics simulation. The app uses device gyroscope and accelerometer data to detect hand movement and applies counter-forces to keep content stable on screen.

## Features

- **Ball Physics Simulation**: Visual demonstration of tilt-based movement using device orientation sensors
- **Boundary Detection**: Ball bounces off screen edges with realistic physics
- **Dual Modes**:
  - **Stabilize Mode** (Black): Ball moves naturally with device tilt
  - **Release Mode** (Blue): Applies counter-forces to center and stabilize the ball
- **Real-time Coordinates**: Display of X, Y positions and adjusted New-X, New-Y values
- **iOS Compatibility**: Includes permission handling for iOS 13+ motion sensor access
- **Mobile-First Design**: Optimized for phone browsers with DeviceOrientation API

## Technical Details

### Physics System
- Gravity and damping simulation
- Bounce mechanics with energy loss
- Stabilization through opposing forces and centering

### Stabilization Mechanism
- Counter-forces applied to neutralize device tilt
- Centering forces to maintain ball position
- Enhanced damping during stabilization mode

### Color Scheme
- Black (#333333) for normal mode
- Royal Blue (#4169E1) for stabilizing mode
- Gray background (#d9d9d9)

## Usage

1. Open the app on a mobile device with motion sensors
2. Grant motion sensor permissions when prompted (iOS)
3. Watch the ball respond to device tilt
4. Tap "Stabilize" to activate counter-forces
5. Observe coordinates showing original and stabilized positions

## File Structure

```
src/
  └── tremor-stabilization.jsx  # Main React component
```

## Future Development

This POC validates the stabilization approach. Next steps would involve:
- Applying stabilization to actual text content
- Performance optimization
- User testing with individuals who have hand tremors
- Settings for sensitivity adjustment

## Platform

Built with React using the DeviceOrientation API for mobile browsers.
