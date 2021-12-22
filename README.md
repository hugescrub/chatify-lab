Based on [Chatify](https://github.com/munafio/chatify)

Following steps were done in Ubuntu 20.04 LTS

## Requirements

`sudo apt install git php mysql-server composer php-mysql`

Installing nodejs:

* `sudo apt install curl`
* `curl -fsSL https://deb.nodesource.com/setup_17.x | sudo -E bash -`
* `sudo apt-get install -y nodejs`

## Database setup

In case of first MySQL installation:

* `sudo mysql`
* `ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';`
* `\q`
* `mysql -u root -p`
* `CREATE DATABASE laravel;`
* `\q`

Or simply:

* `CREATE DATABASE laravel;`

## Installation

* `git clone https://github.com/hugescrub/chatify-lab.git`
* `cd chatify-lab`
* `composer install --ignore-platform-reqs`

Open `.env` file with text editor and change database connection
settings on line 11 if required.

Default settings are:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root
```

* `php artisan migrate`
* `php artisan key:generate`
* `npm install`
* `npm run dev`
* `php artisan storage:link`
* `php artisan serve`

Open localhost:8000
