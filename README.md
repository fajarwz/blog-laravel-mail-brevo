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

Replace the email address destination in `routes\web.php`

```php
\Mail::to('destination.address@xxx.com')->send(new \App\Mail\TestMail($details));
```

Visit the `localhost:8000/send-mail` to send the test mail.