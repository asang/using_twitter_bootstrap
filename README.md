# Using Twitter Bootstrap

This article taks about using [Twitter bootstrap][bootstrap] to create
responsive, professional and responsive user interface with as little effort as
possible Railscast [episode
328](http://railscasts.com/episodes/328-twitter-bootstrap-basics) and [episode
329](http://railscasts.com/episodes/329-more-on-twitter-bootstrap) cover the
basics in great detail. 

## Basics ##

```
rails new store
rails g scaffold product name price:decimal --skip-stylesheets
rake db:migrate
rails g bootstrap:install
rails g bootstrap:themed products -f
```

In order to render the initial view, you might have to run:

	rake db:setup
	rake db:seed
	rake assets:precompile

To run the application in production environment, 

	RAILS_ENV=production

can be prepended to the command-line

## Using Simple Form ##

Using [<code>simple_form</code>][simple form] gem, we can improve the user interface and make the
application more usable. `product` model in this case has been enhanced to take
advantage of this.

## Converting this file to ... ##

[Pandoc][pandoc] can be used to convert this file and practically any format
for your choice

```
pandoc README.md -o README.html
```

[bootstrap]: http://getbootstrap.com/css/#less
[episode 328]: http://railscasts.com/episodes/328-twitter-bootstrap-basics
[episode 329]: http://railscasts.com/episodes/329-more-on-twitter-bootstrap
[simple form]: https://github.com/plataformatec/simple_form
[pandoc]: http://johnmacfarlane.net/pandoc/index.html
