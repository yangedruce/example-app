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

- [ ] **Install Laravel Herd:**  
    Download from [here](https://herd.laravel.com/windows) and run the `.exe` file to install. You can also install Node.js and PHP using Herd. **Important:** Every time you need to run a Laravel project, click the "Start All Services" button.

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

i. **Create a Laravel project from the command prompt:**
    ```
    cd ~/Herd
    laravel new my-app
    cd my-app
    ```
![Screenshot 2024-09-18 232712](https://github.com/user-attachments/assets/176e4db9-ffe5-4438-94aa-5b47cbab3c10)

ii. **Project Setup:**
    - Open the project folder (`my-app`) in VS Code. Path: `C:\Users\your_user_name\Herd\my-app`.
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
![Screenshot 2024-09-18 234258](https://github.com/user-attachments/assets/8d24a9ff-87bb-4437-81ca-0a2606544833)

iv. **Setup the database in `.env`.**

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
    - Alternatively, type `my-app.test` in your browser. Make sure both DBngin and Laravel Herd are running.
