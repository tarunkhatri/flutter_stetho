# flutter_stetho

Flutter stetho by Tarun Khatri (Null Safe support added)

## Getting Started

How can you too get this plugin up and running in your own app? Follow these steps.

### Install the plugin  

Add `flutter_stetho` to your dependencies in the `pubspec.yaml` file

```dart
dev_dependencies:
  flutter_stetho:
    git:
      url: git://github.com/tarunkhatri/flutter_stetho.git
      ref: master
```

### Install StethoHttpOverrides

Next, you'll need to install the `Stetho.initialize()` in the main() function of your app. This will enable Stetho and allow `flutter_stetho` to wrap all http calls and report information to the Chrome Dev Tools via the Stetho package from Facebook.

Note: It's probably a good idea only put this override in [a `main_dev.dart` file](https://flutter.rocks/2018/03/02/separating-build-environments-part-one/). 

```dart
import 'package:flutter_stetho/flutter_stetho.dart';

void main() {
  Stetho.initialize();

  runApp(new MyApp());
}
```

### Run your app on an Android Device

`flutter run`

### Open Brave

Pop open Chrome or Chromium, navigate to `brave://inspect`

You should now see your App appear in the window.

