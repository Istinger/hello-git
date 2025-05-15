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

/home
├── usuario1
│ └── public_html
│ ├── index.html
│ └── credenciales.txt
├── usuario2
│ └── public_html
...
/etc/nginx
├── sites-available
│ └── usuario1.com
└── sites-enabled


---

## ⚙️ Scripts Incluidos

### ✅ `crear_usuarios.sh`

Script que crea automáticamente:

- Usuario del sistema
- Carpeta `public_html` y `index.html` personalizado
- Base de datos + usuario
- Contraseña aleatoria
- Configuración de NGINX y enlaces simbólicos

### ✅ `eliminar_usuarios.sh`

Borra:

- Usuario del sistema
- Carpeta personal
- Base de datos
- Configuración de NGINX

---

## 🧪 Acceso y Pruebas

1. Accede a la página individual:

http://usuario5.com:8023/


2. Prueba desde cliente:
Agrega en `/etc/hosts` (cliente):

172.17.42.125 usuario5.com


3. Accede a phpMyAdmin:

http://172.17.42.125:8013/phpmyadmin


---

## 📸 Captura de diseño

![Ejemplo de sitio](https://cdn.pixabay.com/photo/2022/05/01/23/42/sky-7167273_1280.jpg)

---

## 👨‍💻 Autor

**Jossue – LinuxLab UIO VPS #23**

---

## 📃 Licencia

MIT License
