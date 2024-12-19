# Single Button Garage Door Controller
An ESPHome program to make a single button garage door smart. All in YAML.

# Features
Individual controls for opening, closing and setting position!

### Wait, how does that work?
The door position is calculated based the provided close_time and open_time. That gives us the speed, and as the controller decides the duration, we can calculate the position accurately enough. (If it gets out of sync after downtime for example, the script exposes a button (available in Home Assistant or the like), that resets the door position to closed).

# Requirements
1. The single button default operation has to work like this:
    1. Open: button press closes the door
    2. Closed: button press opens the door
    3. Moving: button press stops the movement
    4. Intermediate (stopped while moving): button press moves the door in the **opposite** direction of which it was moving before being stopped
2. An ESPHome compatible microcomputer (with wifi)
3. A relay module

# Optional
1. Coming soon: Monitor hardwired garage door buttons (to keep the script in sync with manual input)
