# YNAB Property Value tracker

## How it works
Uses the rentcast.io api to get approximate value of real estate. Updates the asset in YNAB. 


## Setup

1. Get [Rentcast.io api key](https://developers.rentcast.io/reference/property-valuation)
2. Get [YNAB API Key](https://api.ynab.com/)
3. Get YNAB `Buget ID` and `Account ID`

This can be done by navigating to your budget in the browser, then extracting ID from the URL 

`https://app.ynab.com/XXXX/accounts/YYYY`  
`xxxx` = Budget ID  
`yyyy` = Account ID  

4. If you don't already have an account to track your property, create a new Unbudgeted tracking asset.

![](./images/Screenshot%202025-08-18%20at%2018.12.16.png)


Set the veriables in the 'Set Fields' node (Or setup subworkflow if you have multiple properties). 


| Variable| Explination | Example | 
| --- | --- | --- | 
|rentcast_api | api key for rentcast | |
| ynab_api | apk key for ynab | | 
| address | Exact address.  Its recomended to look it up in rentcast first since they use non standard values like 'srt' , 'ave', ect... |1600 Pennsylvania Ave NW, Washington, DC 20500 | 
| propertyType | one of 'Single Family', 'Condo', 'Apartment', see [api docs](https://developers.rentcast.io/reference/property-valuation) for all options | Single Family | 
| bedrooms | Number of bedrooms (whole number) | 3 |  
| bathrooms | Number of bathrooms, while fractions (2.5) are probably supported, they haven't been tested | 2 | 
| squareFootage | Total square feet | 1500 |  
| ynab_budget | Budget ID (derive from URL) |xxxx|  
| ynab_account | Account ID (derive from URL ) | yyyy |  

![](./images/Screenshot%202025-08-18%20at%2018.11.30.png)