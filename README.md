# 🔐 Suricata IDS/IPS Lab – Detección de Amenazas en Red

## 📌 Descripción del Proyecto

Este laboratorio tiene como objetivo implementar y configurar un sistema de detección de intrusiones (IDS) utilizando Suricata en un entorno virtualizado, con el fin de analizar tráfico de red y detectar actividades maliciosas simuladas.

El enfoque del proyecto está orientado a tareas de Blue Team, específicamente en monitoreo de seguridad, análisis de alertas y detección de amenazas.

---

## 🎯 Objetivos

* Implementar Suricata como IDS en entorno Linux
* Analizar tráfico de red en tiempo real
* Detectar actividades maliciosas simuladas
* Configurar reglas personalizadas
* Reducir falsos positivos mediante tuning de reglas

---

## 🧪 Entorno de Laboratorio

* Virtualización: VirtualBox
* Sistema IDS: Linux (Debian/Kali)
* Máquina atacante: Kali Linux
* Herramientas utilizadas:

  * Suricata
  * Wireshark
  * tcpdump
  * Nmap

---

## 🌐 Topología de Red

[Atacante] ⇄ [Red Interna] ⇄ [IDS Suricata]

* El IDS monitorea el tráfico entre las máquinas virtuales
* Se simulan ataques desde la máquina atacante hacia el objetivo

---

## ⚔️ Escenarios Simulados

### 1. Port Scanning (Nmap)

Se realizó un escaneo de puertos utilizando Nmap para identificar servicios activos en la red.

**Resultado:**

* Detección de múltiples intentos de conexión SYN
* Generación de alertas en Suricata

---

### 2. Fuerza Bruta (Simulado)

Se generaron múltiples intentos de autenticación fallidos.

**Resultado:**

* Identificación de patrones repetitivos
* Generación de alertas por comportamiento sospechoso

---

## 🔍 Análisis de Tráfico

Se utilizó Wireshark y tcpdump para:

* Analizar paquetes TCP/IP
* Identificar handshake (SYN, SYN-ACK, ACK)
* Detectar tráfico anómalo

---

## ⚙️ Configuración de Suricata

* Activación de reglas por defecto
* Creación de reglas personalizadas para detección de:

  * Escaneo de puertos
  * Actividad sospechosa
* Configuración de thresholds para reducción de alertas repetitivas

---

## 📊 Resultados

* Detección exitosa de escaneo de red
* Generación de alertas en tiempo real
* Reducción de falsos positivos mediante tuning de reglas
* Mejora en la interpretación de logs de seguridad

---

## 🚧 Problemas Encontrados

* Alto volumen de alertas iniciales (ruido)
* Necesidad de ajuste de reglas
* Configuración inicial compleja del entorno

---

## 📚 Aprendizajes Clave

* Importancia del análisis de tráfico en detección de amenazas
* Uso práctico de IDS en entornos controlados
* Diferenciación entre tráfico normal y malicioso
* Optimización de reglas para mejorar la eficiencia

---

## 🚀 Próximos Pasos

* Integrar Suricata con herramientas SIEM
* Simular ataques más complejos
* Generar reportes tipo SOC

---

