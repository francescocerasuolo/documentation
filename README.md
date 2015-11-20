# Urban TEP platform Documentation

This is the official repository of Tep Urban platform's Documentation. This
documentation is live at:
[http://urban-tep.github.io/documentation](http://urban-tep.github.io/documentation).

You are encouraged to fork this repo and send us pull requests!

## Getting started

Here's the procedure to install the required packages on a CentOS 6.x

```
sudo yum install python-sphinx
sudo yum install python-pip
pip install sphinx_bootstrap_theme
git clone https://github.com/urban-tep/documentation.git
```

If needed, set your github information

```
git config --global user.name <github username>
git config --global user.email <email address>
```

## Building

Build the documentation by running ``make html``.

## Publish the documentation

``make html`` creates a ``build`` folder in the documentation local repository.

As root, do:

```
cd /var/www/html
ln -s /home/fbrito/documentation/build/html/ doc-tep-urban
chown apache:apache data-tep-urban
```
> Replace /home/fbrito with the path to the folder where you have cloned the repository

Open you browser at the address http://127.0.0.1/doc-tep-urban

## This documentation is built with sphinx-doc

[More information](http://sphinx-doc.org/).
