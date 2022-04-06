# Flutter-login_page
Flutter login_page code of android

import 'package:catalog_app/utils/routs.dart';

import 'package:flutter/material.dart';

class LoginPage extends StatelessWidget {

  const LoginPage({Key? key}) : super(key: key);
  

  @override
  
  Widget build(BuildContext context) {
  
    return Material(
    
        color: Colors.white,
        
        child: SingleChildScrollView(
        
          child: Column(
          
            children: [
            
              Image.asset(
              
                "assets/images/journal.png",
                
                fit: BoxFit.cover,
                
              ),
              
              const SizedBox(
              
                height: 20,
                
              ),
              
              const Text(
              
                "Admin",
                
                style: TextStyle(
                
                  fontSize: 22,
                  
                  fontWeight: FontWeight.bold,
                  
                ),
                
              ),
              
              const SizedBox(
              
                height: 20,
                
              ),
              
              Padding(
              
                padding: const EdgeInsets.symmetric(
                
                    vertical: 16.0, horizontal: 20.0),
                    
                child: Column(
                
                  children: [
                  
                    TextFormField(
                    
                      autofocus: true,
                      
                      decoration: const InputDecoration(
                      
                        border: OutlineInputBorder(),
                        
                        hintText: "Enter username",
                        
                        labelText: "Username",
                        
                        prefixIcon: Icon(
                        
                          Icons.email,
                          
                        ),
                        
                      ),
                      
                    ),
                    
                    const SizedBox(
                    
                      height: 15.0,
                      
                    ),
                    
                    TextFormField(
                    
                      autofocus: true,
                      
                      obscureText: true,
                      
                      decoration: const InputDecoration(
                      
                          border: OutlineInputBorder(),
                          
                          hintText: "Enter password",
                          
                          labelText: "Password",
                          
                          prefixIcon: Icon(
                          
                            Icons.lock,
                            
                          )),
                          
                    ),
                    
                    const SizedBox(
                    
                      height: 30.0,
                      
                    ),
                    
                    const Text(
                    
                      "Forgot Password?",
                      
                    ),
                    
                    const SizedBox(
                    
                      height: 30.0,
                      
                    ),
                    
                    ElevatedButton(
                    
                      onPressed: () {
                      
                        Navigator.pushNamed(context, MyRoutes.homeRoute);
                        
                      },
                      
                      
                      style: TextButton.styleFrom(
                      
                          minimumSize: const Size(100, 45)),
                          
                      child: const Text("Login"),
                      
                    ),
                    
                  ],
                  
                ),
                
              )
              
            ],
            
        ));
        
  }
  
}
