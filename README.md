//
//  ViewController.swift
//  Fizz Buzz
//
//  Created by Bishrut Bhattarai on 10/8/19.
//  Copyright © 2019 Bishrut Bhattarai. All rights reserved.
//



import UIKit

class ViewController: UIViewController {
    
var string1 = ""
var num = ""
var number = 0
    
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
 string1 = ""
 num = enterText.text ?? "1"
 number = Int(num) ?? 1
  for index in 1...number
  {
      if index % 3 == 0 && index % 5 == 0 && index % 7 == 0 {
       string1 += "FizzBuzzBang"
    } else if index % 3 == 0 && index % 5 == 0 {
       string1 += "FizzBuzz, "
    } else if index % 3 == 0 {
       string1 += ("Fizz, ")
    } else if index % 5 == 0 {
       string1 += ("Buzz, ")
    } else if index % 7 == 0 {
       string1 += ("Bang, ")
    } else {
       string1 += (String(index) + ", ")
   }
  }
   printText.text=string1
 }
}
 
