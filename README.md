import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final DateTime currentDate = DateTime.now();
    final String formattedDate = "${currentDate.day}/${currentDate.month}/${currentDate.year}";

    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.white,
        body: SingleChildScrollView(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.center,
            children: [
              SizedBox(height: 20),
              Text(
                "Today's Date",
                style: TextStyle(fontSize: 20),
              ),
              Text(
                formattedDate,
                style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold),
              ),
              SizedBox(height: 20),
              Text(
                "Steps",
                style: TextStyle(fontSize: 30, color: Colors.grey),
              ),
              Text(
                "2000 steps +",
                style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),
              ),
              Text(
                "1.7km [6 133 kcal]",
                style: TextStyle(fontSize: 20, color: Colors.grey),
              ),
              Text(
                "C20 min",
                style: TextStyle(fontSize: 20, color: Colors.grey),
              ),
              SizedBox(height: 20),
              Container(
                width: 200,
                height: 200,
                decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(100),
                  boxShadow: [
                    BoxShadow(
                      color: Colors.grey.withOpacity(0.5),
                      spreadRadius: 5,
                      blurRadius: 10,
                      offset: Offset(0, 3),
                    ),
                  ],
                ),
                child: Center(
                  child: Text(
                    "Current Day",
                    style: TextStyle(fontSize: 50, fontWeight: FontWeight.bold),
                  ),
                ),
              ),
              SizedBox(height: 20),
              Text(
                "Your Week",
                style: TextStyle(
                  fontSize: 40,
                  fontWeight: FontWeight.w100,
                ),
              ),
              Text(
                "This week, your steps amounted to 40,000 steps",
                style: TextStyle(fontSize: 20, color: Colors.grey),
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.center,
                children: [
                  Icon(
                    Icons.wb_sunny,
                    size: 30,
                    color: Colors.orange,
                  ),
                  Text(
                    "Sunny",
                    style: TextStyle(fontSize: 30, color: Colors.orange),
                  ),
                ],
              ),
              SizedBox(height: 20),
              Text(
                "Nutrition",
                style: TextStyle(
                  fontSize: 30,
                  fontStyle: FontStyle.italic,
                ),
              ),
              Text(
                "Today, try to drink a bit more water",
                style: TextStyle(fontSize: 20),
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.center,
                children: [
                  Icon(
                    Icons.lunch_dining,
                    size: 30,
                    color: Colors.grey,
                  ),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}
