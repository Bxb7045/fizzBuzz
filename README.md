//
//  ViewController.swift
//  Fizz Buzz
//
//  Created by Bishrut Bhattarai on 10/8/19.
//  Copyright © 2019 Bishrut Bhattarai. All rights reserved.
//



import UIKit

class ViewController: UIViewController {
    
var response = ""
var defaultValue = ""
var enteredText = 0
let error1 = "Please type a number."
let error2 = "Please input a number greater than 99."

    
@IBOutlet weak var enterText: UITextField!
    
@IBOutlet weak var printText: UILabel!
    
@IBAction func submitText(_ sender: Any) {
 fizzBuzz()
}
    
    
override func viewDidLoad() {
 super.viewDidLoad()
  fizzBuzz()
}
    
    
func fizzBuzz() {
 response = ""
 defaultValue = enterText.text ?? "1"
 enteredText = Int(defaultValue) ?? 1
    
  if enteredText == 1 {
   printText.text=error1
    }
  else if enteredText <= 99 {
    printText.text=error2
    }
    
  else {
  for index in 1...enteredText
    {
       if index % 3 == 0 && index % 5 == 0 &&  index % 7 == 0 {
         response += "FizzBuzzBang"
     } else if index % 3 == 0 && index % 5 ==   0 {
         response += "FizzBuzz, "
     } else if index % 3 == 0 {
         response += ("Fizz, ")
     } else if index % 5 == 0 {
         response += ("Buzz, ")
     } else if index % 7 == 0 {
         response += ("Bang, ")
     } else {
         response += (String(index) + ", ")
    }
   }
     printText.text=response
  }
 }
}
