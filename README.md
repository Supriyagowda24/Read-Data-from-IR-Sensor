# 📌 Week 2 Assignment – IR Sensor with Arduino UNO

## 🎯 Objective
To interface an IR sensor with Arduino UNO and detect the presence of an object using digital input.

---

## 🧰 Components Required
- Arduino UNO  
- IR Sensor Module  
- Jumper Wires  
- USB Cable  
- Laptop (for Arduino IDE)  

---

## 🔌 Circuit Connections
- VCC → 5V (Arduino UNO) 
- GND → GND (Arduino UNO)  
- OUT → Digital Pin 2 (Arduino UNO)

---

## 💻 Arduino Code

```cpp
int sensorPin = 2;

void setup() {
  pinMode(sensorPin, INPUT);
  Serial.begin(9600);
}

void loop() {
  int sensorValue = digitalRead(sensorPin);

  if (sensorValue == 0) {
    Serial.println("Object Detected");
  } else {
    Serial.println("No Object");
  }

  delay(500);
}

```

## 📊 Working Principle
- The IR sensor emits infrared light.
- When an object comes in front, the light reflects back.
- The sensor detects this reflection and outputs a LOW signal (0).
- Arduino reads this signal and prints "Object Detected" in the Serial Monitor.
- If no object is present, it prints "No Object".

---

🖥️ Output
- Object Detected → when object is near.
- No Object → when no object is present.

---

✅ Result

Successfully interfaced IR sensor with Arduino UNO and detected object presence using digital input.
