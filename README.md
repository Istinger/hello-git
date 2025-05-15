# 🌐 Proyecto de Hosting Web Multiusuario en LinuxLab

Este proyecto implementa un sistema completo de hosting web **multiusuario** usando:

- 🧩 NGINX como servidor web
- 🛢️ MariaDB para bases de datos
- 📂 FTP (vsftpd) para carga de archivos
- 🧠 phpMyAdmin para administración de bases de datos
- 🐧 Usuarios del sistema aislados (enjaulados)
- 🔒 Seguridad y control de acceso
- 🛠️ Script en Bash para automatizar la creación de cuentas

---

## 🎯 Objetivo

Permitir que múltiples usuarios en LinuxLab tengan:

- Su propio sitio web individual:  
  `http://usuarioX.com:8023/`
- Acceso FTP aislado  
- Base de datos propia  
- Acceso a phpMyAdmin  
- Archivos HTML/PHP dentro de `/home/usuarioX/public_html`

---

## 📦 Estructura del Proyecto

