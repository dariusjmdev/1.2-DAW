# Práctica 1.2 - Instalación básica de Apache

## Objetivo

Instalar y verificar el funcionamiento del servidor web Apache.

## Instalación

Actualizamos los repositorios:

sudo apt update

Instalamos Apache:

sudo apt install apache2 -y

## Versión

apache2 -v

Resultado:

<img width="467" height="95" alt="Captura de pantalla 2026-10-20 153922" src="https://github.com/user-attachments/assets/519068f6-0b68-4bde-a9c9-44f99aaaa66e" />


## Verificación del servicio

sudo systemctl status apache2

El servicio aparece como active (running).

<img width="987" height="321" alt="Captura de pantalla 2026-10-20 153950" src="https://github.com/user-attachments/assets/9c53c2bd-0c9a-4236-8295-1d757410959d" />

## Habilitación automática

systemctl is-enabled apache2

Resultado:

enabled

<img width="607" height="50" alt="Captura de pantalla 2026-10-20 154021" src="https://github.com/user-attachments/assets/aec3cced-f11f-4fe8-bdf8-f4d852f50649" />

## Puerto utilizado

Apache escucha en el puerto 80.

Comprobación:

sudo ss -tulpn | grep :80

<img width="977" height="122" alt="Captura de pantalla 2026-10-20 154037" src="https://github.com/user-attachments/assets/1735c7ed-a629-4f7a-97b1-802d054fe20b" />

## Dirección IP

ip a

IP del servidor:

192.168.1.152

## Acceso desde el navegador

Desde el equipo anfitrión se accede mediante:

http://192.168.1.152

Se muestra correctamente la página por defecto de Apache.

<img width="940" height="1003" alt="Captura de pantalla 2026-10-20 154217" src="https://github.com/user-attachments/assets/6eda7ebf-6b77-4418-b7f7-3202164aa6e1" />

## Conceptos

### ¿Qué es un servidor web?

Un servidor web es un software que recibe peticiones HTTP y devuelve contenido como páginas web.

### ¿Qué es Apache?

Apache HTTP Server es uno de los servidores web más utilizados del mundo.

### ¿Qué es HTTP?

HTTP es el protocolo utilizado por los navegadores para solicitar recursos web.

### Diferencia entre HTTP y HTTPS

HTTP transmite la información sin cifrar.
HTTPS utiliza TLS/SSL para cifrar la comunicación y mejorar la seguridad.

### Cliente HTTP

El navegador web actúa como cliente HTTP y Apache como servidor HTTP.

## Conclusión

Apache ha sido instalado correctamente, está activo, habilitado al inicio y accesible desde el host mediante el puerto 80.
