# student-management-system

##Build Laravel 9 CRUD Application with MySQL & Bootstrap 5

An application for the institute to manage students and details.

###Step 1 - Download & Install 9
In the First Steps of Laravel 9 CRUD Application, we have to download and install fresh Laravel 9 Application in our computer. So for this, you have to goes to command prompt and then after goes into directory where you have run PHP 8 script and then after you have to run following command.

composer create-project --prefer-dist laravel/laravel laravel_9_crud

###Step 2 - Make Database Connection
After that, we need to create a database connection with MySQL database. So for this we have to open .env file and under this file, we need to add MySQL database configuration like MySQL database name, MySQL database user name, and password details.

###.env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=testing
DB_USERNAME=root
DB_PASSWORD=

###Step 3 - Create MySQL Table using Laravel 9 Migration
we have to crate students table under MySQL database from this Laravel 9 Application using Migrations. So first we have to create migration file under Laravel 9 application.

php artisan make:migration create_students_table --create=students

Then we have to run following command in command prompt and it will migrate MySQL table defination to 
MySQL database and create students table in MySQL database from this Laravel 9 Application.

php artisan migrate

###Step 4 - Create CRUD Model and Controller
we need to create Controller and Models file for CRUD Operation. So for this, we have goes to command prompt and run following command, which will create new CRUD StudentController and Student Model class file.

php artisan make:controller StudentController --resource --model=Student

###Step 5 - Add Service Provider for Bootstrap Pagination
we have to open app/Providers/AppServiceProvider.php and under this file, we have to add Paginator::useBootstrap() code under boot() method for support the bootstrap pagination.

###Step 6 - Create Views Blades File
we have to create following views blades files under ####resources/views
1. master.blade.php - This is master template file.
2. index.blade.php - This file we will used for display MySQL table data on the web page in HTML table format with pagination link.
3. create.blade.php - This file has been used for load Create Student form on the web page.
4. show.blade.php - This file has been used for display single student data on the web page.
5. edit.blade.php - This file has been used for load student edit form in the browser.

###Step 7 - Set Resource Route
we have to add resource route for student crud application, under ####routes/web.php

###Step 8 - Run Laravel 9 CRUD Application
Using the command prompt and run following command to start Laravel server.

php artisan serve

Then we go to the browser,and type give below URL and view output of Laravel student management project.

http://127.0.0.1:8000/students

