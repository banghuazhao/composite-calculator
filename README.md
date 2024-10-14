# Composite Calculator

A Flutter package for calculating various properties of composite materials. This package includes modules for different composite calculations, such as lamina and laminate properties.

## Installation

Add this package to your `pubspec.yaml` file:

```yaml
dependencies:
  composite_calculator: ^1.0.0
```

Then, run:

```yaml
flutter pub get
```

## Usage

Here's a quick example of how to use the `LaminatePlatePropertiesCalculator` to calculate laminate plate properties.

```dart
import 'package:composite_calculator/models/laminate_plate_properties_input.dart';
import 'package:composite_calculator/calculators/laminate_plate_properties_calculator.dart';

void main() {
  // Create an instance of LaminatePlatePropertiesInput with necessary properties
  LaminatePlatePropertiesInput input = LaminatePlatePropertiesInput(
    E1: 150000,
    E2: 10000,
    G12: 5000,
    nu12: 0.3,
    layupSequence: "[0/90/45/-45]s",
    layerThickness: 0.125,
  );

  // Perform the calculation
  LaminatePlatePropertiesOutput output = LaminatePlatePropertiesCalculator.calculate(input);

  // Print or utilize the output as needed
  print(output);
}
```

## Project structures
The project consists of several calculators and models:

* **Calculators**: Contains calculators for different composite property calculations.
* **Models**: Defines the input and output data structures for the calculators.
* **Utils**: Utility classes and extensions.

## Example Project
To see this package in action, check out [SwiftComp Flutter](https://github.com/banghuazhao/swiftcomp-flutter), an example project that utilizes this package to perform composite material calculations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.