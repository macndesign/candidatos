Site candidatos
===============

Fazendo para as eleições.



Config Vagrant (Ubuntu 12.04 32b)
---------------------------------

    $ vagrant init hashicorp/precise32
    $ vagrant up
    $ vagrant ssh



Install Ubuntu packages
-----------------------

    sudo apt-get -y install python-setuptools fabric libpq-dev python-dev python-psycopg2 python-crypto build-essential libssl-dev libffi-dev libjpeg-dev libfreetype6 libfreetype6-dev zlib1g-dev python-imaging rabbitmq-server wkhtmltopdf python-celery git vim



Install requirements
--------------------

    wget https://raw.github.com/pypa/pip/master/contrib/get-pip.py && sudo python get-pip.py  && sudo pip install -r /vagrant/requirements.txt



Add keygen
----------

    # If not has id_rsa:
    $ ls -al ~/.ssh/

    # Then generate:
    $ ssh-keygen -t rsa -C "macndesign@gmail.com"

    # Select the id_rsa.pub content to clipboard:
    $ cat ~/.ssh/id_rsa.pub

    # Access the follow page: https://github.com/settings/ssh. Then add the key.
    # Check if it works!
    $ ssh -T git@github.com
