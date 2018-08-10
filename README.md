# Config-GNU-Linux

# SCRIP DE INSTALAÇÃO DOS PROGRAMAS PADRÕES UBUNTU 16.04LTS                                                                                                     

ANTES DE TUDO:                                                                                                                                                

Abra a opção “Programas e atualizações” de “Configurações do sistema” do Unity e marque os repositórios “Parceiros da Canonical” na guia “Outros programas”;

1. UNITY TWEAK-TOLL(FERRAMENTA DE CONFIGURAÇÃO DO AMBIENTE UNITY)

sudo apt install unity-tweak-tool


2. FLASH PLAYER

sudo sh -c "echo 'deb http://archive.canonical.com/ubuntu $(lsb_release -cs) partner' >> /etc/apt/sources.list"

sudo apt install adobe-flashplugin


3. JAVA

sudo add-apt-repository ppa:webupd8team/java

sudo apt-get update

sudo apt-get install oracle-java8-installer


4. CODECS MULTIMÍDIA

sudo apt install ubuntu-restricted-extras libavcodec-extra


5. VLC

sudo apt install vlc


6. LIBRE OFFICE

Antes de tudo desinstale a versão mais antiga do LibreOffice

sudo apt-get remove --purge libreoffice*

Depois digite os seguintes comandos:

wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb.tar.gz -O libreOffice.tar.gz

wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb_langpack_pt-BR.tar.gz -O libreOffice-pt-br.tar.gz

tar -vzxf libreOffice.tar.gz

tar -vzxf libreOffice-pt-br.tar.gz

cd LibreOffice_*

cd DEBS

sudo dpkg -i *.deb 

cd LibreOffice*langpack_pt-BR/

cd DEBS

sudo dpkg -i *.deb


7. EDITOR VS CODE(EDITOR OPEN-SOURCE DA MICROSOFT)

sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg

sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg

sudo apt-get update

sudo apt-get install code


8. LAMP SERVER

sudo apt-get install lamp-server^


9. PHPMYADMIN

sudo apt-get install phpmyadmin

criando a pasta para teste do PHP INFO

echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/test.php

sudo /etc/init.d/apache2 restart

http://localhost/test.php


10. KODI

sudo add-apt-repository ppa:team-xbmc/ppa

sudo apt update

sudo apt install kodi-pvr-mythtV


11. TIMESHIFT (CRIA SNAPSHOTS DO SISTEMA – FERRAMENTA DE BACKUP)

sudo add-apt-repository ppa:teejee2008/ppa

sudo apt-get update

sudo apt-get install timeshift
