SSH: Информация о системе

Этот набор скриптов предназначен для отображения полезной информации о системе при подключении по SSH. Скрипты автоматически выводят данные о системе, такие как имя хоста, операционная система, версия ядра, IP-адреса, текущий пользователь, а также состояние системы: время работы, нагрузка на процессор, использование памяти и дисков, и статус важных сервисов.

Как использовать
Скопируйте скрипты на сервер, к которому вы подключаетесь по SSH.

Добавьте вызов этих скриптов в один из файлов:

~/.bashrc

/etc/profile

/etc/update-motd.d/

Это позволит скриптам автоматически запускаться при каждом входе по SSH.

Настройте список сервисов в скрипте services.sh, чтобы отображать статус только тех сервисов, которые важны для вас.

Пример добавления в ~/.bashrc:
```bash
if [ -f /path/to/your/script.sh ]; then
    /path/to/your/script.sh
fi
```

SSH System Dashboard
These scripts are designed to display useful system information upon SSH login. They provide details about the system, such as hostname, operating system, kernel version, IP addresses, current user, as well as system status: uptime, CPU load, memory and disk usage, and the status of important services.

How to Use
Copy the scripts to the server you connect to via SSH.

Add the execution of these scripts to one of the following files:

~/.bashrc

/etc/profile

/etc/update-motd.d/

This will ensure the scripts run automatically upon each SSH login.

Configure the list of services in the services.sh script to display the status of only those services that are important to you.

Example of adding to ~/.bashrc:
```bash
if [ -f /path/to/your/script.sh ]; then
    /path/to/your/script.sh
fi
```
Дополнительные советы

Для /etc/update-motd.d/:
Если вы используете /etc/update-motd.d/, убедитесь, что скрипты имеют права на выполнение:

```bash
chmod +x /etc/update-motd.d/your_script.sh
```
Кастомизация:
Вы можете легко изменить цвета, формат вывода или добавить новые данные, отредактировав скрипты под свои нужды.
