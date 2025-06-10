# ParticlesFX

<p align="center">
  <img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/logo.png" alt="ParticlesFX Logo" width="100%"/>
  <br>
  <em>A beautiful, performant particle animation system for Flutter apps</em>
</p>

<div align="center">

[![Pub Version](https://img.shields.io/pub/v/particles_fx)](https://pub.dev/packages/particles_fx)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Flutter Favorite](https://img.shields.io/badge/style-flutter__favorite-purple)](https://github.com/Solido/awesome-flutter)

</div>

## 🌟 Features

- 🎨 **Customizable particles** (points or images)
- ⚡ **Multiple collision modes** (optimized for performance)
- ✋ **Touch interaction** (particles react to user input)
- 🌈 **Visual effects** (lines, triangles, blur, fade animations)
- 📱 **Responsive design** (adapts to screen size changes)
- 🏎️ **Performance optimized** (quadtree, smart updates)

<div align="center">
  <img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="30%"/>
  <img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="30%"/>
  <img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="30%"/>
</div>

## 🚀 Installation

Add to your `pubspec.yaml`:

```yaml
dependencies:
  particles_fx: ^1.0.0
```

Then run:

```bash
flutter pub get
```

## 🧑‍💻 Usage

### Basic Setup

```dart
import 'package:particles_fx/particles_fx.dart';

ParticlesFX(
  width: 300,
  height: 200,
  particleSettings: ParticleSettings(
    numPoints: 50,
    maxSpeed: 1.5,
  ),
)
```

<img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="100%"/>

### With Lines Between Particles

```dart
ParticlesFX(
  width: MediaQuery.of(context).size.width,
  height: 300,
  lineSettings: LineSettings(
    enableLines: true,
    maxLineDistance: 100,
    lineColor: Colors.blue.withOpacity(0.3),
  ),
)
```
<img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="100%"/>

### Using Custom Images

```dart
ParticlesFX(
  width: 400,
  height: 400,
  particleSettings: ParticleSettings(
    numPoints: 30,
    assetImages: ['assets/particle.png'],
    imageSize: 24,
  ),
)
```

<img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="100%"/>

## 🛠️ Configuration

### Particle Settings

|Parameter | Type	| Default | Description|
|----------|------|---------|------------|
| numPoints            | int          | 50   | Number of particles           |
| maxSpeed             | double       | 1.0  | Maximum particle speed        |
| enablePointCollision | bool         | true | Enable particle collisions    |
| assetImages          | List<String> | []   | Images to use instead of dots | 

### Line Settings

```dart
LineSettings(
  enableLines: true,
  maxLineDistance: 120,
  lineWidth: 1.5,
  lineColorFading: true,
)
```

### Animation Settings

```dart
ParticleAnimationSettings(
  particlesAnimationSeconds: 60,
  initOpacityAnimationSeconds: 2,
  enableInitOpacityAnimation: true,
)
```

## 🎨 Customization Examples

### Triangle Fill Effect

```dart
ParticlesFX(
  lineSettings: LineSettings(
    enableTriangleFill: true,
    triangleColor: Colors.purple.withOpacity(0.1),
  ),
)
```
<img src="https://github.com/Anton-Kulik-1998/particles_fx_test_repo/blob/main/assets/temporary_image.png" width="100%"/>

### Touch Interaction

```dart
ParticlesFX(
  touchReactionSettings: TouchReactionSettings(
    enableTouchReaction: true,
    maxTouchDistance: 150,
    touchSpeedMultiplier: 3.0,
  ),
)
```

## 📚 API Reference

### Main Classes

| Class      | Description |
|------------|-------------|
|ParticlesFX      | Main widget                | 
|ParticleSettings | Controls particle behavior | 
|LineSettings     | Configures connections     | 
|StyleSettings    | Visual styling options     | 

### Advanced Control

```dart
// Access particles manager
_particlesManager.updatePointsPosition();

// Control animations
_particlessAnimation.pausingAnimation();
```

## 🏆 Best Practices

1. Particle Count:
  - <100 particles: ParticlesUpdateMode.doubleCycleMode
  - 100 particles: ParticlesUpdateMode.quadtreeMode
2. Performance Tips:
  ```dart 
  // Disable collisions when not needed
  ParticleSettings(enablePointCollision: false);

  // Reduce line distance checks
  LineSettings(maxLineDistance: 80);
  ```

## 🤝 Contributing

We welcome contributions! Please see our contribution guidelines.

## 📜 License

MIT © [Anton Kulik]

<div align="center"> Made with ❤️ and Flutter </div> 

Key Features of This README:

Visual Hierarchy:
Emoji headers for quick scanning
Consistent section styling
Placeholder images for visual examples
Comprehensive Sections:
Installation instructions
Basic to advanced usage examples
Configuration references
API overview
Best practices
Interactive Elements:
Badges for version/license
Tabular data for settings
Code blocks with syntax highlighting
Professional Touches:
Contribution section
License information
Responsive image placeholders
Optimized for Pub.dev:
Clear feature showcase at top
Multiple usage examples
Visual previews

To use:

1. Replace placeholder images with actual screenshots
2. Update the license information
3. Add your contribution guidelines link
4. Customize the "Made with" footer

The README follows Flutter package best practices while maintaining visual appeal and clear information architecture.