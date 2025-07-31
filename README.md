# layout


import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(
  home: MyLayout(),
  debugShowCheckedModeBanner: false,
));

class MyLayout extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("Layout Demo")),
      body: Column(
        children: [
          Row(
            children: [
              Expanded(child: Container(height: 50, color: Colors.red)),
              SizedBox(width: 8),
              Expanded(child: Container(height: 50, color: Colors.green)),
              SizedBox(width: 8),
              Expanded(child: Container(height: 50, color: Colors.blue)),
            ],
          ),
          SizedBox(height: 16),
          Container(height: 50, color: Colors.orange),
          SizedBox(height: 16),
          Expanded(
            child: ListView(
              children: List.generate(
                3,
                (i) => Container(
                  height: 50,
                  margin: EdgeInsets.symmetric(vertical: 4, horizontal: 8),
                  color: Colors.grey[300],
                  child: Center(child: Text('Item ${i + 1}')),
                ),
              ),
            ),
          ),
        ],
      ),
    );
  }
}
