# NMZ Automation Program

This program automates various tasks within the Nightmare Zone (NMZ) in Old School RuneScape (OSRS), such as managing absorption potions, prayer potions, and overloads. It also tracks round progress, monitors player stats, and performs actions based on in-game conditions.

---

## Features

### **Core Functionality**
- **Potion Management**:
  - Automatically drinks absorption potions to maintain points at 1000 or as high as possible.
  - Refills absorption points when they drop below 300.
  - Drinks overload potions when they expire.
  - Uses prayer potions when prayer points fall below a threshold.
- **Rock Cake Guzzling**:
  - Reduces hitpoints to 1 using a Dwarven rock cake.
- **Round Detection**:
  - Tracks the start and end of each NMZ round.
  - Handles potion consumption and status updates at the beginning of a round.
- **Customizable Selection**:
  - Allows toggling between overload/absorption focus and prayer potion focus.

### **Safety Features**
- Ensures no action is repeated unnecessarily.
- Includes configurable delays for smoother execution.
- Logs all critical actions for debugging and tracking.

---

## Configuration

### **Selection Modes**
Set the `selection` variable in the code to toggle between different modes:
- `0`: Focus on overloads and absorption potions.
- `1`: Focus on prayer potions.

### **Round Management**
- The program tracks rounds using the `ROUND_START` variable.
- At the start of each round, the program ensures absorption points are topped up to 1000.

### **Action Delays**
- Delays between actions are defined using the `sleepWithCatch(int millis)` method.
- Adjust these values as needed for smoother operation or to match your latency.

---

## Usage
1. Start a new NMZ instance and ensure the program is running.
2. The program will:
   - Interact with Dominic Onion to start a dream.
   - Walk to the appropriate locations for potion management and combat.
   - Automatically handle potions and status updates.

---

## Known Issues
- Ensure proper detection of game regions and varbits for consistent performance.
- Prayer potion withdrawal may need adjustment based on inventory space.

---

## Contributing
Contributions are welcome! If you find any bugs or have ideas for new features, feel free to submit an issue or pull request.

---

## License
This project is for educational purposes only and should not be used to violate Jagex’s terms of service. Use at your own risk.

