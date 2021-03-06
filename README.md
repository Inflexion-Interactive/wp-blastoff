<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/794809/7395239/b36379d4-ee66-11e4-8778-28fa95663a61.gif" alt="Blastoff Rocket" />
</p>

# WordPress Blastoff

#### About WP Blastoff

This repository serves as a jumping off point in WordPress development. A modern development workflow should (be/provide):

- fully version controlled
- multiple environments
- straightforward deployment solution
- easily maintainable

This is what we hope to achieve with **WordPress Blastoff**. A repo that will help bootstrap your WordPress projects, but provide the flexibility and customization to accomodate any specific needs.

#### What is involved

Below are the main components of the project:

- **Local** environment setup with [Vagrant](https://www.vagrantup.com/)
- Deployment and Apache provisioning to both **Staging** and **Production** environments with [Mina](http://mina-deploy.github.io/mina/)
- Incredibly easy WordPress core updates (*coming soon*)

## Getting Started

### Setting up Production Environment

To begin, we'll need to create our **production** server first. Since the goal is to mirror our production environment, we'll use this to then setup our other environments. So let's get to it!

<img src="https://cloud.githubusercontent.com/assets/794809/7400105/6e9269ec-ee88-11e4-8c2a-6b109d68d316.png" width="437" height="69" />

1. Your choice of a production server is obviously up to you, but we highly recommend using [Digital Ocean](https://www.digitalocean.com/). It provides a dead-simple and affordable VPS setup with out-of-the-box WordPress support. Follow the instructions on the website and create a droplet. Our default image includes an Ubuntu distro along with the latest version of Wordpress (under **Applications** tab within the *Select Image* section.![digitalocean-droplet](https://cloud.githubusercontent.com/assets/794809/7400011/d6ad02d6-ee87-11e4-8360-e959279123d1.png)

2. Now that your production VPS is bootstrapped, use the `sync` script to quickly pull down the contents of your WordPress-ready server:
Invoke the script
- ./scripts/sync

, grab the `wp-config.php` file that was created by Digital Ocean on the server. Invoke the `getwpconfig` script and plug in 
