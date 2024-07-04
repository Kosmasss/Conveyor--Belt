// Define the motor control pins
const int ENA = 5;  // PWM pin for Motor A
const int IN1 = 8;  // Control pin 1 for Motor A
const int IN2 = 9;  // Control pin 2 for Motor A

const int ENB = 6;  // PWM pin for Motor B
const int IN3 = 10; // Control pin 1 for Motor B
const int IN4 = 11; // Control pin 2 for Motor B

const int POT_PIN = A0;  // Analog pin for potentiometer

void setup() {
  // Set all the motor control pins to outputs
  pinMode(ENA, OUTPUT);
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);

  pinMode(ENB, OUTPUT);
  pinMode(IN3, OUTPUT);
  pinMode(IN4, OUTPUT);

  // Set initial direction for motors
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);
}

void loop() {
  // Read the potentiometer value
  int potValue = analogRead(POT_PIN);

  // Map the potentiometer value to a PWM value (0-255)
  int speed = map(potValue, 0, 1023, 0, 255);

  // Control Motor A speed
  analogWrite(ENA, speed);

  // Control Motor B speed
  analogWrite(ENB, speed);

  // Add a small delay to stabilize the reading
  delay(10);
}
