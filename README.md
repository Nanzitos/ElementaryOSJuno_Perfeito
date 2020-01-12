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
Instalação do Apps Linux, Apache2, MySql e PHP.
Durante a instalação utilizaremos com frequencia o editor de texto no meu caso eu prefiro o vim, para instalar utilize o comando abaixo:

```shell
sudo apt install vim
```


1 - Install Apache2
```shell
sudo apt-get install apache2
```
2 - Install PHP 5.6 7.0 e 7.1
```shell
sudo apt install python-software-properties || sudo apt-get install software-properties-common
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

Para selecionar a versão do PHP que irá trabalhar com o Apache, primeiro desabilite a versão atual com o comando a2dismod e depois habilite a versão que precisa com o comando a2enmod:
```shell
sudo a2dismod php7.0
sudo a2enmod php7.1
```

Para validar se o php esta funcionando crie o arquivo info.php na pasta /var/www/html, em seguida digite o código abaixo para exibir as infos do php no seu navegador em: http://localhost/info.php

```shell
<?php phpinfo(); ?>
```

3 - Instalando o MySql 

Instalando o MySql e suas dependencias 
```shell
sudo apt-get update
sudo apt-get install mysql-server
```
Liberando o acesso remoto
```shell
sudo ufw allow mysql
```
Pode ser que o mysql não permita que o root acesso ao banco dado pelo phpmyadmin, para resolver isso utilize o comando abaixo que irá configurar uma senha para que o root possa acesso ao banco de dados 

```shell
sudo mysql -u root
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'sua_senha'; 
```
4 - Instalando o PhpMyAdmin

Atualize o sistema 
```shell
sudo apt-get update
```

Instale o phpmyadmin
```shell 
sudo apt-get install phpmyadmin -y
```

Após a instalação do phpmyadmin, para acessa ló nos precisamos criar um link symbolic no sistema para pode acessar o link pelo navegador web pelo link http://localhost/phpmyadmin utilize o código abaixo para criar o link symbolic. Vale apena lembrar que para o link funcionar ele precisa ser criado dentro do diretório html em: /var/www/html

```shell 
 sudo ln -s /usr/share/phpmyadmin/ /var/www/html/phpmyadmin 
```



Instalando o mcrypt
```shell
sudo apt-get install php5.6 mcrypt && sudo apt-get install php7.0 mcrypt && sudo apt-get install php7.1 mcrypt 
```

Intalando Mbstring
```shell
sudo apt-get install php5.6-mbstring && sudo apt-get install php7.0-mbstring && sudo apt-get install php7.1-mbstring 
```

Reiniciando o apache
```shell
systemctl restart apache2
```

5 - Instalando o Git 

Instalando o pacote git completo
```shell
sudo apt install git
```

6 - Instalando o Gparted

Instalando o pacote Gparted 
```shell
sudo apt install gparted
```

## Removendo Apps

Remoendo o navegador Epiphany
```shell
sudo apt-get remove epiphany-browser*
```
