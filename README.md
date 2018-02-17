# php-page

A simple Class to work with RainTpl (Template System)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

You will need a web server and PHP configured.
This project is intended to be incorporated into another project, so the minimum prerequisite is the web server and PHP.

### Installing

Installation with Git:

```
git clone https://github.com/lcloss/php-page.git
```

Instalação com o Composer:

```
composer require lcloss/php-page
```

## Running the tests

### Initial setup

The default folder for the templates is ../app/views/front. If you want to change the default folder, change the $ tpl_dir variable in the Page.php file.

In the view folder of your system, create the header.html and footer.html file.
For this example, also create the home.html file.

At the end you will have a structure like:

```
app/views/front/src/footer.html
app/views/front/src/header.html
app/views/front/src/home.html
```

In your application, use:

```
$page = new Page();
$page->setTpl('home', [
	'title'	 => 'Title of your Project',
	'company' => 'Your company',
]);
```

### Creating a template

Create a template called hello.html in your views folder.
Type the following code:

```
<p>Hello {$username}!</p>
```

Use as follow:

```
$page = new Page();
$page->setTpl('hello', [
	'username'	 => 'Frederico Ferdinando',
]);
```

You will see like this:

```
Hello Frederico Ferdinando!</p>
```

## Built With

* [RainTpl](https://github.com/feulf/raintpl3) - The template system used

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [GitHub](https://github.com/) for versioning. For the versions available, see the [tags on this repository](https://github.com/lcloss/php-page/tags). 

## Authors

* **Luciano Closs** - *Initial work* - [LCloss](https://github.com/lcloss)

See also the list of [contributors](https://github.com/lcloss/php-page/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* This project was inspired by the [Curso Completo de PHP 7](https://www.udemy.com/curso-php-7-online/) from [HCode](https://www.hcode.com.br/)
* This README.md was build from [PurpleBooth README Template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
