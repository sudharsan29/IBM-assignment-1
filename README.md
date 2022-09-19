void setup()
{
  Serial.begin(9600);
  pinMode(7,INPUT);
  pinMode(8,OUTPUT);
  pinMode(13,OUTPUT);
  
}
void loop()
{
  int p=digitalRead(4);
  Serial.println(p);
  if(p)
  {
    digitalWrite(13,HIGH);
    Serial.println("motion detected");
  }
  delay(1000);
  double a=analogRead(A0);
  double t=(((a/1024)*5)-0.5)*100;
  
  Serial.println(t);
  if(t>20)
  {
  
  
  digitalWrite(8,HIGH);
    Serial.println("temperature greater than 24");
    
    
  delay(1000);
  }
}
