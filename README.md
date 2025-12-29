This creates a REST service end point to control Ezcoo 4x2 HDMI matrix switch. 

Connect the switch USB UART to pi (/dev/ttyUSB0)
Install python venv
Checkout this code repo
Start service (uvicorn websocketservice:app --host 0.0.0.0 --port 8000)
For startup on boot, copy and modify scripts/ezmatrixserver.service to /etc/systemd/system, systemctl daemon-reload, systemctl enable ezmatrixserver.service, systemctl start ezmatrixserver.service
Deploy the ha-ez-matrix custom component to Home assistant and configure the URL to http://<your-pi-ipaddr>:8000
