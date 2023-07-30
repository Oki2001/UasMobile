import 'package:flutter/material.dart';
import 'package:wisatamakassar/splashscreen.dart';
void main() {

  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Kode untuk menggambarkan tampilan widget di sini
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: SplashScreen(),
    );
  }
}
