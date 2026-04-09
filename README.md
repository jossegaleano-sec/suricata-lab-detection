#  Suricata IDS/IPS Lab - Network Threat Detection

Este laboratorio documenta la implementación de un sistema de detección de intrusos (Suricata) para monitorear y alertar sobre actividades sospechosas en una red privada, específicamente escaneos de puertos y ataques al servicio SMB.

##  1. Configuración del Entorno
Se utilizó VirtualBox para crear un entorno aislado con una red **Host-Only**.

* **Atacante:** Kali Linux (192.168.56.101)
* **Víctima:** Windows 10 (192.168.56.102)

![Configuración de Red](./configuracion%20de%20red.jpeg)

##  2. Preparación y Reglas de IDS
Se configuró Suricata con reglas personalizadas en "local.rules" para detectar tráfico ICMP (ping) y escaneos de puertos TCP. Para asegurar la detección, se desactivó temporalmente el firewall en la máquina víctima.

![Reglas IDS](./normas%20locales:%20mis%20reglas%20ids.jpeg)
![Firewall Desactivado](./desactivacion%20w.defender%20en%20victima.jpeg)

##  3. Fase de Reconocimiento
Se realizó un escaneo con **Nmap** desde la máquina atacante para identificar servicios vulnerables, detectando los puertos 135, 139 y 445 (SMB) abiertos.

![Escaneo Nmap](./ataque%20nmap%20desde%20atacante%20kali.jpeg)

##  4. Explotación y Detección
Se procedió a realizar un acceso mediante "smbclient". El IDS Suricata generó alertas en tiempo real, identificando tanto el escaneo previo como la sesión NTLM establecida.

![Ataque SMB](./Ataque%20SMBclient%20desde%20MV%20atacante%20kali.jpeg)
![Alertas Suricata](./muestra%20alertas%20suricata%20ids.jpeg)

## 5. Análisis de Resultados (SOC)
El log "fast.log" muestra la cronología completa del ataque, desde el primer ping de reconocimiento hasta el acceso administrativo.

![Log Final](./muestra%20alerta%20ingreso%20a%20admin%20en%20w10%20victima.jpeg)
