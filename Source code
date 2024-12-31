int LEDgas = 7;
int LEDtmp = 3;
int buzzer = 6;
int MQ2pin = A0;
int TMPpin = A2;
void setup() {
  pinMode(buzzer,OUTPUT);
  Serial.begin(9600);

}

void loop() {
  float gasValue,tmpValue;
  gasValue = analogRead(MQ2pin);
  tmpValue = analogRead(TMPpin);
  Serial.print(tmpValue);
  Serial.print("\n\n");
  Serial.print("\n\n");
  int g=0,t=0;
  if(gasValue >= 500)
  {
    g=1;
  }
  if(tmpValue >= 1000)
  {
    t=1;
  }
  if(g==1 && t==0){
    digitalWrite(LEDgas, HIGH);
    digitalWrite(LEDtmp, LOW);
    int i =0;
    for(i=0;i<2;i++)
    {
      tone(buzzer, 220, 100);
      delay(1000);
    }
  }
  else if(g==0 && t==1){
    digitalWrite(LEDgas, LOW);
    digitalWrite(LEDtmp, HIGH);
    int i =0;
    for(i=0;i<10;i++)
    {
      tone(buzzer, 220, 100);
      delay(500);
    }
  }
  else if(g==1 && t==1){
    digitalWrite(LEDgas, HIGH);
    digitalWrite(LEDtmp, HIGH);
    int i =0;
    for(i=0;i<20;i++)
    {
      tone(buzzer, 220, 100);
      delay(100);
    }
  }
  else{
    digitalWrite(LEDgas, LOW);
    digitalWrite(LEDtmp, LOW);
    noTone(buzzer);
  }
  delay(1000);
}
