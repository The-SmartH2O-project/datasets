 # Anonymized datasets of SmartH2O project   
 ## Overview
 This repository contains the anonymized datasets of water consumptions of __Tegna__ and __Valencia__ SmartH2O's users.
 Each dataset is stored in its named folder, and have the same file naming:
 
`anonymizer.zip`: the compressed archive of water consumptions and households features

Once decompressed, the archived files are `smarth2o_anonymized_households.csv` and `smarth2o_anonymized_consumptions.csv`

### smarth2o_anonymized_households.csv
It contains the features of the households' users.
Here's an extract :

| index | smart_meter_id | household_size | household_garden_area | household_pool_volume | household_pool | household_garden | residency_type | number_bathrooms | environmental_attitude           | irrigation_system | house_plants | balcony_plants | building_size | name            | efficiency | ecomode | timer | name.1                 | number |
|-------|----------------|----------------|-----------------------|-----------------------|----------------|------------------|----------------|------------------|----------------------------------|-------------------|--------------|----------------|---------------|-----------------|------------|---------|-------|------------------------|--------|
| 0     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | toilet                 | 2      |
| 1     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | sink                   | 3      |
| 2     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | bathtub                | 0      |
| 3     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | shower                 | 0      |
| 4     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | tub_shower             | 2      |
| 5     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | dishwasher_simple      | 1      |
| 6     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | washing_machine | A++        | 1       | 1     | washing_machine_simple | 1      |
| 7     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | toilet                 | 2      |
| 8     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | sink                   | 3      |
| 9     | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | bathtub                | 0      |
| 10    | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | shower                 | 0      |
| 11    | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | tub_shower             | 2      |
| 12    | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | dishwasher_simple      | 1      |
| 13    | 111            | 85,00          | 0,00                  | 0,00                  | 0              | 0                | Flat           | 2                | Medium environmental sensitivity | 0                 | 0            | 0              | \N            | dishwasher      | A++        | 1       | 1     | washing_machine_simple | 1      |

The columns meaning is:
1. `index` The number of the row in the csv file
1. `smart_meter_id` The smart meter's ID
1. `household_size` The size of the Household (in squared meters)
1. `household_garden_area` The size of the garden (in squared meters)
1. `household_pool_volume` The volume of the pool (in cubic meters)
1. `household_pool` The presence of the pool (boolean)
1. `household_garden` The presence of the garden (boolean)
1. `residency_type` The type of residency (Flat, House, Single Family, ...) 
1. `number_bathrooms` The number of bathrooms
1. `environmental_attitude` The environmental attitude sensitivity of the user (High, Medium, Low)
1. `irrigation_system` The presence of an irrigation system (boolean)
1. `house_plants` The presence of house plants (boolean)
1. `balcony_plants` The presence of balcony plants (boolean)
1. `building_size` The size of the building (in squared meters)
1. `name` The name of a complex device (washing mascine, dishwater, ...)
1. `efficiency` The nefficiency of the complex device ( A, A+. A++, ...)
1. `ecomode` The presence of the Eco-Mode feature in the complex device (boolean)
1. `timer` The presence of the timer in the complex device (boolean)
1. `name.1` The name of a simple device (toilet, sink, bathtub, ...)
1. `number` The number of the simple device 

For all columns, a `NULL` value means that the user doesn't provided the information.
### smarth2o_anonymized_consumptions.csv
It contains the periodic readings of the smart meters.
Here's an extract :
| index | smart_meter_id | tst                 | meter_reading |
|-------|----------------|---------------------|---------------|
| 17    | 210            | 2015-05-20 09:15:00 | 178,297       |
| 18    | 210            | 2015-05-21 09:15:00 | 178,372       |
| 19    | 210            | 2015-05-22 09:15:00 | 178,622       |
| 20    | 210            | 2015-05-23 09:15:00 | 178,705       |
| 21    | 210            | 2015-05-24 09:15:00 | 178,826       |
| 22    | 210            | 2015-05-25 09:15:00 | 179,108       |
| 23    | 210            | 2015-05-26 09:15:00 | 179,108       |
| 24    | 210            | 2015-05-27 09:15:00 | 179,117       |
| 25    | 210            | 2015-05-28 09:15:00 | 179,324       |
| 26    | 210            | 2015-05-29 09:15:00 | 179,562       |
| 27    | 210            | 2015-05-30 09:15:00 | 179,579       |

The columns meaning is:
1. `index`  The number of the row in the csv file
1. `smart_meter_id` The smart meter's ID
1. `tst` The timestamp of the reading
1. `meter_reading` The value read

The difference of the reading values between two consecutive rows gives the water __consumption__.

## Security
In order to certificate the autenticity of the datasets, we provide these additional files:

- `anonymizer.zip.asc`: the `anonymizer.zip` signature made by the SmartH2O [OpenPGP](http://openpgp.org/) key
- `sha256sum.txt`: the _sha256 hash_ generated for `anonymizer.zip`
- `sha256sum.txt.asc`: the `sha256sum.txt` signature made by the SmartH2O [OpenPGP](http://openpgp.org/) key 


The SmartH2O key, [available here](https://pgp.mit.edu/pks/lookup?op=vindex&search=0x9739174C8B57ACA9), has this fingerprint: `7F14 4F03 BCB9 9A3C D99D 7483 9739 174C 8B57 ACA9`

## Contacts
For any type of further questions write to `smarth2o@idsia.ch'. 
The maintainer of this dataset is Corrado Valeri (`corrado.valeri@supsi.ch`).