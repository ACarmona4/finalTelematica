# Proyecto Final Telemática
Realizado por: Miguel A. Arcila, Alejandro Carmona y David Restrepo

## Introducción

En este proyecto desarrollamos un servidor DNS usando el software BIND, implementado en una máquina virtual con Ubuntu en VirtualBox. El objetivo principal fue aprender y aplicar conceptos básicos de resolución de nombres dentro de una red privada, configurando zonas directas e inversas, y validando que el servidor funcione correctamente.

El servidor DNS es esencial para que los dispositivos puedan comunicarse usando nombres comunes o fáciles de recordar en lugar de direcciones IP complejas que nadie se va a a memorizar. Este proyecto nos permitió comprender mejor cómo funciona el servicio DNS y cómo configurarlo en un entorno controlado.

## Desarrollo

Para iniciar, instalamos el servicio BIND y sus herramientas asociadas en Ubuntu. Luego configuramos el archivo principal para incluir nuestro dominio simulado `grupoX.local` y creamos los archivos de zona directa (nombre a IP) e inversa (IP a nombre) con registros básicos como A, PTR, SOA y NS.

Las direcciones IP configuradas fueron `192.168.1.34` para el servidor DNS (ns1.grupoX.local) y `192.168.1.35` para un dispositivo cliente simulado (pc1.grupoX.local). Estos dispositivos se encuentran en la misma red local simulada dentro de VirtualBox.

Investigamos también sobre el modo chroot para BIND, que consiste en ejecutar el servidor en un entorno aislado para mejorar la seguridad. Conocimos sus ventajas y consideramos su implementación para futuras mejoras, aunque finalmente no lo configuramos en este proyecto.

Probamos la resolución de nombres usando herramientas como `dig` y `nslookup`, verificando que las consultas directas e inversas funcionaran correctamente desde la máquina virtual.

## Aspectos Logrados y No Logrados

### Logrados
- Instalación y configuración correcta de BIND en Ubuntu.
- Creación y carga exitosa de zonas directa e inversa.
- Validación de funcionamiento mediante pruebas con `dig`.

### No Logrados
- Configuración del modo chroot para aislamiento del servicio.
- Pruebas desde equipos externos fuera de la red local.

## Conclusiones

El proyecto nos permitió comprender de manera práctica cómo funciona un servidor DNS y la importancia de configurarlo correctamente para mantener la seguridad y funcionalidad de la red. Aprendimos que las pruebas con herramientas como `dig` son esenciales para validar el correcto funcionamiento.

Este ejercicio fue muy valioso para entender conceptos claves de redes y seguridad informática, y nos preparó para enfrentar configuraciones reales en entornos de producción con mayor confianza.


