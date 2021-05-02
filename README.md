# Grouped Checkbox

[![pub package](https://img.shields.io/badge/pub-v1.0.0-blue)](https://pub.dartlang.org/packages/grouped_checkbox)

A package to easily group checkboxes in different styles in Flutter projects.

<p>
    <img width="220px" src="https://raw.githubusercontent.com/zfnadia/grouped-checkbox/master/screenshots/one.jpg"/>
    <img width="220px" src="https://raw.githubusercontent.com/zfnadia/grouped-checkbox/master/screenshots/two.jpg"/>
    <img src="https://media.giphy.com/media/Y1do7LrbSxTOcQa5qF/giphy.gif"/>
</p>

## Usage
To use this plugin, add `grouped_checkbox` as a [dependency in your pubspec.yaml file](https://flutter.dev/platform-plugins/).

<br/>
since(02/may/2021) this package not migrated to null safe so use this

<div class="highlight highlight-source-yaml"><pre><span class="pl-ent">dependencies</span>:
  <span class="pl-ent">grouped_checkbox</span>:
    <span class="pl-ent">git</span>:
      <span class="pl-ent">url</span>: <span class="pl-s">git://github.com/lavahasif/grouped-checkbox.git</span>
      <span class="pl-ent">ref</span>: <span class="pl-s">hasif</span>


</pre></div>

```dart
dependencies: grouped_checkbox: 1.0.0
```

### Example

```dart
import 'package:grouped_checkbox/grouped_checkbox.dart';
```

```dart
    List<String> allItemList = [
        'Red',
        'Green',
        'Blue',
        'Yellow',
        'Black',
        'Violet',
      ];
    
    List<String> checkedItemList = ['Green', 'Yellow'];
      
    GroupedCheckbox(
      itemList: allItemList,
      checkedItemList: checkedItemList,
      disabled: ['Black'],
      onChanged: (itemList) {
        setState(() {
           selectedItemList = itemList;
           print('SELECTED ITEM LIST $itemList');
          });
      },
      orientation: CheckboxOrientation.VERTICAL,
      checkColor: Colors.blue,
      activeColor: Colors.red
    );
```
