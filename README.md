# srijanone/ez_decoupled

Enable api support and preview feature for decoupled apps.


## Installation

#### Install the project using composer 

```bash
composer create-project drupal/recommended-project:^10.0 ezdecoupled
cd ezdecoupled;
composer config repositories.drupal8 composer https://packages.drupal.org/8
composer config repositories.asset-packagist composer https://asset-packagist.org
composer config minimum-stability dev
composer config extra.enable-patching true
composer config --no-plugins allow-plugins.cweagans/composer-patches true
composer config --no-plugins allow-plugins.oomphinc/composer-installers-extender true
composer require cweagans/composer-patches
composer require drush/drush
composer require srijanone/ez_decoupled:dev-main
mv recipes/ web
composer install
drush si
drush recipe recipes/ez_decoupled;     
```
#### ddev setup

```bash
composer create-project drupal/recommended-project:^10.0 ezdecoupled
cd ezdecoupled;
ddev config --project-type=drupal9 --docroot=web --create-docroot
ddev start
ddev composer config repositories.drupal8 composer https://packages.drupal.org/8
ddev composer config repositories.asset-packagist composer https://asset-packagist.org
ddev composer config minimum-stability dev
ddev composer config extra.enable-patching true
ddev composer config --no-plugins allow-plugins.cweagans/composer-patches true
ddev composer config --no-plugins allow-plugins.oomphinc/composer-installers-extender true
ddev composer require cweagans/composer-patches
ddev composer require drush/drush
ddev composer require srijanone/ez_decoupled:dev-main
mv recipes/ web
ddev composer install
ddev drush si
ddev drush recipe recipes/ez_decoupled;     
```
## Tech Stack

**CMS:** Drupal

**Note:** This recipe depends on contributed libraries. Ensure you have Composer set up to manage these dependencies effectively by following the instructions in the guide.

#### Recommended Method for Installing, Updating, and Managing Contributed Module Libraries Using Composer

For detailed instructions on how to efficiently manage and install libraries for contributed Drupal modules using Composer, please refer to the official guide:

[Recommended Method for Installing, Updating, and Managing Contributed Module Libraries Using Composer](https://www.drupal.org/docs/extending-drupal/recommended-method-for-installing-updating-and-managing-contributed-module-libraries-using-composer)


This guide covers how to merge the `composer.libraries.json` with your site's `composer.json` file for seamless updates.

