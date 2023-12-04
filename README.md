# Dayana_Web_Django


we’ll build a Blog application for Dayana family with Django that allows users to create, edit, and delete posts. The homepage will list all blog posts, and there will be a dedicated detail page for each individual post. Django is capable of making more advanced stuff but making a blog is an excellent first step to get a good grasp over the framework. The purpose of this chapter is to get a general idea about the working of Django.

step 1: Generated by ('django-admin startproject myProjectName') using Django 4.0.5 in terminal.

step 2: Install using pip, including any optional packages you want...:
tip: You can use this command: pip install -r requirements.txt ,Install the packages used for this project

    pip install django
    pip install djangorestframework
    pip install markdown                # Markdown support for the browsable API.
    pip install django-filter           # Filtering support

step 3 : Create our own app with this command :('python manage.py startapp appname') in terminal, and Add my app to the installed app in settings.py

step 4: Add templates and use block and endblock to separate header base sidebar footer

step 4: Add my apps to your INSTALLED_APPS setting:

        INSTALLED_APPS = [
            ...
           `# my app
            'home.apps.HomeAppConfig',
            'account.apps.AccountConfig',
            'blog_post.apps.BlogPostConfig',

            'django_cleanup.apps.CleanupConfig',
            'django_render_partial',
            'django_social_share',
            # my widget 
            'widget_tweaks',
        ]
        # And add static files and media files:

        # Static files (CSS, JavaScript, Images)
        STATIC_URL = 'static/'
        MEDIA_URL = 'media/'
        STATICFILES_DIRS = [os.path.join(BASE_DIR ,"static")]
        MEDIA_ROOT = os.path.join(BASE_DIR, 'media')

step 5: Create your model(appname/models.py) and in terminal we enter makemigration and migrate with their commands (python manage.py makemigration , python manage.py migrate) please check all models

step 6:Create your form(appname/forms.py) please check all forms

step 7:Create your mixin(appname/mixins.py)

step 8: Create your class base views(appname/views.py) please check all views

step 9: Register your models(appname/admin.py) & in terminal Create super user with command (python manage.py createsuperuser)

step 10: appname URL Configuration(appname/urls.py) please check all urls

step 11: myProjectName URL Configuration(appname/urls.py) Add path of urls myProjectName

        urlpatterns = [
            ...
            path('', include('appname.urls'))
        ]
    # And add path of statics files
        urlpatterns += static(settings.MEDIA_URL,document_root = settings.MEDIA_ROOT)

