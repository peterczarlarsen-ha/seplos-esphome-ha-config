Helpers are needed to make the sensor.bms0_delta_cell_voltage Etc

go to settings -> devices and services -> helpers (in the top menu)

add a template (sensor)

{{ (states('sensor.bms0_max_cell_voltage') | float(0) * 1000) - (states('sensor.bms0_min_cell_voltage') | float(0) * 1000)  }}

<img width="578" alt="Screenshot 2025-03-05 at 18 00 33" src="https://github.com/user-attachments/assets/00c56ecb-6de8-4045-8243-3099145ce0b5" />

make one for each battery, i have three, so i have three

<img width="2286" alt="Screenshot 2025-03-05 at 18 02 12" src="https://github.com/user-attachments/assets/183495a3-53c2-4bf3-ab83-ef948166bd87" />
