# drupal_recipe/ez_decoupled

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
composer require drupal_recipe/ez_page_builder:dev-main
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
ddev composer require drupal_recipe/ez_page_builder:dev-main
mv recipes/ web
ddev composer install
ddev drush si
ddev drush recipe recipes/ez_decoupled;     
```
## Tech Stack

**CMS:** Drupal

