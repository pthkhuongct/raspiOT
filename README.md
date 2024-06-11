sudo rm -f /home/pi/start_venv.sh
sudo nano /home/pi/start_venv.sh
//add script
##script 
#!/bin/bash
source /home/pi/raspiOT/myenv/bin/activate
cd /home/pi/raspiOT
python server.py
##script 
sudo chown pi:pi /home/pi/start_venv.sh
chmod +x /home/pi/start_venv.sh
#Edit crontab-e
crontab -e
//add script
##script 
@reboot /home/pi/start_venv.sh
##script 
