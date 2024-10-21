<h1 align='center'>
  <img src='images/lampada.png' width='200' height='200'> 
  <br>
  Manual de Instalação e Configuração de API Node com PostgreSQL e PM2 no servidor Ubuntu Server 24.04.1 LTS

</h1>

## 📝 Sobre
  <p style="text-align: justify; text-indent: 20px;">Este manual descreve os passos para instalar e configurar uma API usando Node.js que se conecta a um banco de dados PostgreSQL, além de gerenciar o servidor da API utilizando o PM2.</p>

## ⚔ Tecnologias

- [Ubuntu Server 24.04.1 LTS](https://ubuntu.com/download/server)
- [PostgreSQL](https://www.postgresql.org/)
- [API]()
- [PM2](https://pm2.keymetrics.io/)

## 1. Passos para a Instalação

**1.1. Instalando o banco de dados PostgreSQL**
<p style="text-align: justify;text-indent: 20px;">1. Atualizando o Sistema: Abra o terminal no servidor linux e execute os seguintes comandos para atualizar o sistema:</p>

```
sudo apt update -y && sudo apt upgrade -y
```


<p style="text-align: justify; text-indent: 20px;">2.
Adicione o Repositório do PostgreSQL: Postgresql-common é um pacote que fornece utilitários comuns e arquivos de configuração para as versões do PostgreSQL. Ele não inclui o servidor PostgreSQL em si, mas fornece ferramentas e scripts úteis para a instalação e gerenciamento de várias instâncias do PostgreSQL em um sistema.</p>

```
sudo apt install -y postgresql-common
```
 <p style="text-align: justify; text-indent: 20px;">3. A seguir, adicione o repositório do PostgreSQL ao seu sistema. Isto assegurará que obterá a versão mais recente do PostgreSQL. Execute o comando seguinte:</P>

```
sudo /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh
```

<p style="text-align: justify; text-indent: 20px;">Este script adiciona o repositório APT do PostgreSQL Global Development Group (PGDG) ao seu sistema.</p>


<p style="text-align: justify; text-indent: 20px;">4. Atualize novamente o sistema.</p>

```
sudo apt update -y
```


<p style="text-align: justify; text-indent: 20px;">5. Instalando o PostgreSQL.</p>

```
sudo apt install -y postgresql
```

<p style="text-align: justify; text-indent: 20px;">Este comando instalará os pacotes adicionais necessários para o funcionamento do servidor de base de dados PostgreSQL.</p>

<p style="text-align: justify; text-indent: 20px;"> 6. Verificando o serviço PostgreSQL: </p>

```
sudo systemctl status postgresql
```
<p style="text-align: justify; text-indent: 20px;"> O comando verifica o status do serviço PostgreSQL: </p>

```
sudo systemctl start postgresql
```
<p style="text-align: justify; text-indent: 20px;"> O comando inicia o serviço PostgreSQL: </p>

```
sudo systemctl stop postgresql
```
<p style="text-align: justify; text-indent: 20px;"> O comando para o serviço PostgreSQL: </p>

<p style="text-align: justify; text-indent: 20px;">7. Configurar o serviço do PostgreSQL para iniciar automaticamente no momento da inicialização do sistema: </p>

```
sudo systemctl enable postgresql
```
