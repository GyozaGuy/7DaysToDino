# 7DaysToDino
A mod for ARK: Survival Evolved

Wrote bits of code in javascript, because it's all I know at the moment <3

7 DAYS TO DINO CONCEPTS
=======================
=======================

KEY POINTS
==========
Level of dinosaurs depend on number of nights passed
Amount of dinosaurs depend on number of nights passed
Can only get stone buildings from Beacons
Players rewarded with beacons after each (or every 10? 5? 3?) wave(s)


WAVES
=====
Dimorphodon Swarm
Insect Infestation
Dilophosaur Wave
Raptor Assault
Compy Mob
Carbonenymus Combine
Anklyo Attack
Alpha Carno
Alpha Rex
Alpha Raptor Pack
Monkey Mayhem
Kong Karnage
Gorilla Geurillas
Broodmother Battle
Dragon (Doom, Damnation, Duel, D-Day, Destruction)
Araneo Armageddon
Mad Mammoth March
Sabertooth Survival (Sauna)
Meganeura Murder

EVENTS
======
Extreme Heat
Extreme Cold
Acid Rain


WAVE ALGORITHM
==============
Variables:
--------------------------------------
nights = Number of nights passed
waveType = What kind of dino wave or event is happening
dinoLevel = Level of the dinosaurs
amountDinos = How many dinosaurs

dinoLevel
--------------------------------------
dinoLevel = nights //Always equal to the number of nights passed, so it increases in difficulty at a linear rate
			But the amount of dinos makes it become an exponential difficulty growth

amountDinos
--------------------------------------
amountDinos = 0
	if (waveType = example) {
		amountDinos = parse.Int(1.5 * nights); //Amount will vary depending on the waveType
	}
	if (waveType = mammothMarch) {
		amountDinos = parse.Int(0.6 * nights); //Amount will vary depending on the waveType
	}
	if (waveType = compyMob) {
		amountDinos = parse.Int(2 * nights); //Amount will vary depending on the waveType
	}