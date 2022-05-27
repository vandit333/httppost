import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;
import 'package:http/http.dart';

void main() {
  runApp(MaterialApp(home: httppost(),));
}

class httppost extends StatefulWidget {
  const httppost({Key? key}) : super(key: key);

  @override
  State<httppost> createState() => _httppostState();
}

class _httppostState extends State<httppost> {

  TextEditingController email=TextEditingController();
  TextEditingController password=TextEditingController();
  void login(String email,String password)async
  {
    try{
      Response response=await post(
        Uri.parse("https://reqres.in/api/register"),
        body: {
          "email": email,
          "password": password,
        }
      );
      if(response.statusCode==200)
        {
          print("response");
        }
      else{
        print("fall");
      }
      
    }catch(e)
    {
      print(e.toString());
    }
  }


  @override
  Widget build(BuildContext context) {
    return Scaffold(appBar: AppBar(),

    body: Padding(
      padding: const EdgeInsets.all(20),
      child: Column(
        children: [
          TextField(controller: email,
            decoration: InputDecoration(
              hintText: "email"
            ),
          ),
          Container(height: 30,),
          TextField(controller: password,
          decoration: InputDecoration(
            hintText: "password"
          ),
          ),
          SizedBox(height: 30,),
          InkWell(
            onTap: () {
              login(email.text.toString(),password.text.toString());
            },
            child: Container(
              color: Colors.blueGrey,
              height: 50,
              child: Center(child: Text("sing up"),),
            ),
          )
        ],
      ),
    ),
    );
  }
}
