# learning-python-dash
This is a repository for study notes from LinkedIn Learning course `Data Visualization in Python with Dash`.

## Repository structure
This repository contains files according to each specific topic:

* `basic-dash-app.py` basic Dash app structure
* `basic-precious-metals.py` basic Dash app based on Precious Metals dataset
* `plotly-express-graph-configuration.py` how to customize your visualization with plotly
* `style-arguments-for-css.py` how to customize your visualization with CSS style arguments
* `with_assets` folder contains an example of app with CSS and ICO assets
* `dash-callbacks.py` basics of callbacks in Dash
* `dropdown.py` implementation of selectize dropdown and date range selector features

## Heroku Deployment Setup
* Install Git
* Install Heroku CLI
* Make sure both of these are in your system path
* Create a Heroku account

## Deployment Steps
Prepare virtual environment
```commandline
python -m venv venv

source venv/bit/activate

pip install  dash
pip install pandas
pip install gunicorn

pip freeze > requirements.txt
```
Setup Heroku and Git
```commandline
# If not already logged in
heroku login -i

git init

# Change my-dash-app to a unique name
heroku create my-dash-app

# Add all files to git
git add .
git commit -m "init commit"

# Deploy code to Heroku
git push heroku master

# Run the app woth a 1 Heroku "dyno"
heroku ps:scale web-1
```