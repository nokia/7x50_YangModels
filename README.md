# Nokia SR OS YANG models
 
## Overview
 
Nokia SR OS YANG models for configuration and management of SR OS based routers.
 
YANG models are provided per-platform although many of the devices utilize the same common models.
YANG models are provided for the following platforms:
 
- 7950/7750/7450/7710 SR
- 7750 MG/VMG
- 7705 SAR-Hm
- 7250 IXR
 
## Working with the repository
 
The repository is created in order to provide a flexible programmatic interface to assist with
network automation tasks.
 
### `master` branch
 
The `master` branch provides the YANG models for all releases per platform.  Cloning this branch will
provide the maximum output, however, it may be more extensive then required for your use case.
 
```
git clone https://github.com/nokia/7x50_YangModels
```
 
### Per-release branches
 
Each release is provided as a separate branch.  The majority of the platforms utilize a set of common YANG models
and these are represented as SROS_Major_Minor, for example `SROS_19.10`.  Where a platform specific YANG is required
that is different from the common SR OS models a platform specific branch will be supplied, for example `SAR-Hm_SROS_19.10`
(example only).
 
Each release is tagged with the full release revision as well, for example `SROS_19.10.R1`
 
To obtain the YANG modules for a specific release clone the following:
 
```
git clone -b SROS_19.10.R1 --single-branch https://github.com/nokia/7x50_YangModels
```
 
#### Obtaining the differences between releases
 
To compare between two different sets of YANG models using git, clone the `master` branch or a release specific branch
such as `SROS_19.10` and then execute the following:
 
```
git diff SROS_19.10.R1 SROS_19.10.R2
```
 
#### Obtaining a zipped file of the YANG models for a specific release
 
To obtain a compressed TAR file of the available YANG models for a specific release, clone the repository and then
execute the following:
 
```
git archive --format tar.gz SROS.19.10.R1 > Nokia_YANG_19.10.R1.tar.gz
```
 
## Documentation
 
Further documentation regarding Nokia SR OS YANG models can be found on the Nokia Online Support Portal or in the SR OS user
and reference guides.
