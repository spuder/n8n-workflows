# YNAB Super Budget

![](./images/Screenshot%202025-08-19%20at%2021.54.12.png)

Ever wish that Y.N.A.B was just a little smarter when auto-categorizing your transactions?

Now you can supercharge your YNAB budget with ChatGPT! No more manual categorization.

## Setup
Get a YNAB Api Key
Get YNAB Budget ID & Account ID (They are part of the URL) https://app.ynab.com/BUDGETID/accounts/ACCOUNTID

Every transaction that this workflow modifies will be tagged with n8n and color yellow. You can easily review all changes by selecting just that tag.

![](./images/Screenshot%202025-08-14%20at%2021.02.07.png)

## Customization
By default it pulls transactions from the last 30 days.
This workflow will post a message in a discord channel showing which transactions it modified and what categories it chose.

Discord notifications are optional.

![](./images/Screenshot%202025-08-18%20at%2023.41.54.png)

## Considerations
YNAB allows for 200 api calls per hour. If you have more than 200 Uncategorized transactions, consider reducing the previous_days value
