int potpin =15;//potentiometer pin
int ledPin = 2;
int ledValue = 15;
void 
setup() {
  Serial.begin(115200);
   
  pinMode(ledPin,OUTPUT);
}
void loop(){
  // PUT YOUR MAIN CODE HERE, TO RUN REPEATEDLY:
  int potValue = analogRead(potpin);
  // Read analog value (0-4095)

//Print VAlue
  Serial.println(potValue);

//Map the potentiometer value (0-4095) to LED brightness(0-255)
  int brightness = map(potValue, 0, 4095, 0, 255);

  analogWrite(ledPin,brightness);

  delay(200);
}





