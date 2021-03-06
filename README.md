# Vagrant Examples

## What is Vagrant?

Vagrant is a tool that uses Oracle's VirtualBox to dynamically build configurable, lightweight, and portable virtual machines. Vagrant supports the use of either Puppet or Chef for managing the configuration. Much more information is available on the [Vagrant web site](http://www.vagrantup.com).

## What is this project?

This is a collection of sample Vagrant configurations using Puppet. They start out very simple with the bare minimum and gradually get more complex. The examples use Ubuntu 14.04 64 bit, though they should work with any Debian-based Linux distribution. Other distros such as Fedora and SUSE could be supported with some Facter logic in the manifests to ensure that platform-specific packages are installed correctly (e.g. httpd vs apache2).

## How do I install Vagrant?

The host OS used in testing these examples was Ubuntu Trusty64, but any OS should work as long as VirtualBox can be installed. Download Vagrant from this source https://www.vagrantup.com/downloads.html

## How do I run the examples?

From one of the example directories, type the following commands...

```
vagrant init ubuntu/trusty64
vagrant up

vagrant ssh 
   username: vagrant, password: vagrant

vagrant destroy
```

These commands will bring up the Vagrant box, SSH into it, and then remove it respectively.

## Summary of examples

1. Single box with some custom configuration.
2. Single box with VirtualBox provider.
3. Single box with VirtualBox provider and Puppet provisioning.
4. Single box with Apache and sample static site installed via Puppet.
5. Separate Web and database servers serving up static/dynamic sites via Puppet.
6. Pulling out all the stops with cluster of seven Vagrant boxes.
7. Single box with AWS provider and sample static/dynamic sites via Puppet.
