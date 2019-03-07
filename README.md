# ElementaryOSJuno_Perfeito
Elementary OS Juno Perfeito 

1 - Atualizar o update & upgrade
```shell
sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade
```

2 - Install File Compression Libs
```shell
sudo apt-get install unace unrar zip unzip xz-utils p7zip-full p7zip-rar sharutils rar uudeview mpack arj cabextract file-roller -y
```

3 - Habilitar o Add Apt Repository
```shell
sudo apt-get install -y software-properties-common
```
# Install LAMP
Instalação do Apps Linux, Apache2, MySql e PHP

1 - Install Apache2
```shell
sudo apt-get install apache2
```
2 - Install PHP 5.6 7.0 e 7.1
```shell
sudo apt install python-software-properties
sudo add-apt-repository ppa:ondrej/php
```

Depois atualize o sistema
```shell
sudo apt-get update
```

Instale as versões do PHP
```shell
sudo apt install php5.6 && sudo apt install php7.0 && sudo apt install php7.1
```

Instale o PHP fpm
```shell
sudo apt install php5.6-fpm && sudo apt install php7.0-fpm && sudo apt install php7.1-fpm
```

Instale o PHP cli, xml, mysql
```shell
sudo apt install php5.6-cli php5.6-xml php5.6-mysql
sudo apt install php7.0-cli php7.0-xml php7.0-mysql
sudo apt install php7.1-cli php7.1-xml php7.1-mysql
```

Alternar as versões do PHP
PHP 5.6
```shell
sudo update-alternatives --set php /usr/bin/php5.6
```

PHP 7.0
```shell
sudo update-alternatives --set php /usr/bin/php7.0
```

PHP 7.1
```shell
sudo update-alternatives --set php /usr/bin/php7.1
```
