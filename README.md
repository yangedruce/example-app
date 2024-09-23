# Week 1: Familiarize with Tech Stack

## 1) Setup Your Machine

- [ ] **Install PHP:**  
    Download the latest version as a zipped folder from [here](https://windows.php.net/download/) and extract it. Place the folder in `Program Files`. Verify the installation by running the following command:
    ```
    php -v
    ```

- [ ] **Install Node.js:**  
    Download and run `node.exe` from [here](https://nodejs.org/en/download/prebuilt-installer). Verify the installation by running the following command:
    ```
    node -v
    ```

- [ ] **Install Composer:**  
    Download and run `Composer-Setup.exe` from [here](https://getcomposer.org/doc/00-intro.md#using-the-installer). Make sure PHP is already installed before this step. Verify the installation by running the following command:
    ```
    composer -v
    ```

- [ ] **Install VS Code:**  
    Download the zipped version from [here](https://code.visualstudio.com/download) and extract it. Run `code.exe`.

- [ ] **Install Laragon:**  
    Download from [here](https://laragon.org/download/) and run the `.exe` file to install. **Important:** Every time you need to run a Laravel project, click the "Start All" button.

- [ ] **Install DBngin and TablePlus:**  
    - Download DBngin for Windows from [here](https://dbngin.com/).
    - Download TablePlus for Windows from [here](https://tableplus.com/download).

    ### DBngin and TablePlus Setup:
    1. Click the (+) button on the top and choose **MySQL**. Name it "database" and click **Create**.
    2. Click the **Start** button. (This should always be running when the project is active.)
    3. Click the arrow (→) button, then click **Open in TablePlus**.
    4. In TablePlus, create a new database:
        - Click the **database icon** on top, then click **New**.
        - Name the database (it's advisable to name it after your project folder, e.g., `example-app`).

---

## 2) Create A Project

i. **Create a Laravel project from the terminal. Click the terminal button on Laragon and run command:**
    
    ```
    composer create-project laravel/laravel example-app
    ```

ii. **Project Setup:**
    - Open the project folder (`example-app`) in VS Code. Path: `C:\laragon\www\example-app`.
    - From your terminal, run the following commands:

    ```
    composer install
    npm install
    cp .env.example .env
    php artisan key:generate
    ```

iii. **Setup Mailtrap in the `.env` file:**
- Log in to [Mailtrap](https://mailtrap.io/) using your GitHub account.
- Choose **Email Testing**, then select **My Inbox**.
- Select **PHP > Laravel 9+**, and copy the API mailer settings.
- Replace the mail settings in your `.env` file with the Mailtrap settings.

![Screenshot 2024-09-19 004829](https://github.com/user-attachments/assets/92bd10ee-16b0-47a1-b625-6172acfdb5e2)


![Screenshot 2024-09-18 234258](https://github.com/user-attachments/assets/8d24a9ff-87bb-4437-81ca-0a2606544833)


iv. **Setup the database in `.env`.**

![Screenshot 2024-09-19 004936](https://github.com/user-attachments/assets/84ac9d71-6a14-4242-a51b-0ebb48cb2b07)


v. **Run the following commands:**

    ```
    php artisan optimize:clear
    php artisan migrate:fresh --seed
    ```

vi. **View your Laravel project:**
- Run the following command:
    ```
    php artisan serve
    ```
- Alternatively, type `example-app.test` in your browser. Make sure both DBngin and Laragon are running.


# Week 2: Familiarize with Tech Stack: TailwindCSS & AlpineJS

## 1) Install TailwindCSS, Alpine.js, and their dependencies

    ```
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init
    ```

This will create a 'tailwind.config.js' file.

Install Alpine.js:
    
    ```
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init
    ```

## 2) Configure tailwind.config.js

Update the content section in your tailwind.config.js file to include your Laravel blade files, Vue components, and other front-end files where you'll use Tailwind classes:

![Screenshot 2024-09-23 234304](https://github.com/user-attachments/assets/60eb42e3-dc57-47cc-b4a2-303fc62dc753)


## 3) Create CSS and JavaScript Entry Points

In resources/css/app.css, add the TailwindCSS directives:

![Screenshot 2024-09-23 234328](https://github.com/user-attachments/assets/392eedbf-236d-48e5-ba35-69c10faf884c)


In resources/js/app.js, import Alpine.js:

![Screenshot 2024-09-23 235044](https://github.com/user-attachments/assets/3f010c4e-8f1b-4607-8363-59406c129f47)


## 4) Update vite.config.js

![Screenshot 2024-09-23 235145](https://github.com/user-attachments/assets/cdb45398-4a21-4fb2-9526-ff02cde0594f)


## 5) Set up the layout (app.blade.php)

In your Laravel app, create the layout file at resources/views/layouts/app.blade.php:

![Screenshot 2024-09-23 234453](https://github.com/user-attachments/assets/1949eedc-2786-4e57-97bb-678ae8df7b5b)

This layout includes Vite for asset management, and a basic Blade template structure with @yield for inserting content.


## 6) Create a new view (e.g., home.blade.php)

Create a new view file in resources/views and call it home.blade.php:

![Screenshot 2024-09-23 234517](https://github.com/user-attachments/assets/7a07cca2-ed8b-4ea3-b11b-27f1bf014b01)

This home.blade.php view file extends the app.blade.php layout and defines a simple homepage with a TailwindCSS-styled button and Alpine.js interactivity.


## 7) Update your route to return this new view

In routes/web.php, update the / route to return the home view instead of welcome:

![Screenshot 2024-09-23 234549](https://github.com/user-attachments/assets/0503ef34-e13f-48b6-9ad8-2e1296a911ff)

Or, alternatively, you make new route /home:

![Screenshot 2024-09-23 235955](https://github.com/user-attachments/assets/34324d48-d97e-46c6-9cc1-52c5d18432da)

So when you open the link: [example-app.test/home](http://example-app.test/home)







