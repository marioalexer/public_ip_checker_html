# IP pública – HTML simple

Página HTML estática para detectar y copiar la IP pública del navegador.  
No requiere backend ni dependencias externas locales.

Pensada para uso rápido por equipos técnicos, clientes o soporte.

## Características

- Detecta la IP pública desde el navegador
- Soporte IPv4 e IPv6
- Botón y clic directo para copiar al portapapeles
- Fallback entre múltiples proveedores públicos
- Interfaz mínima, responsive y sin frameworks
- Funciona desde cualquier hosting estático

## Cómo funciona

La IP se obtiene consultando varios servicios públicos en orden, con timeout por intento:

- api.ipify.org
- api64.ipify.org
- ipapi.co
- api.myip.com

El primer proveedor que responde devuelve la IP.  
Si todos fallan, se muestra un mensaje de error.

## Requisitos

- Navegador moderno con JavaScript habilitado
- Acceso a servicios externos de detección de IP
- Permisos de portapapeles (Clipboard API)

## Uso

1. Clona o descarga el repositorio
2. Abre `index.html` en un navegador  
   o
3. Súbelo a cualquier hosting estático (Apache, Nginx, GitHub Pages, etc.)

No requiere configuración adicional.

## Personalización

- Reemplaza `logo.png` por tu logotipo
- Ajusta el enlace en `#logoLink`
- Cambia colores y tipografía desde el bloque `<style>`

## Limitaciones conocidas

- No funciona sin conexión a Internet
- Puede fallar en redes corporativas con bloqueo de APIs externas
- No garantiza precisión si el proveedor devuelve IPs proxy/NAT

## Seguridad y privacidad

- No se almacenan datos
- No se usan cookies
- Las consultas se hacen directamente desde el navegador del usuario

## Licencia

MIT
