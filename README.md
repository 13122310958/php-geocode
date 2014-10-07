PHP Geocode
==========
A wrapper around the Google Geocoding API to get different details regarding an address such as 
- Latitude/longitude
- Country
- City
- District
- Postcode
- Town
- Street number

#Requirement
PHP >= 5.2.0 and <code>curl</code> enabled server.

Installation
=========
You can install the library using the following ways
#Composer
The recommended installation method is through <a href="http://getcomposer.org/">Composer</a>, a dependency manager for PHP. Just add <code>kamranahmedse/php-geocode</code> to your project's <code>composer.json</code> file:

```
{
    "require": {
        "kamranahmedse/php-geocode": "*"
    }
}
```
and then run <code>composer install</code>. For further details you can find the package at <a href="https://packagist.org/packages/kamranahmedse/php-geocode">Packagist</a>.

#Manual way
Or you can install the package manually by:
1. Copy <code>src/php-geocode.php</code> to your codebase, perhaps to the vendor directory.
2. Add the <code>Geocode</code> class to your autoloader or require the file directly.

#Getting Started
I'm going to use the address of <a href="http://gcuf.edu.pk">my university</a> to explain the use of library i.e.

```
$address = "Kotwali Road,Jinnah Town,Punjab، 38000 Faisalabad";
```
Firstly, you have to instantiate the <code>Geocode</code> class and pass the address, so your code will look like
```
$address = "Kotwali Road,Jinnah Town,Punjab، 38000 Faisalabad";

$geocode = new Geocode( $address );

// Note: All the functions below accept a parameter as a default value that will be return if the reuqired value isn't found
$geocode->getAddress( 'default value' ); 
$geocode->getLatitude(); // returns the latitude of the address
$geocode->getLongitude(); // returns the longitude of the address
$geocode->getCountry(); // returns the country of the address
$geocode->getLocality(); // returns the locality/city of the address
$geocode->getDistrict(); // returns the district of the address
$geocode->getPostcode(); // returns the postal code of the address
$geocode->getTown(); // returns the town of the address
$geocode->getStreetNumber(); // returns the street number of the address
```

#Feedback
I'd love to hear what you have to say. Please open an issue for any feature requests that you may want or the bugs that you notice. Also you can contact me at <a href="mailto:kamranahmed.se@gmail.com">kamranahmed.se@gmail.com</a> or you can also find me at twitter <a href="http://twitter.com/kamranahmed_se">@kamranahmed_se</a>