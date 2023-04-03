# optimal-keen-vent-control

## Introduction and acknowledgments.
Home Assistant and Node-Red automation system for Keen vents control. Ecobee thermostat is used.
This repository is not complete until further notice.

This repository is inspired, structured, and built upon the work of [Daniel M. Zimmerman](https://github.com/dmzimmerman/HomeAssistantKeenVentsEcobeeAutomation).
However, the changes to some operational concepts are great enough for this to not be a branch of the original repository.

## Why it's different.
While I originally used the [HomeAssistantKeenVentsEcobeeAutomation](https://github.com/dmzimmerman/HomeAssistantKeenVentsEcobeeAutomation) with minor modifications, over time some critical aspects of the operation were changed to better fit my needs, also significantly improve the functionality of the system. These changes make the system more flexible and work better in more situations.
### Advantages:
- #### Thresholds are no longer used.
I moved away from using the thresholds as they allow for the situtions, where multiple vents can be closed to a degree that results in a significant increase in airducts' pressure. This causes strain on the sysytem, which results in airleaks to uncondiitoned space as well as exessive noise in the sysytem and at the vents' exits.
The common beliefe is that no more than 40% of all of the vents in a forced air sysytem should be closed at any one time.[^1]













[^1]: I am not an HVAC professional, nor do I play one on TV.
