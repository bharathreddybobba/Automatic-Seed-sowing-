//sowing seeds 
#include <Servo.h> 
 
Servo myservo;                  
int pos = 0;  

void setup() 
{ 
 Serial.begin(9600);
  myservo.attach(9);
  myservo.write(pos);
  Serial.println("Press 1 for  cotton");
  Serial.println("Press 2 for  chilly");
  Serial.println("Press 3 for ground nuts ");
  Serial.println("Press 4 for green grams");
 
 
} 
 
void loop() 
{ 
  if (Serial.available())
   Serial.readBytes(myCol, a); 
  int input = Serial.read();

  switch (input)
  {
    case '1':
     for (pos = 180; pos >= 0; pos -= 1) 
      {                                 
       myservo.write(pos);                
      delay(15); 
      }

    case'2':
     for (pos = 180; pos >= 0; pos -= 1) 
      {                                 
       myservo.write(pos);                
      delay(5);
      }

     for (pos = 0; pos >= 180; pos -= 1) 
      {                                 
       myservo.write(pos);                
      delay(5);
      }
    case'3':
     for (pos = 180; pos >= 0; pos -= 1) 
      {                                 
       myservo.write(pos);                
      delay(20); 
       }  
    case'4':
     for (pos = 180; pos >= 0; pos -= 1) 
       {                                 
       myservo.write(pos);                
      delay(10);
       }
       for (pos = 180; pos >= 0; pos -= 1) 
       {                                 
       myservo.write(pos);                
      delay(10); 
       }
  }
  }
  
  /// for moving bot
  int IN1 = 2;
int IN2 = 3;
int IN3 = 4;
int IN4 = 5;

void setup()  
{  
      
pinMode(2,OUTPUT);  
pinMode(3,OUTPUT);
pinMode(4, OUTPUT);
pinMode(5, OUTPUT);
     
}  
void loop()  
{  
//Forward      
digitalWrite(2,HIGH);   
digitalWrite(3,LOW);
digitalWrite(4,LOW);  
digitalWrite(5,HIGH);
delay(10000);
//Right
digitalWrite(2,LOW); 
digitalWrite(3,HIGH);
digitalWrite(4,LOW);   
digitalWrite(5,HIGH);
delay(700);
//Forward
digitalWrite(2,HIGH);
digitalWrite(3,LOW);
digitalWrite(4,LOW);   
digitalWrite(5,HIGH);   
delay(700);
//RIGHT
digitalWrite(2,LOW);
digitalWrite(3,HIGH); 
digitalWrite(4,LOW);
digitalWrite(5,HIGH);
delay(700); 
//FORWARD
digitalWrite(2,HIGH); 
digitalWrite(3,LOW);
digitalWrite(4,LOW);   
digitalWrite(5,HIGH); 
delay(10000); 
//LEFT
digitalWrite(5,LOW); 
digitalWrite(4,HIGH);
digitalWrite(2,HIGH); 
digitalWrite(3,LOW);
delay(700);
//FORWARD  
digitalWrite(5,HIGH);
digitalWrite(4,LOW);
digitalWrite(2,HIGH); 
digitalWrite(3,LOW);  
delay(700);
//LEFT
digitalWrite(5,LOW);
digitalWrite(4,HIGH);
digitalWrite(2,HIGH); 
digitalWrite(3,LOW);  
delay(700);
}
