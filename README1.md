Program LED: Cepat → Sedang → Mati
```
cpp
const int ledPin = 6;     // Pin LED
int timeDelay = 100;      // Mulai dari cepat

void setup() {
  pinMode(ledPin, OUTPUT);  // Set pin sebagai output
}

void loop() {

  digitalWrite(ledPin, HIGH); // LED nyala
  delay(timeDelay);

  digitalWrite(ledPin, LOW);  // LED mati
  delay(timeDelay);

  // Jika masih cepat, perlambat jadi sedang
  if (timeDelay < 500) {
    timeDelay += 100;  // delay diperbesar → makin lambat
  } 
  else {
    // Jika sudah sedang → matikan LED permanen
    digitalWrite(ledPin, LOW);
    while(true); // berhenti di sini (tidak looping lagi)
  }
}
```

Penjelasan:
-Program dimulai dari LED berkedip cepat
-Delay bertambah → LED menjadi sedang
-Saat mencapai batas tertentu → LED berhenti (mati)
-Tidak ada reset ke awal seperti program sebelumnya
