Pop PHP Skeleton Application
============================

OVERVIEW
--------

This is a basic skeleton application for the Pop PHP Framework to demonstrate how to
wire up some simple routes for a web-facing application and a CLI-based application.

INSTALL
-------

Clone the repository and install it:

```console
$ composer install
```

Once installed, the web access point is at `public/index.php` and the main
CLI access point is at `bin/pop`

BASIC USAGE
-----------

### Web

Running the built-in PHP web server with `php -S localhost:8000 -t public`,
try these routes to test the web application:

    http://localhost:8000/
    http://localhost:8000/edit/1001

You should see the home page and an "edit" page, respectively.

### CLI

Setting the `bin/pop` script to be executable, you can test the CLI
application like this:

```console
$ ./bin/pop help
$ ./bin/pop hello world
```

You should see the help screen and a "hello" screen, respectively.

NOTES
-----

* The web application has a view folder, `app/view`, that holds the view scripts for page display.
* The web application is utilizing the `pop-http` component to leverage the HTTP request and
response objects within the controller object.
* The CLI application is utilizing the `pop-console` component to leverage it for parsing
the CLI requests and returning the appropriate responses on the CLI.
