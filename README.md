# The Spaghettified Team has solved problem statements 1, 2 and 3 and also a bonus software for STAC Club

`Solutions to Stac Wars`
This github repo contains three folders, each being solutions to their respective problem statements.
Each folder contains a report that briefly explains all findings, work, calculations and analysis of the problems given.

# PS1 – OpenRocket:

Design a two-stage sounding rocket in OpenRocket for the fictional planet **Mustafar** that:


## What we built
A three-section, all-**cardboard** rocket (ogive nose cone):

Payload section: carries the 1 kg payload. No motor. Drogue at apogee, main parachute later.
Sustainer: upper-stage propulsion. AeroTech J415W, 5 fins. Drogue at apogee, main parachute later.
Booster: first-stage propulsion. Cesaroni 1195J295-16A, 3 fins. Drogue at apogee, main parachute later.

Liftoff mass is 4.309 kg including motors. All results are from OpenRocket **Simulation 6** (Mustafar, 10 m/s wind at 270°). The full design reasoning, results and Earth-vs-Mustafar comparison are in the report.

## folder contents
the ps1 folder contains the three files of flightdata, rocket.ork and a detailed report required as per rules
there is also a support folder that holds additional deliverables


## How to open and test it
1. Install **OpenRocket 24.12** (the version the file was saved with).
2. Install the **Planetary Environment plugin** (`.jar`): put it in the `Plugins` folder inside the OpenRocket folder in `%AppData%` (create `Plugins` if it doesn't exist), then restart OpenRocket. Without the plugin the file still opens, but you'll see a warning that the extension isn't found, and re-running would use Earth gravity.
3. Open `Spaghettified.ork`. Don't re-save it unless the plugin is installed.
4. Open **Simulation 6** → Edit → Simulation extensions → *Planetary Environment*. The custom planet is **Mustafar** (g = 6.5 m/s²). To re-add it, load `support/Mustafar.json`.
5. The launch conditions in Simulation 6 are 75 kPa, 700 K (426.85 °C) and wind 10 m/s at 270°.
6. Run the simulation and compare with `Spaghettified_FlightData.csv`. For the Earth comparison, change one environment setting at a time (gravity, then pressure and temperature, then wind) and re-run.


# PS 2 - Data Analysis:

Analysis of the Voyage-123 solar observation data.

# what we did 
The folder for problem statement 2 contains a detailed structure of files and programs for data analysis of solar radiation.

The `README_PS2.md` explains how to implement the codebase in the user's local system and run the programs for themselves using jupyter notebook. (in vscode)

An analysis report has been created that shows all findings, translations and thorough inspection of given data. All questions pertaining to the problem statement have been answered. To view, go to:

- `STACWARS_Spaghettified_ps2_report.pdf` 
- `PS2_Data_Analysis/Mission` for PART wise code implementation

## All(as in all) lines of code, report, slides and readme have been done by hand :} , except the README_PS2.md (ofcourse)



# PS 3 - Astronomy :

The folder corresponding to astronomy ps analyses the telescope brightness observations of three stars: STAC-1, STAC-2, and STAC-3 -- to identify possible exoplanets and determine which is the most promising candidate for further habitability studies.

 `Exoplanet_habitability_ps3_report.pdf` provides calculations and explantions for the following in IEEE format:

- Transit Detection: identify recurring dips in relative stellar brightness and estimate orbital periods.

- Planetary Radius: estimate planet sizes using transit depth and stellar radius.

- Orbital Distance: apply Kepler’s Third Law to calculate orbital distances in AU and kilometres.

- Habitability Comparison: Compare orbital distances with the simplified habitable-zone distances derived from stellar luminosities.


# Bonus idea

The idea for a software is included in the `bonus_software.txt` file in the root folder