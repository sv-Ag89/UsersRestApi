1. Создала проект Symfony: composer create-project symfony/skeleton:"6.4.*" UsersRestApi
2. Установила необходимые пакеты для REST API и авторизации:
composer require jms/serializer-bundle
composer require friendsofsymfony/rest-bundle
composer require symfony/maker-bundle    
composer require symfony/orm-pack --with-all-dependencies
composer require lexik/jwt-authentication-bundle:*
3. Настроила конфигурацию базы данных в файле .env
4. Скорректировала файл config/packages/fos_rest.yaml
5. Создала класс user: php bin/console make:user
6. Добавила новое поле nameuser в файле src\Entity\User.php
7. Создала файл миграции: php bin/console make:migration
8. Сделала перенос миграции: php bin/console doctrine:migrations:migrate
9. Сгенерировала SSL-ключи: php bin/console lexik:jwt:generate-keypair
10. Скорректировала файл config/routes.yaml
11. Создала контроллер для регистрации пользователей: php bin\console make:controller RegistrationController
12. Создала контроллер для проверки аутентификации: php bin/console make:controller DashboardController
13. Скорректировала файл config/packages/security.yaml
14. Создала контроллер для работы с пользователями: php bin/console make:controller UserController
