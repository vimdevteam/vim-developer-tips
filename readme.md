# VIM Development - Basic Overview

Hello, fellow VIM developer! If you are like me, this is probably your first development job and you may have some questions on how to start development on a new project. Don't worry, that's what this guide is for helping you do.

VIM primarily uses WordPress as the technology stack and framework to create sites. There are many benefits to this, the main one being that it is a great start for a static site with a blog section. Here are some of the technologies that you will use on WordPress sites:

HTML/CSS
Javascript (primarily jQuery)
PHP
Apache

## Getting Started

So you've been assigned to start development on a new site, and don't know where to start. The first step you take will be to install WordPress on the computer/server that you are developing on. I recommend starting development locally for fast refresh times.

Once WordPress is installed, you will then need to install a theme. In the past, VIM has usually purchased themes that the design team found appealing, but this practice increases development time because you have to learn how the theme works and where you go to change certain things.

Thus, the solution that I have found is to create a master theme that can then be reused/customized as we need. This theme uses PHP and SASS to create modular components that can be easily maintained or swapped out. You can find the theme on the VIM GitHub account, the instructions on how to install it can be found there.

## Development tips

1. Start with the home page. Develop the site header/menu for all screen widths. I usually like to start with the mobile view (320px) and work my way up to larger screen sizes like tablets (~768px) and desktop (1024px).

2. Once you are done with the header, create the page content and the footer. Then you can work on other pages until the site is complete.

3. Use FontAwesome for icons.

4. If you need to create a custom post type (like videos, or team members) use the Pods Framework. It's a free plugin that makes custom post types very easy to create. You can also use this plugin to extend a post type easily (like if you want to add a custom field to pages or posts).

5. If you come across an error that you aren't sure what is causing it, there are steps you can take:

* Refresh permalinks. This can be done by visiting the permalink page in your settings.
* Check your error logs. They are usually in the root folder of the WordPress install or in your server logs.
* Disable all plugins (if your error goes away, you know it's a plugin)
* Switch your theme (if it goes away, you know it's somewhere in your theme)
* Google is your friend! Stack Overflow has a lot of PHP and WordPress topics that can help you!

## WooCommerce sites

The previous advice is nearly all you need for standard WordPress sites, but things get a bit trickier when the site has a store. You will have to manage Products as another post type, add shipping information, checkout options, and a host of other things. It can be a little bit daunting, but that's why this guide is here!

Ideally, before you start developing a WooCommerce site, you will have all of the product information somewhere. This includes but is not limited to:

* Product Title
* Description
* Price
* Product Image(s)

This is the bare minimum that you will need for product info. It is usually best to get all of this as soon as you can in the form of a spreadsheet and then you can import the products into your site using an import tool.

Other things you may need:

1. Payment method(s). PayPal is the easiest, if they want to accept cards directly on their site this gets a bit trickier. They will need to install an SSL certificate and provide credentials for whichever service they want to use.

2. Shipping method(s). Do they do flat rate? If so then It's a lot easier. Do they use a certain shipping service like FedEx or UPS? If they do, then you have to get the weight and dimensions of every product, and integrate it with whichever API they want.

3. Inventory management - Most people do not need this, but WooCommerce has a way to handle inventory management. However, if they have a third-party system that they want to integrate with their shop then you will most likely have to find a plugin that will do it for you.