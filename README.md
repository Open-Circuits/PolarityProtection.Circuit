# PolarityProtection.Circuit
Using a Diode and double-throw Latching Relay to protect vulnerable electronics downstream from Reverse Polarity accidents. When the correct polarity input is applied? The Latching relay will bypass the diode for higher efficiency, saving power that would've been lost in the diode voltage drop. If reverse polarity: Latching Relay will switch to permanently Off. Diode is only used to switch on the correct circuit path, through the relay, after that it is not used and bypassed. Uses a Capacitor & NOR gateWhen circuit

# Safety feature: Power Off Reset - Capacitor & NOT Gate to Open Relay
Charges a capacitor when running, Always keeping it charged. Upon power loss or disconnect a NOT gate will sense this and activate a transistor dumping the capacitor to Open Relay, resetting it! This resets the state of the Relay to "Off" until next power up. Otherwise it would stay on and reverse polarity would go through.

# Automatic Relay Control line
Can also use a microcontroller to open relay for timed & scheduled power-up.

# Usage:
For ex: DC to DC Converters will burn out or have components explode if wired in reverse polarity.

# Alt: 2 Latching Relays
- 1 Double Throw in Parallell with Diode (bypass for efficiency)
- 1 Single Throw in Series with Diode (if wired in reverse: breaks the circuit Preventing any power from reaching the Diode )
