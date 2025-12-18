# Storm-Breaker-Social-Engineering-Tool
A powerful phishing tool for security testing and penetration testing purposes. Storm Breaker captures device information, camera access, microphone access, and location data through social engineering.
FOR EDUCATIONAL AND AUTHORIZED TESTING PURPOSES ONLY
This tool is designed for security professionals and researchers to test system vulnerabilities with proper authorization. Unauthorized use of this tool is illegal and unethical. The developers assume no liability and are not responsible for any misuse or damage caused by this program.
Features

Camera Access: Captures photos from target device camera
Microphone Access: Records audio from target device
Location Tracking: Retrieves GPS coordinates and location data
Device Fingerprinting: Collects comprehensive device information

IP Address
Operating System
Browser Details
Screen Resolution
CPU Information
Time Zone
Language Settings


Ngrok Integration: Automatic public URL generation
Multiple Templates: Various phishing page templates
Real-time Monitoring: Live HTTP request logging

Prerequisites

Python 3.x
Kali Linux or any Debian-based Linux distribution
Ngrok account (free tier available)
Root/sudo access

Installation
1. Clone the Repository
bashgit clone https://github.com/yourusername/stormbreaker.git
cd stormbreaker
2. Install Dependencies
bashsudo apt-get update
sudo apt-get install python3 python3-pip
pip3 install -r requirements.txt
3. Setup Ngrok

Sign up for a free account at ngrok.com
Download and install ngrok
Authenticate your ngrok account:

bashngrok authtoken YOUR_AUTH_TOKEN

Usage
Starting Storm Breaker
bashcd Storm-Breaker
sudo python3 st.py
Workflow

Start the Application

Navigate to Desktop/Storm-Breaker directory
Run with sudo privileges


Configure Ngrok

The tool will automatically start ngrok on port 2525
A public URL will be generated


Choose Template

Available templates:

Camera access
Microphone access
Location tracker
Normal data collection
Weather app




Send Link to Target

Copy the generated ngrok URL
Send to target through social engineering methods


Monitor Results

View incoming HTTP requests in real-time
Check captured images in /images/ folder
Review device information in the web panel



Example Commands
bash# Navigate to project directory
cd Desktop/Storm-Breaker

# Run Storm Breaker
sudo python3 st.py

# In separate terminal - start ngrok manually
ngrok http 2525

Security Considerations

Always obtain written permission before testing
Only use on systems you own or have explicit authorization to test
Be aware of local laws and regulations
Keep ngrok URLs secure and don't share unnecessarily
Clear captured data after authorized testing

🔧 Troubleshooting
Ngrok Connection Issues
If you see "permission denied" errors:
bashsudo chmod +x /usr/local/bin/ngrok
Port Already in Use
bashsudo lsof -i :2525
sudo kill -9 PID
Python Dependencies
bashpip3 install --upgrade -r requirements.txt

Available Templates

Camera Template - Requests camera access and captures photos
Microphone Template - Requests microphone access for audio
Near You Template - GPS location tracking
Normal Data Template - Standard device information
Weather Template - Disguised as weather app

Legal Notice
This tool is provided for educational purposes only. Users are responsible for complying with all applicable laws. The developers are not liable for any illegal use of this software.
Remember:

Penetration testing without authorization is illegal
Always obtain proper consent
Document all testing activities
Respect privacy and data protection laws

License
This project is licensed under the MIT License - see the LICENSE file for details.
