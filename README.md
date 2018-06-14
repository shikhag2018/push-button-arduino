# push-button-arduino
//led on when button is pressed high and off when again button is pressed
int x=0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
  pinMode(12,OUTPUT);
}

void loop()
{
 while(digitalRead(2)==HIGH) {
    x=~x+2;digitalWrite(13, x);
    digitalWrite(12,1-x);
   
   while(digitalRead(2)!=HIGH);
   }
delay(10); // Delay a little bit to improve simulation performance
}
  
  
