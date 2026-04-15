# 🛡️ SentinelOS
> Sistema operativo de ciberseguridad basado en Debian 12, diseñado para entornos académicos, laboratorios y pruebas de penetración.

---

## 🚀 Descripción General

SentinelOS es una distribución Linux orientada a la seguridad, construida sobre **Debian 12 (Bookworm)**. Fue desarrollada como proyecto final del curso **CY-301 Sistemas Operativos Intermedios** de la Universidad Fidelitas, por el Grupo No. 1.

El sistema incluye un entorno gráfico **GNOME** completamente personalizado, más de **40 herramientas de ciberseguridad** preinstaladas, y un proceso de instalación guiado mediante el instalador gráfico **Calamares**.

---

## 🎯 Propósito

SentinelOS está diseñado para:

- 🔍 Pruebas de penetración (Pentesting)
- 🌐 Análisis de tráfico de red
- 🔐 Análisis forense digital
- 🧠 Aprendizaje práctico en ciberseguridad
- 🛡️ Desarrollo y práctica de mecanismos de defensa

---

## 🧰 Características Principales

- 🐧 **Base:** Debian 12 (Bookworm) — kernel 6.1.0-44-amd64
- 🖥️ **Entorno gráfico:** GNOME 43 con tema Orchis-Grey-Dark e iconos Tela-dark
- 💿 **Instalador:** Calamares con branding personalizado de SentinelOS
- 🪶 **ISO optimizada** mediante compresión squashfs (xz)
- 🔒 **Seguridad integrada:** UFW, Fail2ban, política de contraseñas PAM
- ⚙️ **Instalación modular:** herramientas pesadas se instalan automáticamente en el primer arranque
- 🌐 **Detección automática de zona horaria** por IP al arrancar
- 🧅 **Tor Browser** preinstalado para navegación anónima
- 📦 **Compatible con VirtualBox 7.x y VMware Workstation/Player**

---

## 🧪 Herramientas Incluidas

SentinelOS utiliza un enfoque **modular**: las herramientas ligeras están preinstaladas en el ISO, y las herramientas pesadas se instalan automáticamente en el primer arranque del sistema instalado.

### 🔍 Reconocimiento y OSINT
| Herramienta | Descripción |
|---|---|
| Nmap | Escáner de puertos y servicios de red |
| Masscan | Escáner masivo de puertos |
| theHarvester | Recolección de información OSINT |
| Recon-ng | Framework modular de reconocimiento web |
| DNSRecon / DNSenum | Enumeración y análisis DNS |
| Nikto | Escáner de vulnerabilidades web |
| Whois | Información de registro de dominios |

### 💥 Explotación
| Herramienta | Descripción |
|---|---|
| Metasploit Framework | Framework completo de pruebas de penetración |
| SQLMap | Detección y explotación de inyecciones SQL |
| Commix | Inyección de comandos en aplicaciones web |
| SearchSploit | Base de datos local de exploits (Exploit-DB) |

### 🔑 Ataques de Contraseñas
| Herramienta | Descripción |
|---|---|
| John the Ripper | Crackeo de hashes de contraseñas |
| Hashcat | Crackeo de contraseñas con GPU |
| Hydra | Fuerza bruta de servicios de red |
| Medusa | Fuerza bruta paralela |
| CeWL / Crunch | Generadores de wordlists personalizados |

### 📡 Seguridad Inalámbrica
| Herramienta | Descripción |
|---|---|
| Aircrack-ng | Suite completa de auditoría WiFi |
| Wifite | Auditoría WiFi automatizada |
| Reaver / Bully | Ataques WPS |

### 🕵️ Análisis de Red
| Herramienta | Descripción |
|---|---|
| Wireshark | Analizador gráfico de tráfico de red |
| tcpdump | Captura de paquetes desde terminal |
| Ettercap | Ataques Man-in-the-Middle |
| Bettercap | Framework de ataques de red |
| Mitmproxy | Proxy para análisis de tráfico HTTPS |

