# ESPHome Smart Home Device Configurations

This repository contains a collection of ESPHome configuration files for various smart home devices, including album art displays, garage door controllers, environmental sensors, and more.

## 🏠 Project Overview

This project showcases a comprehensive smart home setup using ESPHome devices integrated with Home Assistant. The configurations range from entertainment displays to utility monitoring and home automation controls.

## 📱 Device Categories

### 🎵 **Album Art & Music Displays**
- **`album-art-*.yaml`** - Multiple room album art displays using ESP32 boards with various display technologies
  - `album-art-living-room.yaml` - ESP32-S3 with advanced display capabilities
  - `album-art-dining.yaml` - Dining room album art display
  - `album-art-workroom.yaml` - HUB75 LED matrix display (64x64) for workroom
  - `album-art--tiny.yaml` - Compact album art display variant

- **`song-display*.yaml`** - LED matrix displays showing current song information
  - `song-display.yaml` - MAX7219 LED matrix with ESP32-C3
  - `song-display-workroom.yaml` - Workroom-specific song display

### 🚗 **Garage Door Controllers**
- **`ratgdov25i-*.yaml`** - RATGDO (Garage Door Opener) controllers for multiple garage doors
  - `ratgdov25i-ee9aef.yaml` - Guest garage controller
  - `ratgdov25i-eec2bc.yaml` - Bike garage controller  
  - `ratgdov25i-eec597.yaml` - Two-car garage controller

### 🌡️ **Environmental Monitoring**
- **`pizza-oven-temperature.yaml`** - Temperature monitoring for outdoor pizza oven
- **`e-paper-weather-display.yaml`** - E-paper weather information display
- **`presence-sensor-test.yaml`** - Presence detection sensor testing

### 🎙️ **Voice & Communication**
- **`home-assistant-voice-090d6c.yaml`** - Home Assistant Voice PE integration

### 🏡 **Home Information Displays**
- **`home-display-panel.yaml`** - Central home information panel (excluded from public repo due to personal info)
- **`days-since-last-bird-death-display.yaml`** - Quirky personal project tracker

### 🧪 **Development & Testing**
- **`led-hub-matrix-test-1.yaml`** - LED matrix testing configuration
- **`esphome-web-c94256.yaml`** - Web-based ESPHome device
- **`test-s3mini.yaml`** - ESP32-S3 Mini testing configuration

## 🔧 Technical Features

### **Display Technologies**
- **HUB75 LED Matrices** - High-resolution RGB displays for album art
- **MAX7219 LED Matrices** - Scrolling text displays for song information
- **E-Paper Displays** - Low-power weather and information displays
- **OLED/LCD Displays** - Various small information displays

### **Microcontroller Platforms**
- **ESP32-S3** - High-performance boards with PSRAM for image processing
- **ESP32-S2** - Mid-range boards for display applications
- **ESP32-C3** - Compact, efficient boards for simple displays
- **ESP32 Classic** - Standard ESP32 boards for general applications

### **Smart Home Integration**
- **Home Assistant API** - Encrypted communication with Home Assistant
- **OTA Updates** - Over-the-air firmware updates
- **WiFi Connectivity** - All devices connect to home network
- **mDNS Discovery** - Automatic device discovery

## 📁 Project Structure

```
├── README.md                          # This file
├── secrets.yaml                       # WiFi credentials and API keys (gitignored)
├── .gitignore                         # Excludes sensitive files
├── fonts/                            # Font files for displays
│   ├── Roboto-*.ttf                  # Roboto font variants
│   └── pixelmix*.ttf                 # Pixel fonts for LED matrices
├── album-art-*.yaml                  # Album art display configurations
├── song-display*.yaml                # Song information displays
├── ratgdov25i-*.yaml                 # Garage door controllers
└── [other device configs]            # Various sensor and utility devices
```

## 🔐 Security & Privacy

- **Encrypted API Communication** - All devices use encrypted Home Assistant API
- **Secrets Management** - Sensitive information stored in `secrets.yaml` (not committed)
- **Personal Information** - Files with personal data are excluded via `.gitignore`
- **Network Security** - Devices operate on local network with proper authentication

## 🚀 Getting Started

### Prerequisites
- [ESPHome](https://esphome.io/) installed
- [Home Assistant](https://www.home-assistant.io/) instance
- ESP32/ESP8266 development boards
- Various displays and sensors (see individual configs)

### Setup
1. Clone this repository
2. Create your own `secrets.yaml` file with:
   ```yaml
   wifi_ssid: "YourWiFiNetwork"
   wifi_password: "YourWiFiPassword"
   # Add device-specific encryption keys
   ```
3. Modify device configurations for your specific hardware
4. Compile and upload using ESPHome CLI or dashboard

### Example Commands
```bash
# Compile a configuration
esphome compile album-art-workroom.yaml

# Upload firmware
esphome upload album-art-workroom.yaml

# View logs
esphome logs album-art-workroom.yaml
```

## 🎨 Notable Projects

### **Album Art Workroom Display**
A 64x64 HUB75 LED matrix displaying album artwork from Home Assistant media players. Features real-time image downloading, resizing, and display with brightness control.

### **RATGDO Garage Controllers** 
Multiple garage door controllers providing:
- Door open/close control
- Status monitoring
- Light control
- Security integration with Home Assistant

### **Song Display Matrix**
Scrolling LED matrix displays showing current song title, artist, and playback information from Home Assistant media players.

## 🤝 Contributing

This is a personal smart home configuration repository, but feel free to:
- Use configurations as inspiration for your own projects
- Report issues or suggest improvements
- Share your own ESPHome configurations

## 📄 License

This project is provided as-is for educational and personal use. Individual components may have their own licenses.

## 🔗 Related Projects

- [ESPHome](https://esphome.io/) - The platform powering all these devices
- [Home Assistant](https://www.home-assistant.io/) - Smart home automation platform
- [RATGDO](https://github.com/ratgdo/esphome-ratgdo) - Garage door opener integration

---

*Last updated: July 2025*
