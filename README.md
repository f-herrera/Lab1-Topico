# Lab1-Topico

//proyecto de semaforo realizado para una tarea de la catedra de Topico

const int buttonPin = 2;    
const int ledPinverde =  13;     
const int ledPinnaranjo =  12;
const int ledPinrojo =  8;
int buttonState = 0;        

void setup() {
  
  pinMode(ledPinverde, OUTPUT);
  pinMode(ledPinnaranjo, OUTPUT);
  pinMode(ledPinrojo, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  buttonState = digitalRead(buttonPin);
  if (buttonState == LOW){
   
    digitalWrite(ledPinverde, HIGH);
  }
  else { 
    delay(3000);
    digitalWrite(ledPinverde, LOW);
    
    digitalWrite(ledPinnaranjo, HIGH);
    delay(500);
    digitalWrite(ledPinnaranjo, LOW);
    
    digitalWrite(ledPinrojo, HIGH);
    delay(5000);
    digitalWrite(ledPinrojo, LOW);
  }
}
