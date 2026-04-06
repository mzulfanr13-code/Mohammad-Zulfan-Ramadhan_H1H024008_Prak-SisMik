Program LED Bergantian (Kiri vs Kanan)
```
cpp
int timer = 200;

void setup() {
  for (int i = 2; i <= 7; i++) {
    pinMode(i, OUTPUT); // semua pin LED jadi output
  }
}

void loop() {

  // Nyalakan 3 LED kiri (2,3,4)
  digitalWrite(2, HIGH);
  digitalWrite(3, HIGH);
  digitalWrite(4, HIGH);

  // Matikan 3 LED kanan (5,6,7)
  digitalWrite(5, LOW);
  digitalWrite(6, LOW);
  digitalWrite(7, LOW);

  delay(timer);

  // Sekarang kebalikannya

  // Nyalakan 3 LED kanan
  digitalWrite(5, HIGH);
  digitalWrite(6, HIGH);
  digitalWrite(7, HIGH);

  // Matikan 3 LED kiri
  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);

  delay(timer);
}
```
Penjelasan:
LED dibagi jadi dua grup:
  -Kiri: pin 2–4
  -Kanan: pin 5–7
Program menyalakan kiri → lalu kanan → berulang terus
Efeknya seperti lampu bergantian
