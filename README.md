xci
===

#### Merging the xAPI, Learning Registry and Medbiquitous competency and performance frameworks. Tested with Ubuntu 12.04.3 and Python 2.7.3

## Installation

Software Installation

	sudo apt-get install build-essential python-dev python-virtualenv mongodb git
	sudo easy_install pip
	sudo pip install virtualenv

Setup Mongo (The app uses xci as the name as the database, but you can change that in the app if you wish)
	
	mongo
	use xci
	db.addUser("username", "password")
	db.auth("username", "password")

Install packages (inside of the virtualenv you created first)

	pip install -r requirements.txt

Add index

	mongo xci
	db.competency.ensureIndex({"title": 1})

Run

	python runserver.py

	(If you want to run the mongo shell run: mongo xci)
