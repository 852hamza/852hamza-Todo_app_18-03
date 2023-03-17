# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/todoApp/staticfiles/todoApp.png)
### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
$ git clone https://github.com/852hamza/852hamza-Todo_app_18-03.git
```
You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide


```bash
$ pip install django
```
Once you have downloaded django, go to todoApp directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we will start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

If you want run this Todo App on your AWS EC2 instance Follow these step

1. Create new Ec2 instance
2. Edit inbound security group with custom tcp (port)
3. connect your Ec2 instance and download the python3 and django and docker by these command
```bash
    $ yum/apt install python3/python
    $ pip install django
    $ yum/apt install docker
```
3. copy the repo by this command
```bash
    $ git clone https://github.com/852hamza/852hamza-Todo_app_18-03.git
```
4. Then run this command for creating the image
```bash
    $ docker build . -t Todo_app
```
5. After that run this command for running the docker container
```bash
    $ docker run -itd --name Todo-app -p 8000:8000 (image-id)
```
6. Copy your Ec2 public Ip and paste it to the browser like
```bash
    $ http://public_ip:8000
```

Cheers and Happy Coding :)
