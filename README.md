# Smart-GPS-Tracker-Aurdino-and-ESP8266-code

Arduino Nano (Transmitter) + NodeMCU (Receiver)

Hardware Connections

Transmitter End (Arduino Nano + LoRa + GPS)

Components:

· Arduino Nano
· LoRa Module (SX1278/RA-02)
· GPS Module (NEO-6M)
· 3.3V Regulator
· Li-ion Battery (3.7V)
· Antennas

Wiring:

· LoRa VCC → 3.3V
· LoRa GND → GND
· LoRa MISO → D12
· LoRa MOSI → D11
· LoRa SCK → D13
· LoRa NSS → D10
· LoRa RST → D9
· LoRa DIO0 → D2
· GPS VCC → 3.3V
· GPS GND → GND
· GPS TX → D4
· GPS RX → D3

Receiver End (NodeMCU + LoRa)

Components:

· NodeMCU
· LoRa Module (SX1278/RA-02)
· Antenna

Wiring:

· LoRa VCC → 3.3V
· LoRa GND → GND
· LoRa MISO → D6
· LoRa MOSI → D7
· LoRa SCK → D5
· LoRa NSS → D8
· LoRa RST → D0
· LoRa DIO0 → D1

Setup Steps

Step 1: Install Libraries

Install these in Arduino IDE:

· LoRa by Sandeep Mistry
· TinyGPS++ by Mikal Hart

Step 2: Upload Transmitter Code

1. Connect Arduino Nano via USB
2. Upload transmitter sketch
3. Set matching LoRa frequency on both devices
4. Disconnect from USB

Step 3: Upload Receiver Code

1. Connect NodeMCU via USB
2. Upload receiver sketch
3. Keep connected for monitoring

Step 4: Power Up

Transmitter:

· Connect battery to 3.3V regulator
· Attach antennas
· Power on

Receiver:

· Keep NodeMCU connected via USB

Operation

Transmitter Behavior:

· Red LED blinks when sending data
· GPS LED indicates satellite status
· Sends location every 30 seconds

Receiver Behavior:

· Listens for LoRa packets
· Displays received data in Serial Monitor
· Blue LED shows activity

Serial Monitor Output

Transmitter (115200 baud):

```
GPS Tracker Started
Searching for satellites...
GPS Fixed: 12.3456, 98.7654
Packet Sent
```

Receiver (115200 baud):

```
Receiver Ready
Waiting for packets...
Received: LAT:12.3456,LNG:98.7654
```

Troubleshooting

No Data:

· Check LoRa frequency matches
· Verify antenna connections
· Ensure 3.3V power

GPS Issues:

· Place transmitter outdoors
· Wait 5-10 minutes for first fix

Connection Problems:

· Check all wiring
· Verify ground connections
· Ensure stable power supply

Notes

· Use 3.3V for all modules
· Place antennas properly
· Allow GPS time to acquire satellites
· Check regional LoRa frequency regulations

System ready when both devices show active LEDs and serial output.