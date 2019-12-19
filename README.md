# SCRIPT DE CONFIGURAÇÃO SISTEMA UBUNTU/LINUX

## SCRIP DE INSTALAÇÃO DOS PROGRAMAS PADRÕES UBUNTU 18.04LTS                                                                                                     
ANTES DE TUDO:                                                                                                                                                
Abra a opção “Programas e atualizações” de “Configurações do sistema” do GNOME e marque os repositórios “Parceiros da Canonical” na guia “Outros programas”;

#### 1. UNITY TWEAK-TOLL(FERRAMENTA DE CONFIGURAÇÃO DO AMBIENTE UNITY)

```console
$ sudo apt install gnome-tweak-tool
```

#### 2. FLASH PLAYER
```console
$ sudo sh -c "echo 'deb http://archive.canonical.com/ubuntu $(lsb_release -cs) partner' >> /etc/apt/sources.list"
```
```console
$ sudo apt install adobe-flashplugin
```

#### 3. JAVA
Para instalação do JAVA execute os camandos listados abaixo:
```console
sudo apt-get purge openjdk*
```

```console
$ sudo add-apt-repository ppa:webupd8team/java
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install oracle-java8-installer
```

```console
sudo apt-get install oracle-java8-set-default
```

#### 4. CODECS MULTIMÍDIA
```console
$ sudo apt install ubuntu-restricted-extras libavcodec-extra
```

#### 5. VLC
```console
$ sudo apt install vlc
```

#### 6. LIBRE OFFICE

Antes de tudo desinstale a versão mais antiga do LibreOffice
```console
$ sudo apt-get remove --purge libreoffice*
```

Depois digite os seguintes comandos:
```console
$ wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb.tar.gz -O libreOffice.tar.gz
```

```console
$ wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb_langpack_pt-BR.tar.gz -O libreOffice-pt-br.tar.gz
```

```console
$ tar -vzxf libreOffice.tar.gz
```

```console
$ tar -vzxf libreOffice-pt-br.tar.gz
```

```console
$ cd LibreOffice_*
```

```console
$ cd DEBS
```

```console
$ sudo dpkg -i *.deb 
```

```console
$ cd LibreOffice*langpack_pt-BR/
```

```console
$ cd DEBS
```

```console
$ sudo dpkg -i *.deb
```

#### 7. EDITOR VS CODE(EDITOR OPEN-SOURCE DA MICROSOFT)
```console
$ sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

```console
$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
```

```console
$ sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install code
```

#### 8. LAMP SERVER
```console
$ sudo apt-get install lamp-server^
```

#### 9. PHPMYADMIN
```console
$ sudo apt-get install phpmyadmin
```

```console
$ criando a pasta para teste do PHP INFO
```

```console
$ echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/test.php
```

```console
$ sudo /etc/init.d/apache2 restart
```

```console
$ http://localhost/test.php
```

#### 10. KODI
```console
$ sudo add-apt-repository ppa:team-xbmc/ppa
```

```console
$ sudo apt update
```

```console
$ sudo apt install kodi-pvr-mythtV
```

#### 11. TIMESHIFT (CRIA SNAPSHOTS DO SISTEMA – FERRAMENTA DE BACKUP)
```console
$ sudo add-apt-repository ppa:teejee2008/ppa
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install timeshift
```

#### 12. ALIAS MODIFICADAS PARA MELHORAR NA DIGITAÇÃO DOS CÓDIGOS

Alias modificadas por [Diógenes Dantas](https://github.com/Doginnn "GitHub - Doginnn")

Este arquivo contém algumas Alias modificadas para agilizar alguns processos no BASH.

#### Passo á passo para modificar o seu BASH:
- 1º Navegue até a pasta pessoal e abra seu editor de código favorito como super usuário.

    (No meu caso utilizo o [VSCode](https://code.visualstudio.com/ "Visual Estúdio Code"));
    
```console
$ sudo code .
```
- 2º Aperte em "Add Folder" para adicionar uma nova pasta ao Workspace;
- 3º Aperte as Ctrl + h para aparecer os arquivos ocultos;
- 4º Adicione toda a sua "Pasta Pessoal" no workspace;
- 5º Procure e abra o arquivo "bash.rc";
- 6º Copie e cole todo esse código abaixo na última linha do "bash.rc", salve, feche o editor depois abra novamente;

```console
# Alias modificadas para atualização.
alias upd='sudo apt update'
alias upg='sudo apt upgrade'
alias autoremove='sudo apt autoremove'

# Alias modificadas para testes de net.
alias google='ping 8.8.8.8'
alias 1111='ping 1.1.1.1'
alias 4444='ping 4.4.4.4'

#Comandos para diretórios.
alias raiz='cd ../../..'

