# African horse sickness data  
[![DOI](https://zenodo.org/badge/295426173.svg)](https://zenodo.org/badge/latestdoi/295426173)  
Information pertaining to AHS outbreaks and control in South Africa.

## Outbreak case and herd level data for outbreaks in the AHS controlled area of South Africa 
*data_outbreaks_ca.csv* contains actual numeric data for outbreaks  
*references_data_outbreaks_ca.csv* are the relevant references for said data, doi's have been included where available  

## Movement data for analysis of 2019 movement patterns within South Africa  
*data_2019movements.csv* contains all movements associated with the AHS controlled area (CA) and Infected zone (IZ) where the origin of movement occurs in the IZ and for the 2019 calendar year. 
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

# AHS case data for 2019 based on the ECOD disease reporting system in South Africa
*data_2019cases_ecod.csv* contains monthly aggregated case totals from 2019 for AHS cases as reported on the Equien Cause of Disease (ECOD) system which is a private veterinary association reporting system. Data is primarily based on laboratory reports and a review of the AHS case reporting for 2019 can be found [here](http://jdata.co.za/myhorse/documents/infographics/Reports/2019%20General%20AHS%20surveillance%20and%20testing%20report.pdf), while the ECOD system is available through the disease reporting links on the SAEVA [website](www.saeva.co.za).  
The dataset includes the unique identifiers for the local municiaplity (_lmgid_) and district municipality ( _dmgid_) within which the cases occurred which will assist in linking up this dataset with the *data_2019movements.csv* and spatial datasets. 

# Associated spatial data  
Associated spatial data relating to this repository is stored in the _/gis_ folder. Unless otherwise indicated all files are shapefiles with a CRS of 4326.  
  * _distrmun_ District municipalities of South Africa. Equine census data is aggregated to this level
  * _lm_ Local municipalities (2011) of South Africa. Movements and AHS case data are aggregated at this level. Where census data is required we recommend aggregating both case and movement data up to the district municipality level.
