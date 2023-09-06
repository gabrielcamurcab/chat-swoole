# chat-swoole

## Descrição do projeto
Este é projeto de estudo utilizando o **Swoole**(uma extensão para PHP que permite a programação assíncrona e de alto desempenho). 
Este é meu primeiro projeto usando essa extensão, e achei simplesmente genial!

O código base, que me deu o norte para o iniciar, está [aqui](https://blog.4linux.com.br/criando-um-chat-utilizando-php-e-swoole/).

## Como rodar o projeto?

### Requisitos
- **Sistema Operacional:** Linux, FreeBSD ou MacOS
- **Versão do PHP:** >=5.4
- **Versãoo do Kernel do Linux:** >= 2.3.32


### Instalação do ambiente
Para instalar o Swoole, você precisa ter o **PECL instalado em sua máquina**.
Aqui trago o passo a passo de instalação no Linux, que é o meu ambiente:

- Instale o php-pear: `sudo apt-get install php-pear`
- Instale o php-dev: `sudo apt-get install php-dev`

Após isso, você precisa:

- Instalar o Swoole: `pecl install swoole`
- Adicionar ele no php.ini:
```
php -i | grep php.ini # Aqui você verifica o caminho do php.ini
sudo echo "extension=swoole.so" > php.ini # Inclui a extensão no arquivo
php -m | grep swoole # Verifica se foi adicinada com sucesso
```
### Clonagem e execução do projeto
Agora vem a parte mais simples. A implementação do projeto em seu ambiente local:

```
git clone https://github.com/gabrielcamurcab/chat-swoole
composer install
php server.php
```

Você verá a mensagem:

`WebSocket Server is listening on 0.0.0.0:8081`

Ela indica que o seu WebSocket está rodando. Além disso, todas as mensagens de log serão exibidas.
Para testar, abra o `test.html` em diferentes navegadores, e envie suas mensagens.

Divirtam-se!
