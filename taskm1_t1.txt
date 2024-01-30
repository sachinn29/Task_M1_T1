#define pirPin 2
#define ledPin 3

void setup() {
  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {

  int pirState = digitalRead(pirPin);

  if(pirState == HIGH){
    digitalWrite(ledPin, HIGH);
    Serial.println("Motion detected! Turning on LED.");
  }
  else {
    digitalWrite(ledPin, LOW);
    Serial.println("No motion detected. Turning off LED.");
  }

  delay(1000);

}
