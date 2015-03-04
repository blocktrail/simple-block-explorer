Simple Bitcoin Block Explorer
=====================

This a simple example of a Bitcoin block explorer, built using the [Blocktrail Bitcoin API](https://www.blocktrail.com/) and [Laravel framework.](http://laravel.com/).
You can use it to get started on integrating Bitcoin data in your own php applications.

###Requirements
***On Linux*** you need to install the following packages:
```
sudo apt-get install php5-bcmath php5-intl php5-gmp php5-mcrypt
sudo php5enmod mcrypt
```

***On Windows*** you need to enable the following extensions in your `php.ini`:
```
extension=php_intl.dll  
extension=php_gmp.dll  
```

You will also need [composer](https://getcomposer.org/) for package management in the backend.


###Getting Started
#####1. Copy the code
Clone the repository and run `composer update` to download the required packages.

#####2. Get an API key
Go to [www.blocktrail.com](https://www.blocktrail.com/) and sign up for a free API account. Create an API key, and then add this to an `.env.php` file in the project folder as follows:

    <?php     
      return array(
        'BLOCKTRAIL_KEY' ='MY_API_KEY',
        'BLOCKTRAIL_SECRET' ='MY_API_SECRET',
      );
*(note that this file has been added to the .gitignore. You should always keep your API details secret)*

#####3. Set up the server
run `php artisan serve` to quickly setup a nice little local server serve the app 

#####4. You're good to go
With the server up and running now, simply navigate to [http://localhost:8000](http://localhost:8000) to see the block explorer at work 


#####5. Things to know
***Windows Developers***  
A note for windows developers: you may encounter an issue in php with cURL and SSL certificates, where cURL is unable to verify a server's cert with a CA ((error 60)[http://curl.haxx.se/libcurl/c/libcurl-errors.html]).  
Too often the suggested solution is to disable ssl cert verification in cURL, but this completely defeats the point of using SSL. Instead you should take two very simple steps to solve the issue permanently:  

1. download `cacert.pem` from the [curl website](http://curl.haxx.se/docs/caextract.html). This is a bundle of trusted CA root certs extracted from mozilla.org. Save it in a folder within your php installation.  
2. open your `php.ini` and add/edit the following line (use an absolute path to where you placed the cert bundle):  
  ```
  curl.cainfo = C:\php\certs\cacert.pem
  ```



###Need Help?
Get in contact with us at [devs@blocktrail.com](mailto://devs@blocktrail.com) and we'll be happy to help you in any way we can.

A tutorial will be coming soon describing the steps to creating this Bitcoin block explorer with Laravel.
