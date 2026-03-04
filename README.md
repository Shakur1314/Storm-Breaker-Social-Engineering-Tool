# Storm-Breaker-Social-Engineering-Tool

![Banner](images/stormbreaker-banner.jpg.jpeg)

A powerful phishing tool for security testing and penetration testing purposes. Storm Breaker captures device information, camera access, microphone access, and location data through social engineering.

> **FOR EDUCATIONAL AND AUTHORIZED TESTING PURPOSES ONLY**
> Unauthorized use of this tool is illegal. The developers assume no liability for misuse.

---

## Technical Workflow

### Step 1: Initialization
Navigate to the project directory and launch the tool with root privileges to initialize the local server.

```bash
sudo python3 st.py
```

![Terminal Start](images/Terminal-start.jpg.jpeg)

### Step 2: Tunneling with Ngrok
To reach targets outside your local network, start an ngrok tunnel on port 2525.

```bash
ngrok http 2525
```

![Ngrok Setup](images/ngrok-setup.jpg.jpeg)

### Step 3: Template Selection
Access the web panel to select a phishing template. Each template is designed for a specific data-gathering objective.

![Control Panel Desktop](images/control-panel-desktop.jpg.jpeg)
![Control Panel Mobile](images/control-panel-mobile.jpg.png)

### Step 4: Target Interaction
The target receives a permission request. Once they click "Allow," the listener gains access to the hardware.

![Target Permission Request](images/target-permission-request.jpg.png)

### Step 5: Data Capture & Logging
- Monitor the incoming server logs for real-time HTTP requests.
- Review the exfiltrated device information and captured media files in the panel.

![Server Logs](images/server-logs.jpg.jpeg)
![Captured Device Data](images/captured-device-data.jpg.jpeg)
![Image Saved Notification](images/image-saved-notif.jpg.jpeg)

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/stormbreaker.git
cd stormbreaker
```

### 2. Install Dependencies

```bash
sudo apt-get update
sudo apt-get install python3 python3-pip
pip3 install -r requirements.txt
```

---

## Available Templates
- **Camera:** Captures photos from the target device.
- **Microphone:** Records audio from the target device.
- **Near You:** GPS location tracking.
- **Weather:** Standard data collection disguised as a weather app.

---

## Troubleshooting
- **Permission Denied (Ngrok):** `sudo chmod +x /usr/local/bin/ngrok`
- **Port 2525 in Use:** `sudo kill -9 $(sudo lsof -t -i:2525)`
