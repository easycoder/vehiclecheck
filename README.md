# Vehicle Check

This is a mobile-oriented web app, designed to record the regular checks made on fleet vehicles. It can handle a fleet of any size. The app URL is [https://vehiclecheck.netlify.app](https://vehiclecheck.netlify.app) and the app contains its own user manual, accessed from the _"i"_ icon on the home screen.

The items to be checked, along with default values where appropriate, are held in `resources/json/refdata.json` and act as the defaults for all the vehicles in the fleet.

In the current version, data collected is placed in local storage and emailed on request to an address given by the user. It is feasible to replace this with a REST mechanism that uses a designated server; the changes required are fairly minor.

The app is written using EasyCoder and comprises 7 scripts. The primary script is `resources/ecs/vehicles.txt`, which calls the others as they are needed. The code is designed to be easy to write, easy to read and easy to maintain. No build tools are required as the scripts are run directly by the EasyCoder compiler, which is loaded from the GitHub CDN.
