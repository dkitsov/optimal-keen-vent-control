# optimal-keen-vent-control

## Introduction and acknowledgments.
Home Assistant and Node-RED automation system for Keen vents control. Ecobee thermostat is used.
*This repository is not complete until further notice.*

This repository is inspired, structured, and built upon the work of [Daniel M. Zimmerman](https://github.com/dmzimmerman/HomeAssistantKeenVentsEcobeeAutomation).
However, the changes to some operational concepts are significant enough for this not to be a branch of the original repository.

## Why it's different.
While I initially used the [HomeAssistantKeenVentsEcobeeAutomation](https://github.com/dmzimmerman/HomeAssistantKeenVentsEcobeeAutomation) with minor modifications, over time, some critical aspects of the operation were changed to better fit my needs, also significantly improve the functionality of the system. These changes make the system more flexible and work better in more situations.
### Advantages:
- #### Thresholds are no longer used.\nI moved away from using the thresholds as they allow for situations where multiple vents can be closed to the degree that significantly increases air duct pressure. This causes strain on the system, resulting in air leaks to unconditioned space and excessive noise in the system and at the vents' exits.
The common belief is that no more than 40% of all vents in a forced air system should be closed at any time.[^1]
- #### Weighted mean average vent position is utilized.
This further lowers the chance of overpressure in the system.[^1] The function will always attempt to keep the weighted position of all the vents above 60.
- #### Vent positions changes are ranked.
Node-RED flow will make sure that the vents that get more opened are controlled first so that there is no unnecessary increase of pressure in the system.
- #### Operation of the vents is staggered so that there are no substantial changes to the airflow and no sudden changes to pressure, further increasing the system's stability and lowering the noise.












[^1]: I am not an HVAC professional, nor do I play one on TV.
