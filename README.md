# FARMFORECAST

A web frontend for forecasting hydroponic lettuce sales and generating a planting schedule.

## What it does

1. Pick a vegetable type — RedOak, GreenOak, RedCoral, or Frillice
2. Upload a CSV of historical sales data for that vegetable (at least 17 months of data, no BOM)
3. Choose the month to forecast
4. The app sends the file to the [deploy-fastapi](https://github.com/Fielddddd/deploy-fastapi) backend, which returns a predicted sales weight (kg) for that month
5. From the predicted weight, it works out how many plants are needed and lays out a 3-round planting schedule with seeding, transplanting, and harvest dates

## Stack

Plain HTML/CSS/JS. No build step — open `index.html` or serve the folder statically.

## Backend

Calls the FastAPI service in [deploy-fastapi](https://github.com/Fielddddd/deploy-fastapi) (`/upload_csv` endpoint) to get the sales prediction.
