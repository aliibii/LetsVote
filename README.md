# Dockerized Polling App with Django

You have to register in this app to show the polls and to vote. If you already voted you can not vote again. Only the owner of a poll can add poll , edit poll, update poll, delete poll , add choice, update choice, delete choice and end a poll. If a poll is ended it can not be voted. Ended poll only shows user the final result of the poll. There is a search option for polls. Also user can filter polls by name, publish date, and by number of voted.

<h1>Prerequisites</h1>
<code>python== 3.5 or up , django==2.0 or up and Docker-compose== 1.29.2 </code>


<h2>Installation</h2>
<pre>open terminal and type</pre>
<code>git clone https://github.com/aliibii/LetsVote.git</code><br><br>

and then run the following in the directory to run the app on port 80 (you can change it in docker-compose.yml):

<code>sudo docker-compose up --build -d</code>

<h2>To migrate the database type</h2>

<code>sudo docker-compose run web python manage.py makemigrations</code>

<code>sudo docker-compose run web python manage.py migrate</code>

<h2>To use admin panel you need to create superuser using this command </h2>
<code>sudo docker-compose run web python manage.py createsuperuser</code>


<h2>To Create some dummy text data for your app follow the step below :</h2>
  (just on your local host for testing the app, if you're going to run it on docker-compose then you need to update the requirments.txt file and the Dockerfile.yml)
<code>pip install faker</code>
<code>python manage.py shell</code>
<code>import seeder</code>
<code>seeder.seed_all(30)</code>
<p>Here 30 is a number of entry. You can use it as your own</p>
