# Prototype-2-to-Prototype-1-controls
feel free to commit sugestions

f10 and f11 to restart stop the script, so you can inject new one without close .exe
I capture the varible to check de player state with CheatEngine:
  0x0628A974  or  0x062FA974; // 0 floor / 1 air / 3 wall


This is the simplest thing I could come up with:

1️⃣ Swap of behavior between SHIFT → Space
When the character is in the air (gIsOnAir = 1)

2️⃣ Short SPACE → Medium SPACE (simulation of minimum press of 350ms)
The minimum jump is extended so Space already activates the jump

3️⃣ Double press of SHIFT (1000ms) → Short SPACE (DODGE / ROLL)
To recover the new DODGE mechanic in Prototype 2, I have opted for double SHIFT although I also thought about double direction key (AWSD):
If the player presses SHIFT twice in a row and is on the ground (gIsOnAir = 0), a short SPACE press is simulated


I believe the main problem is that instead of pressing the keys in a held manner,
the simulation presses the keys repeatedly very fast and generates:
	When I am in the air and press SHIFT it only works correctly on the first press.
	When I am on the ground and press space, sometimes it jumps a lot, other times little, and the second press acts like SHIFT sometimes.
