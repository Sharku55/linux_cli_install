## Part 1. Установка ОС

- Узнайте версию Ubuntu, выполнив команду cat /etc/issue.

![](q1_issue.png)

## Part 2. Создание пользователя

- Вызов команды для создания пользователя.

![](q2_user_add.png)

- Вызов команды для просмотра пользователей.

![](q2_passwd.png)

## Part 3. Настройка сети ОС

- Новое имя машины.

![](q3_hostname.png)

- Установка временной зоны.

![](q3_time_zone.png)

- Вывод названий сетевых интерфейсов.

![](q3_ifconfig.png)

> Lo (loopback device) – виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес 127.0.0.1.

> DHCP - Dynamic Host Configuration Protocol
- Вывод IP - адреса устройства.

![](q3_ip.png)

- Вывод внешнего и внутреннего IP-адреса шлюза.

![](q3_externalip.png)

![](q3_internalip.png)

- Задание статичных настроек ip, gw, dns.

![](q3_parametrs.png)

- После перезагрузки.

![](q3_parametrs-restart.png)

- Пропинговка хостов.

![](q3_ping.png)

## Part 4. Обновление ОС

- Проверка отсутствия обновлений.

![](q4_upgrade.png)

## Part 5. Использование команды **sudo**

> Sudo — это утилита, предоставляющая привилегии root для выполнения административных операций в соответствии со своими настройками.

- Добавление пользователя в группу с привилегиями sudo.

![](q5_hostname.png)
- Изменение hostname.

## Part 6. Установка и настройка службы времени

- Вывод корректного времени.

![](q6_auto_time.png)

## Part 7. Установка и использование текстовых редакторов 

- Содержимое перед закрытием (vim)

![](q7-vim_create.png)

> Выход с сохранением: Esc, :, wq

- Содержимое перед закрытием (nano)

![](q7_nano_crate.png)

> Выход с сохранением: CTRL+0, CTRL+x

- Содержимое перед закрытием (mcedit)

![](q7_mcedit_create.png)

> Выход с сохранением: F2, F10

- Содержимое после редактирования (vim) 

![](q7_vim_change.png)

> Выход без сохранения: Esc, :, q

- Вывод файла.

![](q7_vim_res.png)

- Содержимое после редактирования (nano)

![](q7_nano_change.png)

> Выход без сохранения: CTRL+x, n

- Вывод файла.

![](q7_nano_res.png)

- Содержимое после редактирования (mcedit)

![](q7_mcedit_change.png)

> Выход без сохранения: F10

- Вывод файла.

![](q7_mcedit_res.png)

> Поиск в vim через: /

- Результат поиска (vim)

![](q7_vim_serch.png)

- Команда для замены (vim)

![](q7_vim_replace.png)

- Результат поиска (nano)

![](q7_nano_serch.png)

![](q7_nano_serch2.png)

- Команда для замены (nano)

![](q7_nano_replace.png)

![](q7_nano_replace2.png)

- Результат поиска (mcedit)

![](q7_mcedit_serch.png)

- Команда для замены (mcedit)

![](q7_mcedit_replace.png)

![](q7_mcedit_replace2.png)

![](q7_mcedit_replace3.png)

## Part 8. Установка и базовая настройка сервиса **SSHD**

- Установка SSHd (sudo apt install openssh-server).
- Добавление в автозагрузку (sudo systemctl enable sshd)
- Перенастройка SSHd на порт 2022 (sudo vim /etc/ssh/sshd_config)

![](q8_port_edit.png)

- С помощью ps -C sshd показать наличие процесса sshd.

![](q8_ps_-C.png)

> Ключ -C выбирает процесс по названию

- Вывод netstat -tan.

![](q8_netstat_-tan.png)

- -t отображает только TCP соединения
- -a вывод всех подключений
- -n вывод активных подключений TCP с отображением адресов и номеров портов в числовом формате
- Proto - название протокола (протокол TCP или протокол UDP)
- recv-Q - очередь получения сети
- send-Q - сетевая очередь отправки
- Local Address - адрес локального компьютера
- Foreign Address - адрес удаленного компьютера
- State - состояние сервера
- 0.0.0.0 - означает IP-адрес на локальной машине

## Part 9. Установка и использование утилит **top**, **htop**

- По выводу команды top определить:

![](q9_top.png)

- uptime: 0:13
- количество авторизованных пользователей: 1
- общая загрузка системы: 0,02, 0,01, 0,00
- общее кол-во процессов: 117
- загрузка CPU: 0.0
- загрузка памяти: 173.8 M
- pid процесса занимающего больше всего памяти: 713

![](q9_top_memory_max.png)

- pid процесса, занимающего больше всего процессорного времени: 1257

![](q9_top_time_max.png)

- Вывод htop, отсортированный по PID, PERCENT_CPU, PERCENT_MEM, TIME

![](q9_htop_pid.png)

![](q9_htop.png)

![](q9_htop_mem.png)

![](q9_htop_time.png)

![](q9_htop_all_sort.png)

- Вывод htop, отфильтрованный для sshd

![](q9_htop_sshd.png)

- Вывод htop с процессом syslog, найденным, используя поиск

![](q9_htop_serch_syslog.png)

- Вывод htop с добавленными hostname, clock, uptime

![](q9_htop_hostname_time_uptime.png)

## Part 10. Использование утилиты **fdisk**

- Вывод fdisk -l

![](q10_fdisc+swap.png)

![](q10_swap_check.png)

- Название: VBOX HARDDISK
- Размер: 30Gib
- Кол-во секторов: 62914560
- Размер swap: 0G

## Part 11. Использование утилиты **df** 

- Вывод df

![](q11_df.png)

- Размер раздела: 14339080
- Размер занятого пространства: 2579368
- Размер свободного пространства: 11009532
- Процент использования: 19%

- Вывод df -Th

![](q11_df_-Th.png)

- Размер раздела: 12G
- Размер занятого пространства: 14G
- Размер свободного пространства: 2.5G
- Процент использования: 19%
- Тип файловой системы: ext4

## Part 12. Использование утилиты **du**

- Вывод  du

![](q12_du.png)

- Вывод  du /home

![](q12_du_-b_home.png)

- Вывод  du /var

![](q12_du_-b_var.png)

- Вывод  du /var/log

![](q12_du_-b_var_log.png)

- Вывод  du /var/log/*

![](q12_du_-b_var_log_s.png)

## Part 13. Установка и использование утилиты **ncdu**

- Вывод ncdu /home

![](q13_ncdu.png)

- Вывод ncdu /var

![](q13_ncdu_var.png)

- Вывод ncdu /var/log

![](q13_ncdu_var_log.png)


## Part 14. Работа с системными журналами

- Просмотр /var/log/dmesg

![](q14_var_log_dmesg.png)

- Просмотр /var/log/syslog

![](q14_var_log_syslog.png)

- Просмотр /var/log/auth.log

![](q14_var_log_authlog.png)

- Последняя авторизация: Sep 5 01:18:18 hothfort by LOGIN
- Перезапуска службы SSHd

![](q14_sshd_restart.png)

![](q14_sshd_restart_check.png)

## Part 15. Использование планировщика заданий **CRON**

- Запуск задачи

![](q15_cron_add_task.png)

- Информация о выполнении

![](q15_cron_check.png)

- Список после удаления задачи

![](q15_cron_default.png)