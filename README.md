# African horse sickness data  
[![DOI](https://zenodo.org/badge/295426173.svg)](https://zenodo.org/badge/latestdoi/295426173)  
Information pertaining to AHS outbreaks and control in South Africa.

## Outbreak case and herd level data for outbreaks in the AHS controlled area of South Africa 
*data_outbreaks_ca.csv* contains actual numeric data for outbreaks  
*references_data_outbreaks_ca.csv* are the relevant references for said data, doi's have been included where available  

## Movement data for analysis of 2019 movement patterns within South Africa  
*data_2019movements.csv* contains all movements associated with the AHS controlled area (CA) and Infected zone (IZ) where the origin of movement occurs in the IZ  
  * _mid_ refers to the unique identifier for that movement
  * _lmgid_ refers to the unique identifier of the local municipality that the movement occurred from
  * _dmgid_ refers to the unique identifier of the district municipality that the movement occurred from
  * _originholdingid_ refers to the unique identifier of the holding of origin that the movement occurred from
  * _destinationholdingid_ refers to the unique identifier of the holding of destination that the movement occurred to
  * _totalmoved_ refers to the total equids that moved with _movementspecies_ the species of equid associated with the movement
  * _movementtype_ relates to the type of movement that occurs, each relating to varying levels of risk of AHS introduction into the AHS CA
    * _standard_ movements are directly between the AHS IZ and the AHS CA
    * _soq_ movements are movements where horses stand at a stop-over quarantine facility in a low risk area for at least 14 days prior to an AHS PCR test and onward movement
    * _soq_zebra_ movements are specifically associated with zebra movements where control measures are in place to facilitate safe movement, including quarantine and testing
    * _vpsoq_ movements are _soq_ movements where the facility of quarantine is vector protected. These exist either in the AHS infected zone, in areas where for periods of the year direct movements are not posssible, or in the AHS CA (_vpsoq_ca_).
  
  * Generally movements are single entities with an origin and destination - sometimes however movements are a two step process where three holdings are part of the movement as a whole. In particular this relates to _vpsoq_ca_ where original holdings are known, PCR testing is performed prior to entry and exit. _soq_ movements are also three-holding type movements however data relating to the origin of these animals is not generally captured, although they will only use this process if the holding occurs in an area that is restricted from moving directly into the AHS CA.
  * In the case of _vpsoq_ca_ movements the full process including all three associated holdings is included in *data_2019movements.csv* 
  
  * All information regarding equine movements in South Africa can be obtained at [here](https://www.myhorse.org.za/ahsvpn/)
