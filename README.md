# Easily Send Emails in Laravel with Brevo
This is an implementation of sending mail with Brevo in Laravel. A blog about this can be found here: [Easily Send Emails in Laravel with Brevo | Fajarwz](https://fajarwz.com/blog/easily-send-emails-in-laravel-with-brevo/).

## Installation

### Composer Packages 
```
composer install
```

## Configuration

### Create `.env` file from `.env.example`
```
cp .env.example .env
```

### Generate Laravel App Key
```
php artisan key:generate
```

## Run App
```
php artisan serve
```

## Send email demo

First adjust your `.env` file first with your own configuration.

```
MAIL_DRIVER=smtp
MAIL_HOST=smtp-relay.brevo.com
MAIL_PORT=587
MAIL_USERNAME=login.address@xxx.com
MAIL_PASSWORD=masterpassword
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="${MAIL_USERNAME}"
MAIL_FROM_NAME="${APP_NAME}"
```

Replace the email address destination in `routes\web.php`.

```php
\Mail::to('destination.address@xxx.com')->send(new \App\Mail\TestMail($details));
```

Visit the `localhost:8000/send-mail` to send the test mail.