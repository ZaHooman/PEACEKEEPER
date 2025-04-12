#include <DHT.h>

//Definitions
#define DHTPIN 2
#define DHTTYPE DHT11

#define TRIG_PIN 12
#define ECHO_PIN 11

#define BUZZER_PIN 4
#define RED_LED 7
#define BLUE_LED 8

DHT dht(DHTPIN, DHTTYPE);

float prevHumidity = -1;

//Setup
void setup() {
  pinMode(TRIG_PIN, OUTPUT);
  pinMode(ECHO_PIN, INPUT);

  pinMode(BUZZER_PIN, OUTPUT);
  pinMode(RED_LED, OUTPUT);
  pinMode(BLUE_LED, OUTPUT);

  dht.begin();
  Serial.begin(9600);
}

void loop() {
  //Sensors
  float humidity = dht.readHumidity();
  float temperature = dht.readTemperature();

  if (isnan(humidity) || isnan(temperature)) return;

  //Ultrasonic Sensor
  digitalWrite(TRIG_PIN, LOW);
  delayMicroseconds(2);
  digitalWrite(TRIG_PIN, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);

  long duration = pulseIn(ECHO_PIN, HIGH);
  float distance = duration * 0.034 / 2;

  //Humidity Checker
  if (prevHumidity >= 0 && (humidity - prevHumidity) >= 1.0) {
    digitalWrite(BLUE_LED, HIGH);
    tone(BUZZER_PIN, 500);
    delay(300);
    digitalWrite(BLUE_LED, LOW);
    noTone(BUZZER_PIN);
  }
  prevHumidity = humidity;

  //Distance
  if (distance <= 6.0) {
    tone(BUZZER_PIN, 1000);
    digitalWrite(RED_LED, HIGH);
  } else {
    noTone(BUZZER_PIN);
    digitalWrite(RED_LED, LOW);
  }

  //Plotting Output
  Serial.print(temperature);
  Serial.print(",");
  Serial.print(humidity);
  Serial.print(",");
  Serial.println(distance);

  delay(500);
}
