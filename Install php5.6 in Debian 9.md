

Install-php5.6-in-Debian-9

Open the terminal and run the following command:

apt-get install apt-transport-https lsb-release ca-certificates

Get the gpg key:

wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg

or:

curl https://packages.sury.org/php/apt.gpg | apt-key add -

Add the new repository to your sources:

echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list

Install PHP5.6

apt-get update apt-get install php5.6

To switch between PHP versions:

update-alternatives --config php

Sample output:

    0 /usr/bin/php7.0 70 mode automatique 1 /usr/bin/php5.6 56 mode manuel 2 /usr/bin/php7.0 70 mode manuel
