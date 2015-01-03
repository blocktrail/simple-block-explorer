Simple Bitcoin Block Explorer
=====================

An example Bitcoin block explorer, using the [Blocktrail Bitcoin API](https://www.blocktrail.com/) and [Laravel framework.](http://laravel.com/). Basic frontend built with the lightweight css framework, [Skeleton](http://laravel.com/).

###Requirements
You need [composer](https://getcomposer.org/) to for package management in the backend. 


##Getting Started
1. Clone the repository and run `composer update` to download the required packages.

2. Go to [www.blocktrail.com](https://www.blocktrail.com/) and sign up for a free API account. Create an API key, and then add this to `.env.local.php` for your local environment, and/or to `end.php` if in your production environment. *(note that these files have been added to the .gitignore. You should always keep your API details secret)*

3. run `php artisan serve` to quickly setup a nice little local server serve the app 

4. With the server up and running now, simply navigate to [http://localhost:8000](http://localhost:8000) to see the block explorer at work 


##

###Need Help?
Get in contact with us at [devs@blocktrail.com](mailto://devs@blocktrail.com) and we'll be happy to help you in any way we can.

A tutorial will be coming soon describing the steps to creating this Bitcoin block explorer with Laravel.