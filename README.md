# ArduinoProjects

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
