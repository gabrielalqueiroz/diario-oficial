# Processing Flow

TODO: Describe processing flow

### Daniel

### Elthon
```
git clone https://github.com/gabrielalqueiroz/diario-oficial.git
cd diario-oficial/
git status
    On branch master
    Your branch is up-to-date with 'origin/master'.
    nothing to commit, working directory clean
sudo apt-get install docker
sudo apt-get install docker-compose
    //versão 1.8.0 instalada
    //deu erro ao executar 'make setup' >> ERROR: Version in "./docker-compose.yml" is unsupported.
    //troquei pela versão 1.20.0 com os comnado a seguir
sudo rm /usr/bin/docker-compose
sudo curl -L https://github.com/docker/compose/releases/download/1.20.0/docker-compose-`uname -s`-`uname -m` -o /usr/bin/docker-compose
    //deu erro ao executar 'make setup' de novo >> make: execvp: docker-compose: Permission denied
    //após várias leituras, descobri q era necessário executar o código abaixo
sudo chmod +x /usr/bin/docker-compose 
    //novo erro >> ERROR: Couldn't connect to Docker daemon at http+docker://localhost - is it running?
    //resolvi adicionando meu usuário ao grupo docker. aparentemente tudo era uma questão de permissão de leitura/escrita
sudo usermod -aG docker $USER
make setup
docker-compose up
```
### Gabriela

