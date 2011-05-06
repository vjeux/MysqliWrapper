<a href="http://blog.vjeux.com/2009/php/mysqli-wrapper-short-and-secure-queries.html">MysqliWrapper</a> - Short and Secure Queries
===============

Mysqli Wrapper is shortening the code required to run queries, make them 100% safe against SQL Injections and gives a handy Array as result. No more pain writing queries!

When developing a PHP application, SQL queries is the most dangerous area. This is because the built-in tools are either not secure by conception or too much complicated to use. I've made a little wrapper to mysqli that solves all these problems and make you enjoy writing queries!

What's good about this:

* A single 6 characters function
* Secure because parameterized
* Returns an Array
* Easy migration from the basic method


Example
-------

```javascript
$db = new dbWrapper('host', 'user', 'pass', 'database', true);

$result = $db->q("
  SELECT Name, CountryCode
  FROM City WHERE Zip = ? AND Population > ?",
  'si', $zip, $pop);

foreach ($result as $key => $city) {
  // $city['Name'], $city['CountryCode']
}
```



Read the full explanation on my blog: http://blog.vjeux.com/2009/php/mysqli-wrapper-short-and-secure-queries.html
