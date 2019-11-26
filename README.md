# python_server
Configure Apache as Python server - simple steps 

#install Apache
1. sudo apt update
2. sudo apt install apache2

#Install mod_wsgi
1. for python 3.6 (preferable)
2. sudo apt-get install libapache2-mod-wsgi-py3 python-dev

for python 2.7

sudo apt-get install libapache2-mod-wsgi-py python-dev

Install flask
(Assuming you have pip3.6 installed)
pip3.6 install flask


Let create a nested directory named as ExampleFlask in home direcory (location could be anything)

mkdir -p ~/ExampleFlask/ExampleFlask

Add below 3 files in the inner ExampleFlask directory

__init__.py
Empty file

my_flask_app.py


Let's create the config file for our flask application
vim /etc/apache2/sites-available/ExampleFlask.conf

Enable the file with a2ensite:

sudo a2ensite /etc/apache2/sites-available/ExampleFlask.conf

Restart apache2
So, the new changes could take effect.

apache2 -f /etc/apache2/apache2.conf -k stop
apache2 -f /etc/apache2/apache2.conf -k start

Check browser if it's running your flask app at your machine IP address with prefix /testFlask
url : http://192.168.1.103/testFlask/

Congratulations, we have successfully deployed a flask application on ubuntu 18.04
