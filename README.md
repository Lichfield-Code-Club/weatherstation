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

## 🔄 Battery Swap Instructions

To maintain uninterrupted power for the Pimoroni weather board, swap the 12V LiFePO4 battery every 3 months (or as needed based on runtime measurements). This guide ensures safe, reproducible swaps inside the Stevensons container.

### 🧰 Required Items
- Fully charged 12V LiFePO4 battery (20Ah recommended)
- XT60 or Anderson Powerpole connectors
- 3A blade fuse (spare)
- Multimeter (optional, for voltage check)
- Insulated gloves (recommended)

### 🔌 Swap Procedure

1. **Prepare the replacement battery**
   - Confirm it's fully charged (≥13.2V for LiFePO4).
   - Inspect terminals and connectors for corrosion or damage.

2. **Power down the weather board**
   - If possible, wait for a sleep cycle or manually disable the board.
   - Disconnect the 5V line from the buck converter output.

3. **Disconnect the old battery**
   - Unplug the XT60 or Anderson connector.
   - Remove the fuse if inline.
   - Store the old battery in a safe, dry location for recharging.

4. **Install the new battery**
   - Connect the XT60 or Anderson plug securely.
   - Insert a fresh 3A fuse if needed.
   - Verify polarity: red to +Vin, black to –Vin on the buck converter.

5. **Restore power**
   - Reconnect the 5V line to the weather board.
   - Confirm LED or sensor activity during the next wake cycle.

6. **Log the swap**
   - Record the date, battery voltage, and any observations.
   - Update runtime estimates based on previous cycle duration.

### ⚠️ Safety Notes
- Never short the terminals or reverse polarity.
- Avoid swapping during rain or high humidity.
- Recharge removed batteries using a LiFePO4-compatible charger only.

*Figure: Battery swap ensures continuous operation with minimal downtime and traceable maintenance.*
