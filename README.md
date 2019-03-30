Primeiro tem que instalar o composer: https://getcomposer.org/download/, é so clicar "Composer-Setup.exe "

depois de descompactar na pasta do servidor, entra na pasta do projeto e executa os seguinte comando e ajuste abaixo:

##################
## Configurando ##
##################

1- Rodar comando "composer install"

2- Configurando o .env

    1- Renomeie o arquivo "env.example" para ".env"
    2- Setar a url do projeto na chave "APP_URL" (exemplo abaixo)

        APP_URL=http://localhost:8000

    3- Setar as configurações de conexão com a base de dados (exemplo abaixo)

        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=sigres
        DB_USERNAME=root
        DB_PASSWORD=

3- Rodar comando "php artisan migrate"

4- Rodar comando "php artisan key:generate"

5- Rodar comando "php artisan passport:install"

6- Rodar comando "php artisan passport:keys"

7- Rodar comando "php artisan db:seed --class=DatabaseSeeder"


# comando para executar o test
vendor\bin\phpunit --configuration phpunit.xml
