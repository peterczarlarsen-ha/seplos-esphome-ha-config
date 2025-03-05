ESPhome config for a Seplos BMS v3 interface (to home assistant or standalone)

# batteries in HA, with delta and all stats
<img width="1615" alt="Screenshot 2025-03-05 at 17 40 36" src="https://github.com/user-attachments/assets/7cf51820-cd63-47bd-8b51-a9595e7d11d4" />

Helpers are needed to make the sensor.bms0_delta_cell_voltage Etc

Go to settings -> devices and services -> helpers (in the top menu)

add a template (sensor)

For bms0 you will need this:

<code>{{ (states('sensor.bms0_max_cell_voltage') | float(0) * 1000) - (states('sensor.bms0_min_cell_voltage') | float(0) * 1000)  }}</code>

It look like this
<img width="578" alt="Screenshot 2025-03-05 at 18 00 33" src="https://github.com/user-attachments/assets/00c56ecb-6de8-4045-8243-3099145ce0b5" />

make one for each battery, i have three, so i have three helpers
<img width="2286" alt="Screenshot 2025-03-05 at 18 02 12" src="https://github.com/user-attachments/assets/183495a3-53c2-4bf3-ab83-ef948166bd87" />



# Direct connection to ESP32
<img width="2492" alt="Screenshot 2025-03-05 at 09 52 57" src="https://github.com/user-attachments/assets/33895ab7-7132-48b9-81bb-f00979c1c68e" />
