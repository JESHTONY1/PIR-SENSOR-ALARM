const int pirPin = 2;     // PIR sensor output pin
const int buzzerPin = 3;  // Buzzer pin
const int ledPin = 4;     // LED pin

void setup() {
    pinMode(pirPin, INPUT);
    pinMode(buzzerPin, OUTPUT);
    pinMode(ledPin, OUTPUT);
}

void loop() {
    int motion = digitalRead(pirPin); // Read PIR sensor

    if (motion == HIGH) {  // If motion detected
        digitalWrite(buzzerPin, HIGH); // Turn buzzer on
        digitalWrite(ledPin, HIGH);    // Turn LED on
        delay(5000);                   // Keep alarm on for a second
    } else {
        digitalWrite(buzzerPin, LOW);  // Turn buzzer off
        digitalWrite(ledPin, LOW);     // Turn LED off
    }
}
