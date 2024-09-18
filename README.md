# Week 1: Familiarize with Tech Stack

## 1) Setup Your Machine
[] Install PHP. Download latest version in zipped folder from [here] (https://windows.php.net/download/) and extract. Put the folder in ProgramFiles. Verify the installation by running the below command:
```
php -v
```

[] Install NodeJS. Download and run node.exe from [here] (https://nodejs.org/en/download/prebuilt-installer). Verify the installation by running the below command:
```
node -v
```

[] Install Composer. Download and run Composer-Setup.exe from [here] (https://getcomposer.org/doc/00-intro.md#using-the-installer). Make sure PHP is already installed before do this step. Verify the installation by running the below command:
```
composer -v
```

[] Install VSCode. Download zipped version from [here] (https://code.visualstudio.com/download) and extract. Run code.exe.

[] Install Laravel Herd. Download from [here] (https://herd.laravel.com/windows?fbclid=IwAR1Xf0-4c9TJJv7wZEcXWd_kCYeSu7jSCr5touH3-I1lTXRv49nxAp1OrtA_aem_AahxCRT1vBH88VwHf3iHU1C5UXXmkid1mPq-sfew2QMpQjNmaVw0sHjOOpWOQ45aW14) and then run the .exe file to install. In here, you can also install NodeJS and PHP. Everytime you need to run laravel project, you MUST click the Start All Services button.

[] Install DBngin for windows from [here] (https://dbngin.com/) and install TablePlus for windows from [here] (https://tableplus.com/download).

   - DBngin and TablePlus Setup
     i) Click (+) plus button on the top and choose MySQL. Put the name as 'database' and click create.
     ii) Click start button. (This button should always start when the project is running)
     iii) Click arrow (->) button and then click 'Open in TablePlus'.
     iv) Create database by clicking database icon on top and then click new. Put database name, advisable to put the database name the same as your project folder name. For example, 'example-app'.


## 2) Create A Project
i) Create laravel project from command prompt. 
```
cd ~/Herd
laravel new my-app
cd my-app
```

ii) Choose setup as below:

iii) Open your project folder 'my-app' in VS Code. Path from C:\ > Users > user_folder_name > Herd > project_folder.
iv) From your prompt terminal, run below command:
```
composer install
```
```
npm install
```
```
cp .env.example .env
```
```
php artisan key:generate
```

v) Setup mailtrap in the .env. Login [mailtrap] (https://mailtrap.io/) using your GitHub account. Choose email testing and then select my inbox then choose PHP > Laravel 9+. Copy the API mailer and then replace that in .env.


vi) Setup database. 

vii) Run below command:
```
php artisan optimize:clear
```
```
php artisan migrate:fresh --seed
```

ix) You can see the laravel project created via below command:
```
php artisan serve
```

or just type my-app.test on the browser. Make sure DBngin and Laravel Herd already running.





