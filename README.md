int PIR = 13;
int RELAY= 12;

void setup()
{
  pinMode(PIR, INPUT);
  pinMode(RELAY, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  int read = digitalRead(PIR);
  
  Serial.println(read);

  if (read == 1) {
    digitalWrite(RELAY, HIGH);
  }
  else {
    digitalWrite(RELAY, LOW);
  }
  
  delay(50);
}
