# 🚀 Smart GPS Tracker (Arduino Nano + ESP8266)

A **LoRa-based GPS Tracker** using **Arduino Nano (Transmitter)** and **NodeMCU (Receiver)**.  
This project sends GPS coordinates via LoRa and displays them in real time on the receiver side.

---

## 🧩 Hardware Setup

### **Transmitter End (Arduino Nano + LoRa + GPS)**

**Components:**
- Arduino Nano  
- LoRa Module (SX1278 / RA-02)  
- GPS Module (NEO-6M)  
- 3.3V Regulator  
- Li-ion Battery (3.7V)  
- Antennas  

**Wiring:**

| LoRa Pin | Arduino Nano Pin |
|-----------|------------------|
| VCC | 3.3V |
| GND | GND |
| MISO | D12 |
| MOSI | D11 |
| SCK | D13 |
| NSS | D10 |
| RST | D9 |
| DIO0 | D2 |

| GPS Pin | Arduino Nano Pin |
|----------|------------------|
| VCC | 3.3V |
| GND | GND |
| TX | D4 |
| RX | D3 |

---

### **Receiver End (NodeMCU + LoRa)**

**Components:**
- NodeMCU  
- LoRa Module (SX1278 / RA-02)  
- Antenna  

**Wiring:**

| LoRa Pin | NodeMCU Pin |
|-----------|--------------|
| VCC | 3.3V |
| GND | GND |
| MISO | D6 |
| MOSI | D7 |
| SCK | D5 |
| NSS | D8 |
| RST | D0 |
| DIO0 | D1 |

---

## ⚙️ Setup Steps

### **Step 1: Install Libraries**

Install the following libraries in **Arduino IDE**:
- `LoRa` by **Sandeep Mistry**  
- `TinyGPS++` by **Mikal Hart**

---

### **Step 2: Upload Transmitter Code**

1. Connect **Arduino Nano** via USB  
2. Upload the **transmitter sketch**  
3. Set matching **LoRa frequency** on both devices  
4. Disconnect Nano from USB after upload  

---

### **Step 3: Upload Receiver Code**

1. Connect **NodeMCU** via USB  
2. Upload the **receiver sketch**  
3. Keep NodeMCU connected for **Serial Monitor** monitoring  

---

### **Step 4: Power Up**

**Transmitter:**
- Connect battery to 3.3V regulator  
- Attach antennas  
- Power on the system  

**Receiver:**
- Keep NodeMCU connected via USB  

---

## 🔄 Operation

### **Transmitter Behavior**
- Red LED blinks when sending data  
- GPS LED indicates satellite fix status  
- Sends location every **30 seconds**

### **Receiver Behavior**
- Listens for LoRa packets  
- Displays received data in Serial Monitor  
- Blue LED blinks on activity  

---

## 🧰 Troubleshooting

**No Data:**
- Check LoRa frequency matches  
- Verify antenna connections  
- Ensure stable 3.3V power  

**GPS Issues:**
- Place transmitter outdoors  
- Wait 5–10 minutes for first fix  

**Connection Problems:**
- Check all wiring  
- Verify ground connections  
- Use stable power supply  

---

## ⚠️ Notes

- Use **3.3V** for all modules  
- Place antennas properly  
- Allow GPS time to acquire satellites  
- Follow **regional LoRa frequency regulations**

---

### ✅ System Ready

Your system is ready when:
- Both devices show active LEDs  
- Serial Monitors display data as expected  

---

📡 **Smart GPS Tracker — Powered by LoRa, Arduino Nano, and NodeMCU**