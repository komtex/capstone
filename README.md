# Final project
My final project for **cs50w** is a plain web application for managing
martial art memberships.   
The whole application is based on the Django framework,
which take care of user authentication, site maps, create automatically
database tables and many more tasks-right out of the box.
To facilitate responsive content this application uses Bootstrap CSS
which make web application mobile responsive. Bootstrap's grid system
uses a series of containers, rows and columns to layout and align content.
It's built with flexbox and is fully responsive.  
The difference between capstone project and previous projects is that:
- *This application* makes use and manage the data to check the
membership users, update and add user's information using **post-save**
signal which work on the concept of senders and receivers. The sending
component is model User, and the receiving component is the processing
handler function that works on the data once it receives a notification
that the data is just has been saved.  
- *Was created* register/login modal form, dynamically using JavaScript
to edit modal, depending on if its register or login.  
- *Finally* I include lettering.js library which create some cool
effects to make web pages more attractive.  
## Folders and files
- *Membership* - main application directory.
    - *static/membership* - contain all static content.
    - *scripts.js* -JavaScript file for manage modal register/login using fetch API.
    - *jquery.lettering.js* - A jQuery plugin for radical web typography,
    animations text.
    - *styles.css* - All CSS files.
-  *templates/membership* - All templates files.
    - *layout.html* - main template. All other templates extend it.
    - *index.html* - basic template, which show search form where you can search
    membership in database, by input any words. Links to all other pages
    only for login and register users and JavaScript splitting text animation
    which triggering by clicking the word subscribe.
    - *add_user.html* - template for adding new members to database.
    - *update_user.html* - template for update users information in database.
    - *view_user.html* - this one shows member's database data, links to
    update.html and search form.
- *views.py* - respectively, contain all application views.
- *urls.py* - all application URLs.
- *test.py* - contain class and function for test User objects.
- *forms.py* - hear I added some classes for update and add User model
and Meta class for User model.
- *models.py* - contain one custom user model `AbstractUser`.
## Usage
- Make and apply migrations:
```
  python manage.py makemigrations  
  python manage.py migrate
```  
- start Django development server:  `python manage.py runserver`

[The capstone video:](https://youtu.be/4ccpb_kpSoc)               
