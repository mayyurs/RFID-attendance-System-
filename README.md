# RFID-attendance-System-
This project implements an RFID-based attendance system using NodeMCU ESP8266, MFRC522 RFID module, and a 5V buzzer. The system allows users to tap RFID cards to record attendance, which is then sent to a Google Sheet along with the corresponding time and date.

Components Used
NodeMCU ESP8266 development board
MFRC522 RFID module
RFID cards or tags
5V buzzer
Jumper wires
Breadboard (optional)
Setup and Configuration
Connect the components as follows:

NodeMCU ESP8266:

Connect the VCC pin to 3.3V power.
Connect the GND pin to the ground.
Connect the D1 pin to the SDA (Serial Data) pin of the MFRC522 module.
Connect the D2 pin to the SCK (Serial Clock) pin of the MFRC522 module.
Connect the D3 pin to the MOSI (Master Out Slave In) pin of the MFRC522 module.
Connect the D4 pin to the MISO (Master In Slave Out) pin of the MFRC522 module.
Connect the D5 pin to the RST (Reset) pin of the MFRC522 module.
MFRC522 RFID module:

Connect the VCC pin to 3.3V power.
Connect the GND pin to the ground.
Connect the SDA pin to the D1 pin of the NodeMCU ESP8266.
Connect the SCK pin to the D2 pin of the NodeMCU ESP8266.
Connect the MOSI pin to the D3 pin of the NodeMCU ESP8266.
Connect the MISO pin to the D4 pin of the NodeMCU ESP8266.
Connect the RST pin to the D5 pin of the NodeMCU ESP8266.
Buzzer:

Connect the positive (red) wire of the buzzer to a digital pin (e.g., D6) of the NodeMCU ESP8266.
Connect the negative (black) wire of the buzzer to the ground.
Install the required libraries:

MFRC522 library: Install the library from the Arduino Library Manager.
ESP8266WiFi library: Install the library from the Arduino Library Manager.
Adafruit MQTT library: Install the library from the Arduino Library Manager.
Open the "data to sheet.ino" sketch in the Arduino IDE.

Configure the Wi-Fi settings:

Replace <YOUR_SSID> with your Wi-Fi network name (SSID).
Replace <YOUR_PASSWORD> with your Wi-Fi network password.
Configure the Google Sheet settings:

Replace <YOUR_GSHEET_SCRIPT_URL> with the URL of the Google Sheet script that records attendance data.
Modify the script according to your requirements.
Upload the sketch to the NodeMCU ESP8266 board.

Ensure that the Google Sheet script is properly set up to receive and process the data sent from the NodeMCU ESP8266.

Power up the system and test it by tapping an RFID card/tag on the MFRC522 module. The buzzer will sound, indicating a successful attendance record.