### 🌐 Seguridad Web
| Herramienta | Descripción |
|---|---|
| Burp Suite Community | Proxy para pruebas de seguridad web |
| OWASP ZAP | Escáner de vulnerabilidades web |
| Gobuster | Fuerza bruta de directorios web |
| WhatWeb | Fingerprinting de aplicaciones web |
| WFuzz / Dirb | Fuzzing y enumeración web |

### 🔬 Análisis Forense
| Herramienta | Descripción |
|---|---|
| Autopsy | Plataforma gráfica de análisis forense |
| Volatility3 | Análisis de volcados de memoria RAM |
| Binwalk | Análisis y extracción de firmware |
| Steghide | Esteganografía en imágenes |
| ExifTool | Análisis de metadatos de archivos |

### ⚙️ Ingeniería Inversa
| Herramienta | Descripción |
|---|---|
| Ghidra | Framework de ingeniería inversa (NSA) |
| GDB | Depurador de binarios |
| Radare2 | Análisis y desensamblado de binarios |

---

## 🔒 Mecanismos de Seguridad

| Mecanismo | Descripción |
|---|---|
| UFW | Firewall — deny incoming, allow outgoing por defecto |
| Fail2ban | Bloqueo automático de IPs con intentos fallidos SSH |
| PAM pwquality | Política de contraseñas: mín. 12 chars, mayús, minús, números y símbolos |
| Faillock | Bloqueo de cuentas tras 10 intentos fallidos |
| Permisos de archivos | Sistema de permisos Unix estándar |

---

## 💿 Instalación

### Opción 1: Modo Live (sin instalación)
1. Cargar `SentinelOS-1.0-amd64.iso` en VirtualBox o VMware
2. Arrancar la VM — el sistema inicia automáticamente en modo live
3. El instalador Calamares se abre automáticamente para instalar en disco

### Opción 2: Instalación completa con Calamares
1. Arrancar desde el ISO en modo live
2. Seguir el asistente de instalación Calamares
3. Crear usuario y configurar el sistema
4. Reiniciar — el sistema arranca desde el disco instalado
5. En el primer arranque se instalan automáticamente las herramientas pesadas

### Requisitos mínimos
| Componente | Mínimo | Recomendado |
|---|---|---|
| RAM | 4 GB | 6 GB |
| Disco | 20 GB | 40 GB |
| CPU | 2 núcleos 64-bit | 4 núcleos |
| Video | 128 MB VRAM | 256 MB VRAM |

---

## 🧠 Arquitectura del Sistema

```
SentinelOS ISO
├── Modo Live
│   ├── Autologin → admin
│   ├── Calamares (instalador gráfico)
│   └── Herramientas ligeras disponibles
└── Sistema Instalado
    ├── Pantalla de login (sin autologin)
    ├── Primer arranque → instala herramientas pesadas
    │   ├── Metasploit Framework
    │   ├── Burp Suite Community
    │   ├── Ghidra
    │   ├── theHarvester
    │   └── Volatility3, Shodan CLI
    └── Sistema completamente funcional
```

---

## ⚠️ Aviso Legal

SentinelOS está diseñado exclusivamente para **uso educativo y ético**. Todas las herramientas incluidas deben utilizarse únicamente en entornos controlados y con autorización explícita.

Los desarrolladores no se hacen responsables por el uso indebido o actividades ilegales realizadas con este sistema.

---

## 👨‍💻 Autores

| Nombre | Usuario |
|---|---|
| Daniela Álvarez Murillo | `dalvarez` |
| Jathzael Saavedra Ugalde | `jsaavedra` |
| Mauricio Trejos Gómez | `mtrejos` |
| Saulo Jimenez Aguiluz | `sjimenez` |

**Universidad Fidelitas — CY-301 Sistemas Operativos Intermedios — Grupo No. 1 — 2026**

---

## ⭐ Apoyo

Si te gusta este proyecto:
- ⭐ Dale estrella al repositorio
- 🔁 Compártelo con la comunidad
- 🧠 Brinda retroalimentación
