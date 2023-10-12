"# HEISZERTON-REST-API-Crash-Course" 

Following along the simple tutorial "REST API Crash Course - Introduction + Full Python API Tutorial" on Caleb Curry youtube. (link to video: https://www.youtube.com/watch?v=qbLc5a9jdXo)


Usefull commands:

To create and run virtual environment:
py -m venv .venv							(create virtual environment)
.venv\Scripts\activate							(activate environment)
py -m pip install flask							(install flask)
py -m pip install flask-sqlalchemy					(install flask-sqlalchemy)
py -m pip freeze > requirements.txt					(save requirements to txt)
set FLASK_APP=application.py						(set flask application)
set FLASK_ENV=development						(set flask environment)
flask --debug run							(run in debug mode)


To init and add to database:
py									(launch the python command line)
from application import db, app, Drink
app.app_context().push()
db.create_all()								(create the database)
drink = Drink(name="Grape Soda",description="tastes like grapes") 	(create drink 1)
db.session.add(drink)							(add drink to db)
db.session.commit()							(commit to db)

