Simple Instruction to deploy the app on a EC2 instance:

create a EC2 instance in AWS with proper security group rule (Inbound traffic from port 8000 )
Login to the instance then follow the underlying steps :
1.	Update the System  :   sudo apt-get update
2.	Clone the repository : git clone https://github.com/Souvik-clr/DJango-app.git

Go inside the folder : cd Django-app

3.	Download django usig pip :  A. sudo apt install python3-pip -y  B.  pip install Django

In Django-app /django_project/settings.py change ALLOWED_HOSTS = [ 'Instance_IP', ] 

4.	To create all the migrations file (database migrations) required to run this App : python3 manage.py makemigrations
5.	To apply this migrations  :  python3 manage.py migrate
6.	One last step and then our App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user : python3 manage.py createsuperuser
7.	Start the server by following command : python3 manage.py runserver 0.0.0.0:8000
