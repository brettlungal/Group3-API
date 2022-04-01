# Group3-API Description
# Manitoba Clinic Finder 

## Description
* Manitoba clinic finder is a API that helps Manitoba residents find clinics near them, based on their current needs. 

## Endpoints
* ### By Location
  `https://mbclinicfinder/api/clinic/location`

  Parameters: longitude and latitude of the area you want to find the clinic in.

* ### By Service
  `https://mbclinicfinder/api/clinic/service`

  Parameters: service type of the service you need (walk-in/ dental/ psychologist...).

* ### By Shots
  `https://mbclinicfinder/api/clinic/shots`

  Parameters: shots type of the shot/vaccination you need (flu shot/ COVID-19 vaccination/ MMR...).

## Description of Resources
    ```json
    {
        "clinics": [
            {
                "clinicName": "Winnipeg Dental",
                "clincAddress":"12 Dentist Way, Winnipeg, MB"
            },
            {
                "clinicName": "Downtown Clinic",
                "clinicAddress": "1 Downtown Ave, Winnipeg, MB"
            },
            {
                "clinicName": "The Best Dental Clinic",
                "clinicAddress":"500 Osbourne Ave, Winnipeg, MB"
            }
        ],
        "Status": "OK",
        "Code": 200
    }
    ```

## Sample Request with Sample Response
* ### Example By Location
    #### Request:
    `https://mbclinicfinder/api/clinic/location?lat=49.8944133&lng=-97.136550`

    #### Response:
    ```json
    {
        "clinics": [
            {
                "clinicName": "Health Sciences Center",
                "clincAddress":"820 Sherbrook St, Winnipeg, MB"
            },
            {
                "clinicName": "Downtown Clinic",
                "clinicAddress": "1 Downtown Ave, Winnipeg, MB"
            },
            {
                "clinicName": "The Winnipeg Clinic",
                "clinicAddress":"2 Winnipeg Rd, Winnipeg, MB"
            }
        ],
        "Status": "OK",
        "Code": 200
    }
    ```

* ### Example By Service
    #### Request:
    `https://mbclinicfinder/api/clinic/service?service=dental`

    #### Response:
    ```json
    {
        "clinics": [
            {
                "clinicName": "Winnipeg Dental",
                "clincAddress":"12 Dentist Way, Winnipeg, MB"
            },
            {
                "clinicName": "Downtown Clinic",
                "clinicAddress": "1 Downtown Ave, Winnipeg, MB"
            },
            {
                "clinicName": "The Best Dental Clinic",
                "clinicAddress":"500 Osbourne Ave, Winnipeg, MB"
            }
        ],
        "Status": "OK",
        "Code": 200
    }
    ```

* ### Example By Shots
    #### Request:
    `https://mbclinicfinder/api/clinic/shots?shot=MMR`

    #### Response:
    ```json
    {
        "clinics": [
            {
                "clinicName": "Vaccine Clinic",
                "clinicAddress": "404 Vaccination Ave, Winnipeg, MB"
            },
            {
                "clinicName": "Shot In Arm Clinic", 
                "clinicAddress":"12 St. Marys Rd, Winnipeg, MB"
            }
        ],
        "Status": "OK",
        "Code": 200
    }
    ```

