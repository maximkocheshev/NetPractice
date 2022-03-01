IP-адрес – это уникальный адрес, идентифицирующий устройство в интернете или локальной сети.

An IP address is a unique address that identifies a device on the Internet or a local network.

Маска сети - это 32-разрядная двоичная маска, используемая для разделения IP-адреса на подсети и указания доступных узлов сети.

выполнение побитовой логической операции и над IP-адресом с маской подсети создает сетевой адрес.

A subnet mask is a 32-bit number created by setting host bits to all 0s and setting network bits to all 1s. In this way, the subnet mask separates the IP address into the network and host addresses.

IP:   1101 1000 . 0000 0011 . 1000 0000 . 0000 1100  (216.003.128.012)

Mask: 1111 1111 . 1111 1111 . 1111 1111 . 0000 0000  (255.255.255.000)

      ---------------------------------------------

      1101 1000 . 0000 0011 . 1000 0000 . 0000 0000  (216.003.128.000) - Сетевой адрес
      
Процесс разделения сети как минимум на две отдельные сети называется подсетью

маршрутизаторы — это устройства, которые позволяют обмениваться трафиком между подсетями, выступая в качестве физической границы.

The process of dividing a network into at least two separate networks is called a subnet, and routers are devices that allow traffic to be exchanged between subnets, acting as a physical boundary.

Сетевой адрес и широковещательный адрес не используются в качестве IP-адресов компьютеров. В Сети первое поле адреса зарезервировано для сети, а последнее-для широковещательного адреса. В поле между этими двумя адресами находятся адреса хостов сети.

The network address and broadcast address are not used as computer IP addresses. In the Network, the first address field is reserved for the network, and the last field is reserved for the broadcast address. The field between these two addresses contains the addresses of the hosts on the network.

Широковещательный адрес это специальный адрес, который, если устройство отправляет пакет на этот адрес, может получить его любое устройство.

A broadcast address is an IP address that is used to target all systems on a specific subnet network instead of single hosts. In other words broadcast address allows information to be sent to all machines on a given subnet rather than to a specific machine.

Широковещательные рассылки используются для обнаружения устройств, например, устройство, подключающееся к WiFi, обычно отправляет DHCP-запрос на широковещательный адрес.

Коммутатор (switch) - устройство для соединения нескольких устройств в одной сети. У всех устройств одинаковая маска.

https://www.javatpoint.com/switch-vs-router

Таблица маршрутизации - электронная база данных в маршрутизаторе, которая представляет из себя некий набор правил. В ней содержится информация о сетевых маршрутах по которым определяется наилучший путь для передачи пакета данных. Она содержит в себе адрес и маску сети подключения, адрес шлюза (т. е. маршрутизатора сети, на который отправляются данные), метрику (расстояние) и интерфейс (имя и индентификатор устройства).

In computer networking, a routing table, or routing information base (RIB), is a data table stored in a router or a network host that lists the routes to particular network destinations, and in some cases, metrics (distances) associated with those routes. The routing table contains information about the topology of the network immediately around it.

Общедоступный IP-адрес Это публичные (глобальные) адреса, которые используются в Интернете. Общедоступный IP-адрес — это IP-адрес, который используется для доступа в Интернет. Общедоступные IP-адреса могут маршрутизироваться в Интернете, в отличие от частных адресов. 

Частные (внутренние) адреса не маршрутизируются в Интернете, и на них не может быть направлен трафик из Интернета; они должны работать только в локальной сети.

Private IP Address and Public IP Address are used to uniquely identify a machine on the internet. Private IP address is used with a local network and public IP address is used outside the network. Public IP address is provided by ISP, Internet Service Provider.

Система доменных имен (DNS) — это служба Интернета, которая преобразует доменные имена (например, its.umich.edu) в IP-адреса.

Протокол динамической конфигурации хоста (DHCP) — это протокол для автоматического назначения IP-адресов и других конфигураций устройствам при их подключении к сети. 

Domain Name System (DNS) is an Internet service that translates domain names (e.g., its.umich.edu) into IP addresses. Dynamic Host Configuration Protocol (DHCP) is a protocol for automatically assigning IP addresses and other configurations to devices when they connect to a network.

Разница между моделью TCP/IP и моделью OSI
https://community.fs.com/ru/blog/tcpip-vs-osi-whats-the-difference-between-the-two-models.html

TCP И UDP – В ЧЕМ РАЗНИЦА?
https://wiki.merionet.ru/seti/23/tcp-i-udp-v-chem-raznica/

Перед выполнением заданий не забываем главного:

Последний IP-адрес подсети - широковещательный
Первый IP-адрес подсети - адрес сети
IP-адреса 10.0.0.0-10.255.255.255, 172.16.0.0-172.31.255.255 и от 192.168.0.0 до 192.168.255.255 зарезервированы для частных адресов, диапазон 127.0.0.1-127.255.255.254 зарезервирован для коммуникации с самим собой, остальные-для публичных IP-адресов
В таблице маршрутизации default или 0.0.0.0/0 соответствуют всему
У роутера для каждой подсети своя маска

Last Subnet IP Address - Broadcast
The first subnet IP address is the network address
IP addresses 10.0.0.0-10.255.255.255, 172.16.0.0-172.31.255.255 and 192.168.0.0 to 192.168.255.255 are reserved for private addresses, the range 127.0.0.1-127.255.255.25 is reserved for communication with itself public IP addresses
In the routing table, default or 0.0.0.0/0 matches everything
The router has a different mask for each subnet.

