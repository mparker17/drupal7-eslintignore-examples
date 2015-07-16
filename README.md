# drupal7-eslintignore-examples

Some eslintignore samples for Drupal 7 projects.

Since Drupal's coding standards differ slightly from other communities, [ESLint](http://eslint.org/) needs a `.eslintrc` file (and usually, a `.eslintignore` file as well) in your project's root directory. 

If you're working on a Drupal 8 project, ESLint will just work, because it's configuration files ship with Drupal 8.0.x core. For other projects, you'll need to [copy `.eslintrc` from Drupal 8 core](http://cgit.drupalcode.org/drupal/tree/.eslintrc).

[Drupal 8.0.x core's `.eslintignore`](http://cgit.drupalcode.org/drupal/tree/.eslintignore) probably won't work for your project, but this project is designed to provide some example ones that will.

# Which example file do I use?

## If the root of your repository is Drupal core

Use [the example at `core/.eslintignore`](blob/master/core/.eslintignore).

## If the root of your repository is an installation profile (in `profiles`)

Use [the example at `core/ .eslintignore`](blob/master/core/profiles/example/.eslintignore).

## If the root of your repository is site directory (in `sites`)

Use [the example at `core/ .eslintignore`](blob/master/core/sites/example/.eslintignore).

## If you're writing a custom theme or module

If you're writing your own JavaScript for a theme or module, you probably don't need a `.eslintignore` — just put the `.eslintrc` in your theme or module folder.

If you do need a `.eslintignore` to ignore the code in someone else's JavaScript that you're committing to your theme or module, keep in mind that [you cannot upload code to Drupal.org which is not GPL2-licensed](https://www.drupal.org/licensing/faq) (you can still use it, but you will need to put the library in `sites/all/libraries` and use [the libraries API](https://www.drupal.org/project/libraries)).

If you're not planning to contribute the theme or module to the Drupal community, then you'll have to [write your own `.eslintignore`](http://eslint.org/docs/user-guide/configuring#ignoring-files-and-directories) because there is not a standard structure for JavaScript files in a theme or module.

## If "its complicated"

I would start by looking at all the examples here and choosing one that makes the most sense for your repository. You might need to [customize it or write your own `.eslintignore`](http://eslint.org/docs/user-guide/configuring#ignoring-files-and-directories).

In most cases, you will want to place the `.eslintignore` in the same folder as the `.eslintrc` file to make them easier to find. Put both files:

* In a folder which you will run the `eslint` command from, or in one of the ancestors of the folder that you run `eslint` from, and,
* In a folder that contains JavaScript, or whose descendent folders contain JavaScript.

In really complicated setups, you might need multiple copies. This is okay; just remember that will have an impact on how easy it is to maintain.

# Notes

For more information, including how to customize one of these, read [the official `.eslintignore` documentation](http://eslint.org/docs/user-guide/configuring#ignoring-files-and-directories).
