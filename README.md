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
  <img src="https://via.placeholder.com/300x200?text=Basic+Example" width="30%"/>
  <img src="https://via.placeholder.com/300x200?text=Lines+Example" width="30%"/>
  <img src="https://via.placeholder.com/300x200?text=Images+Example" width="30%"/>
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

<img src="https://via.placeholder.com/300x200?text=Basic+Example+Preview" width="100%"/>

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
<img src="https://via.placeholder.com/300x200?text=Lines+Example+Preview" width="100%"/>

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

<img src="https://via.placeholder.com/300x200?text=Images+Example+Preview" width="100%"/>

## 🛠️ Configuration

### Particle Settings