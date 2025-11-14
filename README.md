# weatherstation
Capture weather data and send to an mqtt broker
## 🔋 Off-Grid Power Setup for Pimoroni Weather Board

This schematic shows how to power a Pimoroni weather board from a 12V LiFePO4 battery housed inside a Stevensons container. The board wakes every 5 minutes, so the system includes a buck converter to drop voltage to 5V and a fuse for protection.

![Power schematic for Pimoroni weather board](images/weatherstation-schematic.png)

**Components:**
- 12V LiFePO4 battery (20Ah recommended for 3-month runtime)
- XT60 connector or Anderson Powerpole for modular swaps
- 3A blade fuse on the 12V line
- DC-DC buck converter (12V → 5V, rated ≥3A)
- 220µF electrolytic + 0.1µF ceramic capacitor on 5V output
- Pimoroni weather board (with deep sleep enabled)

**Installation Notes:**
- Mount all components inside a weatherproof box within the container
- Use strain relief and sealed connectors to prevent corrosion
- Add a voltmeter or low-voltage cutoff to protect the battery
- Optional: log current draw with INA219 or USB meter to refine runtime estimates

*Figure: Schematic showing battery, fuse, buck converter, and weather board wiring.*
