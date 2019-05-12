# Example

An example using responsive_text_field

## Code
```dart
import 'package:flutter/material.dart';
import 'package:responsive_text_field/responsive_text_field.dart';
void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: Scaffold(
        body: Home()
      )
    );
  }
}

class Home extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: ResponsiveTextField(
        availableWidth: MediaQuery.of(context).size.width-4,
        minLines: 1,
        maxLines: 5,
        decoration: InputDecoration(
          contentPadding: EdgeInsets.symmetric(vertical: 5,horizontal: 0),
          focusedBorder: OutlineInputBorder(
            borderSide: BorderSide(width: 2,color: Colors.red)
          ),
          border: OutlineInputBorder(
              borderSide: BorderSide(width: 2,color: Colors.red)
          )
        ),
        style: TextStyle(
          fontSize: 16
        ),
      ),
    );
  }
}
```