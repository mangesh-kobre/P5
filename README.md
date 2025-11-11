# P5
const int motorPin = 9;  // Motor connected via transistor to PWM pin D9 
void setup() { 
pinMode(motorPin, OUTPUT);   // Set motorPin as output 
} 
void loop() { 
// Gradually increase motor speed from 0 to 255 
for (int speed = 0; speed <= 255; speed++) { 
analogWrite(motorPin, speed);  // Write PWM signal 
delay(20);                    
}
delay(1000);  // Keep motor at full speed for a while 
// Gradually decrease motor speed from 255 to 0 
for (int speed = 255; speed >= 0; speed--) { 
analogWrite(motorPin, speed); 
delay(20); 
} 
delay(1000);  // Wait before restarting loop 
}
