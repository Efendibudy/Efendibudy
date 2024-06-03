- 👋 Hi, I’m @Efendibudy
- 
// Definisikan pin yang digunakan
const int sensorPin = A0; // Gunakan pin analog A0

void setup() {
  // Mulai komunikasi serial dengan kecepatan 9600 baud
  Serial.begin(9600);
}

void loop() {
  // Baca nilai analog dari pin sensor
  int sensorValue = analogRead(sensorPin);

  // Konversi nilai analog menjadi tegangan (dalam volt)
  float voltage = sensorValue * (5.0 / 1023.0);

  // Tampilkan tegangan ke serial monitor
  Serial.print("Tegangan: ");
  Serial.print(voltage);
  Serial.println(" volt");

  // Tunggu sejenak sebelum membaca lagi
  delay(1000);
}
