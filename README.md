# Project Setup

- Install virtualenv_wrapper
- $ mkvirtualenv -p /usr/bin/python3 canphone
- $ workon canphone
- $ pip install -r requirements.txt
- $ pip install -r requirements-dev.txt

# Required packages
```
apt install baresip
apt install mosquitto 
apt install libasound2-dev
apt install rpi.gpio

```

# Eventphone extension
- Create account at eventphone.de
- Create extension there

# Configuration
- Put asoundrc to /home/pi/.asoundrc (use mpv to play an audio file to get alsa recognize the preamp, if it does not work - preamp has to be shown in alsamixer) 
- Copy baresipconf folder to ~/.baresip
- Alter files accounts to match your extension credentials
- Adjust contacts file to match other canphone
- Change /usr/share/alsa/alsa.conf
  - set defaults.ctl.card 1 
  - set defaults.pcm.card 1 
- Add bind_address localhost in /etc/mosquitto/mosquitto.conf to bind broker to pi only

# SystemD services
- Copy and enable service files under systemd_service_files



clone the git at github: sake/canphone

then cd into the the directory and do: 
 $ pip3 install -r requirements.txt
 $ pip3 install -r requirements-dev.txt


