# Configurar la red en linux manualmente

1. Iniciamos una terminal y en ella ingresamos y editamos el archivo con permisos de superusuario.

`sudo nano /etc/network/interfaces`

2. En el caso de una red Ethernet (Cableada) DHCP (Diámica) se configura.

`auto eth0`
`iface eth0 inet dhcp`

### Donde `eth0` es la interfaz de red, para ver tu interfaz de red escribe en la terminal `sudo ifconfig` o `iwconfig`.

3. En el caso de una red Ethernet (Cableada) Estática se configura.

`auto eth0
iface eth0 inet static
address 192.168.1.145 (IP)
netmask 255.255.255.0 (Máscara de red)
network 192.168.1.0 (Red)
broadcast 192.168.1.255
gateway 192.168.1.1` (Puerta de enlace)

4. En el caso de una red WiFi (Inalámbrica) DHCP (Dinámica).

`iface wlp2s0 inet dhcp`  

`wpa-essid "Jazztel_XXXX"` (Nombre de red)  

`wpa-psk "enCaPylSaPeB4hY6m"` (Contraseña WiFi)

5. En el caso de una red WiFi (Inalámbrica) Estática.

### Básicamente coge los valores de red (IPs y demás) y se les añaden junto con el nombre de red y su contraseña, un ejemplo:

`iface wlp2s0 inet static`  

`wpa-essid "Jazztel_XXXX"` (Nombre de red)  

`wpa-psk "enCaPylSaPeB4hY6m"` (Contraseña WiFi)  

`address 192.168.1.145` (IP)  

`netmask 255.255.255.0` (Máscara de red)  

`network 192.168.1.0` (Red)  

`broadcast 192.168.1.255`  

`gateway 192.168.1.1` (Puerta de enlace)
