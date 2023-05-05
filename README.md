# devops-netology
Будут проигнорированы следующие файлы:

*.tfstate
*.tfstate.*

Файлы аварийного лога
crash.log
crash.*.log

Файлы с паролями, ключами итп пользователей
*.tfvars
*.tfvars.json

Файлы перенаправления ресурсов
override.tf
override.tf.json
*_override.tf
*_override.tf.json

Файлы конфигурации командной строки
.terraformrc
terraform.rc
