# Introduction #

Terra Data combines all the tasks we often repeatedly perform that are related to our data and gives them to you in an extremely easy to use library. From validation to HTML form generation, and even API generation, and even exporting/importing data to/from different formats, everything is taken care of for you. All you need to do is create a simple PHP array that tells Terra Data what the data you want to handle is.

# Getting and Configuring Terra Data #

Getting Terra Data ready to use couldn't be any easier.
  * [Download Terra Data](http://code.google.com/p/terradata/downloads/list)
  * Unzip and upload the lib folder in your project's directory or in your server root.
  * Make `lib/Terra_AppData` writable (CHMOD the folder to 0777 if you're using a Unix/Linux server)
  * To use Terra Data on your project(s), add `require_once 'lib/Terra/Autoload.php';` to your code.
  * That's it! You can now use Terra Data on your project(s).

There is no need to include any Terra Data files on your code, since Terra Data automatically registers an autoloader to take care of that for you.

# Using Terra Data (Basic) #

-> Talk about data set configurations and instantiating Terra Data.
-> Link to more advanced document.