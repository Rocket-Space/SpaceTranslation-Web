# Especificaciones Técnicas y Requisitos del Sistema
*Documento para el Agente Web de la Landing Page*

Usa esta información para construir la sección de "Requisitos del Sistema", "Características" o "Preguntas Frecuentes (FAQ)" de la página web de descarga de **Space Translation**.

## 🚀 Características Clave (Para destacar en la web)
- **Ultra Ligero**: Consumo mínimo de RAM (aprox 15-25 MB).
- **Traducción Asíncrona**: La interfaz nunca se congela, traducciones fluidas en segundo plano.
- **Multimotor Integrado**: Acceso gratuito a los mejores motores del mundo sin necesidad de API Keys (Google, Alibaba, Yandex, Papago y herramientas nativas para idioma Chino como Sogou).
- **Inyección Automática de Texto**: Capacidad de traducir y escribir automáticamente el resultado en la ventana o juego que el usuario tenga abierto.

## 💻 Requisitos del Sistema (Para la sección de descargas)

### 🪟 Windows
- **Sistemas Soportados**: Windows 10, Windows 11.
- **Dependencias Adicionales**: Ninguna. La aplicación funciona de manera nativa ("Plug and Play").

### 🍎 macOS
- **Sistemas Soportados**: macOS 10.15 (Catalina) o superior.
- **Requisitos Adicionales**: Para que la función de "Traducir e Insertar" funcione, el usuario debe otorgar permisos de **Accesibilidad** a la aplicación en `Preferencias del Sistema > Seguridad y Privacidad > Privacidad > Accesibilidad`.

### 🐧 Linux
- **Sistemas Soportados**: Cualquier distribución moderna (Ubuntu, Fedora, Arch, Mint, etc.).
- **Dependencias de Inyección de Texto (Obligatorias)**:
  Debido a las estrictas medidas de seguridad de Linux, para que la app pueda "escribir/insertar" el texto traducido automáticamente en otros programas, el usuario debe instalar las herramientas de teclado virtual según su protocolo de pantalla:
  
  > **Para usuarios con Wayland (Ubuntu 22.04+, Fedora, etc.):**
  > ```bash
  > sudo apt install wl-clipboard wtype
  > # o su equivalente en pacman/dnf
  > ```
  > **Para usuarios con X11 / X.Org (Sistemas más antiguos o configuraciones clásicas):**
  > ```bash
  > sudo apt install xclip xdotool
  > ```
  *(Nota para el agente web: Es altamente recomendable colocar un botón de "Ver Instrucciones para Linux" que despliegue estos dos comandos).*

## 🌐 Requisitos de Red
- Conexión a Internet activa (banda ancha estándar).
- Sin bloqueos de firewall hacia dominios de traducción públicos.
