The-Phenakistoscope
===================

Code of Project 1 for Creation And Computation 



int ledGreen=13;
int ledRed=12;

int DCmotor=3;
int Fsensor=0;

int FsensorValue;
int Fsensormap;

void setup(){
Serial.begin(9600);


pinMode(ledGreen, OUTPUT);
pinMode(ledRed, OUTPUT);
pinMode(DCmotor, OUTPUT);
pinMode(Fsensor, INPUT);

}

void loop()
{
  FsensorValue = analogRead(Fsensor);



if (FsensorValue > 5) {
digitalWrite(ledGreen, HIGH);
digitalWrite(ledRed, LOW);
analogWrite(DCmotor, 18);

}

else {
digitalWrite(ledGreen, LOW);
digitalWrite(ledRed, HIGH);
analogWrite(DCmotor, 0);

}

}
  
  
  
