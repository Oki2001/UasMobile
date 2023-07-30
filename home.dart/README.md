import 'package:flutter/material.dart';
import 'package:wisatamakassar/benteng_somba_opu.dart';
import 'package:wisatamakassar/beranda.dart';
import 'package:wisatamakassar/header_drawer.dart';
import 'package:wisatamakassar/fort_rotterdam.dart';
import 'package:wisatamakassar/pantai_losari.dart';
import 'package:wisatamakassar/profil.dart';
import 'package:wisatamakassar/pulau_kayangan.dart';
import 'package:wisatamakassar/pulau_lae-lae.dart';
import 'package:wisatamakassar/samalona_island.dart';


class HomePage extends StatefulWidget {
  const HomePage({Key? key}) : super(key: key);

  @override
  _HomePageState createState() => _HomePageState();
}
// menambah gambar dan kolom

class _HomePageState extends State<HomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(//Widget yang menyediakan Kerangka Dasar
      appBar: AppBar(//AppBar: Digunakan sebagai batang navigasi di bagian atas aplikasi.
        backgroundColor: Colors.blue,//Mengatur Warna background
        title: const Text("Daftar Tempat..."),
      ),
      drawer: Drawer(//pengaturan tambahan
        child: SingleChildScrollView(//fitur
          child: Column(//Menambahkan kolom
            children: [
              const MyHeaderDrawer(),
              ListTile(
                leading: const Icon(Icons.home),//menambahkan ikon
                title: const Text("Beranda"),
                onTap: () {//navigasi ke halaman lain
                  Navigator.push(context,
                      MaterialPageRoute(builder: (context) => const beranda()));
                },
              ),
              ListTile(
                leading: const Icon(Icons.settings),
                title: const Text("Pengaturan"),
                onTap: () {
                  Navigator.pop(context);
                },
              ),
              ListTile(
                leading: const Icon(Icons.money),
                title: const Text("Berlangganan"),
                onTap: () {
                  Navigator.push(context,
                      MaterialPageRoute(builder: (context) => const beranda()));
                },
              ),
              ListTile(
                leading: const Icon(Icons.people),
                title: const Text("Profil"),
                onTap: () {
                  Navigator.push(context,
                      MaterialPageRoute(builder: (context) => const profil()));
                },
              ),
              ListTile(
                leading: const Icon(Icons.logout),
                title: const Text("Log Out"),
                onTap: () {
                  Navigator.pop(context);
                },
              ),
            ],
          ),
        ),
      ),
      body: GridView.count(
        padding: const EdgeInsets.all(25),
        crossAxisCount: 2,
        children: <Widget>[
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (context) => const Roterdam()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/rotherdam.jpg',
                      height: 50,
                    ),
                    Text("Fort Rotterdam", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(
                    context,
                    MaterialPageRoute(
                        builder: (context) => const PantaiLosari()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/PantaiLosari.jpg',
                      height: 50,
                    ),
                    Text("Pantai Losari", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (context) => const somba_opu()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/Benteng-Somba-Opu.jpg',
                      height: 50,
                    ),
                    Text("Benteng Somba Opu", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (context) => const samalona()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/PulauSamalona.jpg',
                      height: 50,
                    ),
                    Text("Pulau Samalona", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (context) => const kayangan()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/Pulaukayangan.jpg',
                      height: 50,
                    ),
                    Text("Pulau Kayangan", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
          Card(
            margin: const EdgeInsets.all(8),
            child: InkWell(
              onTap: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (context) => const lae()));
              },
              splashColor: Colors.blue,
              child: Center(
                child: Column(
                  mainAxisSize: MainAxisSize.min,
                  children: [
                    Image.asset(
                      'images/pulaulae-lae.jpeg',
                      height: 50,
                    ),
                    Text("Pulau lae lae", style: TextStyle(fontSize: 11.0)),
                  ],
                ),
              ),
            ),
          ),
        ],
      ),
    );
  }
}
