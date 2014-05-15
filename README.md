int ledr=6;
int ledw=5;


void setup() {
  pinMode(ledr, OUTPUT);
  pinMode(ledw, OUTPUT);
}

void loop()
{
  int r = random(60,255);
  int r2 = random(120, 255);
  //red
  analogWrite(ledr, r);
  delay(50);
  //white
  analogWrite(ledw, r);
  delay(50);
}
