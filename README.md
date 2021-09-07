# MMM-TitanSchoolMealMenu

#### A module for the MagicMirror framework that retrieves a school meal menu from the Titan Schools API (family.titank12.com)

![Screenshot](./docs/screenshot.png)

## Usage

Add this to your MagicMirror `config.js`:

    {
        module: "MMM-TitanSchoolMealMenu",
        position: "top_left",
        header: "School Menu",
        config: {
            buildingId: '23125610-cbbc-eb11-a2cb-82fe13669c55',
            districtId: '93f76ff0-2eb7-eb11-a2c4-e816644282bd',
            numberOfDaysToDisplay: 3, // Default 3
        },
    },

## Finding your `buildingId` and `districtId`

#### 1. Go to the Titan Schools webpage and search for your school district: https://family.titank12.com/

![Search for your school district](./docs/step1.png)

#### 2. Enter your state (or refine with city and state)

![Use the search box to search by city/state](./docs/step2.png)

#### 3. Use your browser's developer tools to inspect a request to the `/FamilyMenu` endpoint. The `districtId` and `buildingId` will be present as query string parameters on these requests.

![Use developer tools to inspect a network request](./docs/step3.png)