# Alias modificadas para GitHub
alias init='git init'
alias clone='git clone'
alias show='git show'
alias status='git status'
alias add='git add'
alias commit='git commit'
alias branch='git branch'
alias merge='git merge'
alias pull='git pull'
alias push='git push'
```

- 7º Depois disso seu novo terminal já deve está funcionando com as ALIASES que você configurou.


# SCRIP DE INSTALAÇÃO DOS PROGRAMAS PADRÕES UBUNTU 16.04LTS                                                                                                     
ANTES DE TUDO:                                                                                                                                                
Abra a opção “Programas e atualizações” de “Configurações do sistema” do Unity e marque os repositórios “Parceiros da Canonical” na guia “Outros programas”;

#### 1. UNITY TWEAK-TOLL(FERRAMENTA DE CONFIGURAÇÃO DO AMBIENTE UNITY)

```console
$ sudo apt install unity-tweak-tool
```

#### 2. FLASH PLAYER
```console
$ sudo sh -c "echo 'deb http://archive.canonical.com/ubuntu $(lsb_release -cs) partner' >> /etc/apt/sources.list"
```
```console
$ sudo apt install adobe-flashplugin
```

#### 3. JAVA
```console
$ sudo add-apt-repository ppa:webupd8team/java
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install oracle-java8-installer
```

```console
sudo apt-get install oracle-java8-set-default
```

#### 4. CODECS MULTIMÍDIA
```console
$ sudo apt install ubuntu-restricted-extras libavcodec-extra
```

#### 5. VLC
```console
$ sudo apt install vlc
```

#### 6. LIBRE OFFICE

Antes de tudo desinstale a versão mais antiga do LibreOffice
```console
$ sudo apt-get remove --purge libreoffice*
```

Depois digite os seguintes comandos:
```console
$ wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb.tar.gz -O libreOffice.tar.gz
```

```console
$ wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.0.6/deb/x86_64/LibreOffice_6.0.6_Linux_x86-64_deb_langpack_pt-BR.tar.gz -O libreOffice-pt-br.tar.gz
```

```console
$ tar -vzxf libreOffice.tar.gz
```

```console
$ tar -vzxf libreOffice-pt-br.tar.gz
```

```console
$ cd LibreOffice_*
```

```console
$ cd DEBS
```

```console
$ sudo dpkg -i *.deb 
```

```console
$ cd LibreOffice*langpack_pt-BR/
```

```console
$ cd DEBS
```

```console
$ sudo dpkg -i *.deb
```

#### 7. EDITOR VS CODE(EDITOR OPEN-SOURCE DA MICROSOFT)
```console
$ sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

```console
$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
```

```console
$ sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install code
```

#### 8. LAMP SERVER
```console
$ sudo apt-get install lamp-server^
```

#### 9. PHPMYADMIN
```console
$ sudo apt-get install phpmyadmin
```

```console
$ criando a pasta para teste do PHP INFO
```

```console
$ echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/test.php
```

```console
$ sudo /etc/init.d/apache2 restart
```

```console
$ http://localhost/test.php
```

#### 10. KODI
```console
$ sudo add-apt-repository ppa:team-xbmc/ppa
```

```console
$ sudo apt update
```

```console
$ sudo apt install kodi-pvr-mythtV
```

#### 11. TIMESHIFT (CRIA SNAPSHOTS DO SISTEMA – FERRAMENTA DE BACKUP)
```console
$ sudo add-apt-repository ppa:teejee2008/ppa
```

```console
$ sudo apt-get update
```

```console
$ sudo apt-get install timeshift
```

#### 12. ALIAS MODIFICADAS PARA MELHORAR NA DIGITAÇÃO DOS CÓDIGOS

Alias modificadas por [Diógenes Dantas](https://github.com/Doginnn "GitHub - Doginnn")

Este arquivo contém algumas Alias modificadas para agilizar alguns processos no BASH.

#### Passo á passo para modificar o seu BASH:
- 1º Navegue até a pasta pessoal e abra seu editor de código favorito como super usuário.

    (No meu caso utilizo o [VSCode](https://code.visualstudio.com/ "Visual Estúdio Code"));
    
```console
$ sudo code .
```
- 2º Aperte em "Add Folder" para adicionar uma nova pasta ao Workspace;
- 3º Aperte as Ctrl + h para aparecer os arquivos ocultos;
- 4º Adicione toda a sua "Pasta Pessoal" no workspace;
- 5º Procure e abra o arquivo "bash.rc";
- 6º Copie e cole todo esse código abaixo na última linha do "bash.rc", salve, feche o editor depois abra novamente;

```console
# Alias modificadas para atualização.
alias upd='sudo apt update'
alias upg='sudo apt upgrade'
alias autoremove='sudo apt autoremove'

# Alias modificadas para testes de net.
alias google='ping 8.8.8.8'
alias 1111='ping 1.1.1.1'
alias 4444='ping 4.4.4.4'

#Comandos para diretórios.
alias raiz='cd ../../..'

# Alias modificadas para GitHub
alias init='git init'
alias clone='git clone'
alias show='git show'
alias status='git status'
alias add='git add'
alias commit='git commit'
alias branch='git branch'
alias merge='git merge'
alias pull='git pull'
alias push='git push'
```

- 7º Depois disso seu novo terminal já deve está funcionando com as ALIASES que você configurou.