# Continuous Delivery of Flask App on Google Cloud Platform
This repo contains source code on how to set up continuous delivery of flask app on Google Cloud Platform. Any push action is monitored by a predefined trigger so that once changes are made to the repo, they will be delpoyed automatically.

## Demo Video
[![](http://img.youtube.com/vi/vyJf69DbSKY/0.jpg)](https://youtu.be/vyJf69DbSKY "Continuous Delivery of Flask App on GCP")

## To replicate this project and add new routes
Run the following command in your GCP shell:

```
gcloud config set project $GOOGLE_CLOUD_PROJECT
git clone git@github.com:yichenghuang980/cd-flask-app.git
cd cd-flask-app
```

Create a python3 virtual environment:

```
virtualenv --python $(which python3) venv
source venv/bin/activate
```

Install all the packages needed:

```
make install
```

After editing the main.py file, run this command to test:

```
python main.py
```

Click the url link and enter one of the following route name each time:

```
/name/<value> : e.g. /name/wilson will take you to a page where value is wilson
/html: take you to a hello world page
/pandas: take you to a page which contains a pandas data frame
/wikipedia/<company>: e.g. /wikipedia/Netflix will take you to a page that introduces NetFlix
```
