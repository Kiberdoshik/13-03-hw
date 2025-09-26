# Домашнее задание к занятию "`Защита сети`" - `Соседова Надежда`

### Задание 1

`Suricata зафиксировала сканирование портов с адреса 10.0.0.5. События ET SCAN указывают на попытки обнаружить службы то, что злоумышленник пытается обнаружить распространенные службы, такие как MySQL, Oracle SQL, MSSQL, PostgreSQL и т.д.
В журнале Fail2Ban события отсутствуют. Fail2ban реагирует на неудачные попытки аутентификации, чтобы заблокировать IP-адрес`

1. `Установлена Suricata.`
    ![Suricata](img/Suricata.png)
2. `Установлен Fail2Ban.`
    ![Fail2ban](img/Fail2ban.png)
3. `Развернута ВМ с Kali Linux.`
    ![Fail2ban](img/Kali.png)
4. `Запущено сканирование sudo nmap -sA 10.0.0.7`
    ![Fail2ban](img/Cканирование%20sudo%20nmap%20-sA.png)
    ![Fail2ban](img/Результаты%20сканирования%20sudo%20nmap%20-sA.png)
5. `Запущено сканирование sudo nmap -sT 10.0.0.7`
    ![Fail2ban](img/Сканирование%20sudo%20nmap%20-sT.png)
    ![Fail2ban](img/Рехзультаты%20сканирования%20sudo%20nmap%20-sT.png)
6. `Запущено сканирование sudo nmap -sS 10.0.0.7`
    ![Fail2ban](img/Сканирование%20sudo%20nmap%20-sV%2010.0.0.7.png)
    ![Fail2ban](img/Результаты%20сканирования%20sudo%20nmap%20-sS%2010.0.0.7.png)
7. `Запущено сканирование sudo nmap -sV 10.0.0.7`
    ![Fail2ban](img/Сканирование%20sudo%20nmap%20-sV%2010.0.0.7.png)
    ![Fail2ban](img/Результаты%20сканирования%20sudo%20nmap%20-sV%2010.0.0.7.png)

### Задание 2

`Fail2Ban успешно заблокировал IP-адрес атакующей машины 10.0.0.5). В логах Fail2Ban были обнаружены записи о блокировке IP-адреса. Suricata обнаружила трафик, похожий на сканер SSH, и зарегистрировала события ET SCAN Potential SSH Scan.`

1. `Произведен подбор логина и пароля при выключенном Fail2ban`
![Hydra1](img/Hydra_without%20fail2ban.png)
2. `Произведен подбор логина и пароля при включенном Fail2ban`
![Hydra2](img/Hydra_with%20fail2ban.png)
![Hydra2](img/Fail2ban_block.png)
![Hydra2](img/Suricata_log.png)
