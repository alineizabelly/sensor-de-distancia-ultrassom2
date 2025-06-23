// C++ code
//
#include <Servo.h>

int semsor = 0;

Servo servo_13;

void setup()
{
  pinMode(8, INPUT);
  servo_13.attach(13, 500, 2500);
}

void loop()
{
  semsor = digitalRead(8);
  if (semsor <= 30) {
    servo_13.write(90);
    delay(3000); // Wait for 3000 millisecond(s)
  }
  servo_13.write(0);
  delay(3000); // Wait for 3000 millisecond(s)
}
