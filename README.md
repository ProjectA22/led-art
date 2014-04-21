int led1
int led2
int led3
int led4
int led5
int led6
int led7
int led8
int sensorPin = A0;    //Microphone Sensor 'ANALOG' pin on Arduino
int aLED = 13;    

int sensorValue = 0;

void setup() {
  pinMode (led1, OUTPUT);
  pinMode (led2, OUTPUT);
  pinMode (led3, OUTPUT);
  pinMode (led4, OUTPUT);
  pinMode (led5, OUTPUT);
  pinMode (led6, OUTPUT);
  pinMode (led7, OUTPUT);
  pinMode (led8, OUTPUT);
  pinMode(aLED, OUTPUT);
  Serial.begin(9600);
}
void loop ( ){
  sensorValue = analogRead(sensorPin);    
 Serial.println(sensorValue);
 for (i=0; i<8; i++) {{
  digitalWrite(led1, HIGH);   
  delay(1000);    
  digitalWrite(led2, HIGH);   
  delay(1000);               
 digitalWrite(led3, HIGH);   
  delay(1000);               
  digitalWrite(led4, HIGH);     
  delay(1000);              
  digitalWrite(led5, HIGH);   
  delay(1000);               
  digitalWrite(led6, HIGH);    
  delay(1000);              
 digitalWrite(led7, HIGH);   
  delay(1000);               
  digitalWrite(led8, HIGH);   
  delay(1000);               
if (sensorValue<869){
    digitalWrite(aLED, HIGH);

    delay(20);  
} else {
    digitalWrite(aLED, LOW); 
