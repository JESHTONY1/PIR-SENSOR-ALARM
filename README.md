const int pirPin = 2;
const int buzzerPin = 3; 
const int ledPin = 4;

void setup() {
    pinMode(pirPin, INPUT);
    pinMode(buzzerPin, OUTPUT);
    pinMode(ledPin, OUTPUT);
}

void loop() {
    int motion = digitalRead(pirPin); 

    if (motion == HIGH) {  // If motion detected
        digitalWrite(buzzerPin, HIGH); 
        digitalWrite(ledPin, HIGH);
        delay(5000);
    } else {
        digitalWrite(buzzerPin, LOW);
        digitalWrite(ledPin, LOW);
    }
}
