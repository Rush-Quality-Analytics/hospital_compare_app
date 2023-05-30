# hospital_compare_app
Python source code for the Rush [Hospital Compare Application](https://hospital-compare.herokuapp.com/).

## Description and functionality

The Rush [hospital compare application](https://hospital-compare.herokuapp.com/) is a freely available and lightweight python-based Plotly dashboard application for aggregating, analyzing, and downloading data from the Rush [hospitals-data-archive] (https://github.com/Rush-Quality-Analytics/hospitals-data-archive). This open-source tool allows users to compare data features among hospitals and across time, to explore relationships between features, to design new features and examine them across time, and to download 700+ data features from any of 6,000+ hospitals, and for each year (and most yearly quarters) since 2013.

## How to run this app

1. After downloading or cloning this repository, open a terminal window or command prompt in the root folder.

2. Create a virtual environment for running this app with Python (>=3.8)

	In MacOS or Linux:
	  
	```
	python3 -m virtualenv venv
	
	```
	In Unix:
	
	```
	source venv/bin/activate
	
	```
	In Windows: 
	
	```
	venv\Scripts\activate
	```
3. Install required packages using pip:

	```
	pip install -r requirements.txt
	```

4. Run this app locally with:

	```
	python3.8 app.py
	```

	The output of the terminal window will look like:

	```
	Dash is running on http://0.0.0.0:8050/
	```
	
5. Paste the url into your web browser and voila!

## Requirements
These are automatically installed when following the instructions above.

* werkzeug==2.0.3
* dash==2.0.0
* gunicorn==20.1.0
* numpy==1.22.1
* pandas==1.4.0
* scipy>=1.7.3
* flask>=1.1.2
* plotly==5.5.0
* datetime==4.3
* pathlib==1.0.1
* statsmodels==0.13.1
* scikit-learn==1.0.2
* dash_bootstrap_components==1.0.2
* lxml==4.8.0

## Files & Directories

<details><summary>app.py</summary>	
The primary file for running the Rush hospital compare application. This file contains the entirety of source code for the app as well as many comments to explain the application's functionality.
</details>

<details><summary>assets</summary>
Files in this directory are used by the application to format its interface or are used as images in this README file. All files except `RUSH_full_color.jpg` were obtained from another open source Plotly Dash app (https://github.com/plotly/dash-sample-apps/tree/main/apps/dash-clinical-analytics/assets.): `Acumin-BdPro.otf`, `base.css`, `clinical-analytics.css`, - `plotly_logo.png`- `resizing.js`


- `Acumin-BdPro.otf`: An OpenType font file used by the application. 
- `base.css` A cascading style sheets (CSS) used by the application. CSS is a stylesheet language used to describe the presentation of a document written in HTML or XML.
- `clinical-analytics.css` An additional css file.
- `plotly_logo.png`
- `RUSH_full_color.jpg`
- `images_for_README`: A directory containing png files used in this README document.
</details>

<details><summary>Procfile</summary>	
This extensionless file is necessary for deployment on Heroku, and essentially tells Heroku how to handle web processes using the gunicorn server. The file contains a single line with the following: `web: gunicorn app:server`
</details>

<details><summary>requirements.txt</summary>		
This file lists all of the software libraries needed for the app to run. When deploying the app on Heroku, this file is used to set up the server with the libraries necessary for running the application. When used locally, this file tells pip which libraries need to be installed (i.e., `pip install -r requirements.txt`).
</details>

<details><summary>runtime.txt</summary>
This file is used when setting up the app to run on an online Heroku server. It contains a single line: `python-3.8.12, indicating the version of python to use. 
</details>

## Developer 
Kenneth J. Locey, PhD. Senior Clinical Data Scientist. Center for Quality, Safety & Value Analytics. Rush University Medical Center.