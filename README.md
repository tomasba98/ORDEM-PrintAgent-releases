**[OrdemPrintAgent.exe — Latest Release](../../releases/latest)**

# ORDEM PrintAgent

[![License: Proprietary](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)
[![.NET](https://img.shields.io/badge/.NET-10-512BD4.svg)](https://dotnet.microsoft.com/download)

## ¿Qué es esto?

El **Agente de Impresión ORDEM** es un servicio de Windows que actúa como puente entre el sistema ORDEM en la nube y las impresoras térmicas físicas de tu restaurante. Se ejecuta en segundo plano (sin interfaz gráfica) y maneja la impresión de tickets de cocina y facturas fiscales automáticamente.

## Instalación

Para instalar el agente en la PC del restaurante, no necesitas modificar ningún archivo de configuración de forma manual. El proceso es guiado y automático:

1. **Generar el código de vinculación:**
   Desde el panel web de ORDEM, dirígete a **Ajustes → Agente de Impresión → Generar código**. Cópialo al portapapeles.
2. **Descargar el agente:**
   Descarga el archivo `OrdemPrintAgent.exe` desde la [última release](https://github.com/tomasba98/ORDEM-PrintAgent-releases/releases/latest).
3. **Ejecutar como Administrador:**
   Haz clic derecho sobre el archivo descargado y selecciona **Ejecutar como administrador**.
4. **Vincular:**
   En la consola que se abrirá, pega el código de vinculación que generaste en el paso 1.

¡Listo! El agente se instalará como un servicio de Windows (`OrdemPrintAgent`) y arrancará automáticamente al encender la PC.

## Comandos de Mantenimiento

El instalador configura automáticamente un comando corto en tu sistema. Para utilizarlo, abre una **consola nueva** (Símbolo del sistema o PowerShell) como **Administrador** y ejecuta cualquiera de las siguientes opciones:

| Comando | Descripción |
| :--- | :--- |
| `ordem --status` | Muestra el estado del servicio, la versión instalada, la última conexión al servidor y las impresoras detectadas. |
| `ordem --test-print` | Imprime un ticket de prueba en una impresora (selección interactiva). |
| `ordem --logs` | Muestra los registros (logs) del sistema en tiempo real. Presiona `Ctrl+C` para salir. |
| `ordem --update` | Fuerza la búsqueda e instalación de la última actualización disponible. |
| `ordem --restart` | Reinicia el servicio de Windows en caso de algún problema. |
| `ordem --setup` | Repite el flujo de instalación para re-vincular el agente con un código nuevo. |
| `ordem --version` | Muestra la versión actual del agente. |
| `ordem --uninstall` | Detiene y elimina el servicio por completo del sistema. |
| `ordem --help` | Muestra la lista completa de comandos disponibles. |

> **Nota:** Si Windows no reconoce el comando `ordem`, asegúrate de haber cerrado la consola y abierto una nueva después de finalizar la instalación para que se actualicen las variables del sistema.

## Código Fuente

El código fuente de esta aplicación se mantiene en un repositorio privado. Este repositorio público se utiliza exclusivamente para la distribución automatizada de las versiones (releases) y su documentación operativa.
