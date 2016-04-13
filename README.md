# Open Earth Documents

This repository contains documents to support Open Earth projects understanding the network features and infrastructure and facilitate migration and project management.

## Technical specifications

Open Earth is an environmental geojournalism network using WordPress Multisite with [JEO](http://jeowp.org), custom JEO child themes and several plugins.

### Core features running versions

| Software | Version |
| --- | --- |
| WordPress | **4.3.1** |
| JEO | **1.0.5** |

## Available features

### JEO child themes

List of installed and available JEO child themes:

 - JEO Newsroom
 - Mekong Eye
 - Ekuatorial
 - InfoAmazonia

### Plugins

List of installed and available plugins:

| Plugin | Version |
| --- | --- |
| Advanced Custom Fields | **4.4.4** |
| Advanced Custom Fields: qTranslate | **1.7.9** |
| Better Analytics | **1.1.2** |
| Custom Post Type UI | **1.1.2** |
| iframe | **4.2** |
| JEO API | **0.0.3** |
| Jetpack by WordPress.com | **3.8.2** |
| Page Builder by SiteOrigin | **2.2.2** |
| qTranslate-X | **3.4.6.4** |
| SiteOrigin Widgets Bundle | **1.5.4** |
| WP Feature Box | **0.1.3** |
| WP Paginate | **1.3.1** |
| wpckan | **1.2.0** |
| Yet Another Related Posts Plugin | **4.2.5** |

## Start your project inside the network

Contact xx@xx.com with your thoughts.

## Develop a project from stratch

This network is based on [JEO](http://jeowp.org), a wordpress parent theme that works as a framework for geojournalism project.

You can check out the [project documentation](http://www.jeowp.org/) and also use [JEO Blank](https://github.com/InfoAmazonia/jeo-blank) as a bootstrap to start your own JEO child theme.

If you'd like to later integrate your project to the network, please be aware of the network's software versions before submitting your project.


## Migrating your current project to the network

Learn how you should prepare your project's code and database to integrate the network.

The project owner is responsible for adapting the project's theme and database to Open Earth infrastructure standards:

### Steps overall

 - Check the software versions on the list above, your project should work with this environment.
 - Make sure your theme's code runs with this setup of WordPress
 - Make sure your database runs with this setup of WordPress

### Migration tips

#### Previous to version 1.0

If your JEO project runs on a version previous to **v1.0.0** its most important that you check out the [changelog and diff for this version](https://github.com/oeco/jeo/releases/tag/v1.0.0). A new layer system was launched.

Instead of storing the layers as a post meta to the map, it has its own post type. This allows a single published layer to be used across different maps.

**The new system will make all your current published maps without layers, since it will look elsewhere for them.**

You'll need to migrate your layers manually or create a migration script to the new layer system.

## Submit your project

Considering you already have your project migrated to the network standards you should submit your code and database to us.

### Submitting the theme's code

You can submit a zip file with the theme's code or the theme's git repository url, stating which branch/release to be imported.

### Submitting the project's database

The database should be in WXR (WordPress eXtended RSS) format. This is the native format for the WordPress export file, XML based.

### Plugins policy

We don't accept new plugins instalation, Open Earth provides a good set of plugins that you can use on your project. If a specific plugin is crucial for your project and is missing on the list, let us know.

## Migration FAQ

### Why don't you accept the whole WordPress folder for import?

Since we are using WordPress Multisite, we already run a WordPress installation, which your project will be part of. All projects share the same core, allowing the network maintenance to support all projects.

### Why not accept SQL file for database import?

WordPress MultiSite has a different approach to its database infrastructure. Thats why its important to use the native import tool. SQL requires manual edits to the import file, which is not ideal and can result in errors.
