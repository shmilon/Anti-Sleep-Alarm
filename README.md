# Anti Sleep Alarm

## Components used / Material Required
* Eye blink sensor with Goggles
* Arduino Nano
* Vibration Sensor
* Buzzer
* SPST switch
* 9V Battery
* Mini USB Cable
* Wire

## Circuit Diagram of Anti-Sleep Alarm Project

![image](https://user-images.githubusercontent.com/36078194/195566451-7d142da1-6008-41a3-8507-b2595e1117f6.png)


## Final Assembled Face
 
![image](https://user-images.githubusercontent.com/36078194/195565898-6a4f58bb-9b5b-4f97-aefa-e3b17a5709ee.png)


## code
```
//Code of Anti Sleep Alarm Project

define SENSE A0 // for eye blink sensor output 
void setup()
{ 
  pinMode(SENSE, INPUT);
  pinMode(2, OUTPUT);
  pinMode(LED_BUILTIN, OUTPUT); // Pin number 13 of Arduino
}
void loop()
 { 
   if(digitalRead(SENSE))
   {
      digitalWrite(LED_BUILTIN, LOW);
      pinMode(2, LOW);
  }
  else 
  { 
    delay (2000); 
    if(digitalRead(SENSE)) 
    { 
      digitalWrite(LED_BUILTIN, LOW); 
      pinMode(2, LOW); } 
    else 
      digitalWrite(LED_BUILTIN, HIGH);
      pinMode(2, HIGH); 
    } 
}
```
