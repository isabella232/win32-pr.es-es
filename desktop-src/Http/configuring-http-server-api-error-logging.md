---
title: Configuración del registro de errores de LA API del servidor HTTP
description: El registro de errores de la API del servidor HTTP se controla mediante tres valores del Registro en una clave \\ de parámetros HTTP.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API de servidor HTTP, configuración de registros de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7864a4361ce0ae9e2726884e749fd0342f52a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467932"
---
# <a name="configuring-http-server-api-error-logging"></a>Configuración del registro de errores de LA API del servidor HTTP

El registro de errores de la API del servidor HTTP se controla mediante tres valores del Registro en una clave **de** parámetros HTTP \\  ubicada en:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> La ubicación y la forma de los valores de configuración pueden cambiar en versiones futuras del Windows operativo.

 

Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del Registro y ver o modificar los archivos de registro y la carpeta que los contiene.

La información de configuración de los valores del Registro se lee cuando se inicia el controlador de API del servidor HTTP. Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores. Esto se puede lograr mediante los siguientes comandos de consola:

**net stop http**

**net start http**

Los archivos de registro se denominan mediante la convención siguiente:

**httperr +** *SequenceNumber* **+ .log**

Por ejemplo: "httperr4.log".

Los archivos de registro se ciclon cuando alcanzan el tamaño máximo especificado por el valor del Registro **ErrorLogFileTruncateSize** y el valor no puede ser inferior a un megabyte (MB).

Si la configuración del registro de errores no es válida o se produce algún tipo de error al escribir en los archivos de registro, la API del servidor HTTP usa el registro de eventos para notificar a los administradores que no se produjo el registro de errores.

Los valores de configuración del Registro se describen en la tabla siguiente.




| Valor del Registro | Descripción | 
|----------------|-------------|
| <span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br /> | DWORD <strong>que</strong> se puede establecer en <strong>TRUE para</strong> habilitar el registro de errores o <strong>FALSE</strong> para deshabilitarlo. El valor predeterminado es <strong>TRUE.</strong><br /> | 
| <span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br /> | DWORD <strong>que</strong> especifica el tamaño máximo de un archivo de registro de errores, en bytes. El valor predeterminado es un MB (0x100000).<br /><blockquote>[!Note]<br />El valor especificado no puede ser menor que el valor predeterminado.</blockquote><br /> | 
| <span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br /> | Cadena <strong>que</strong> especifica la carpeta en la que la API del servidor HTTP coloca sus archivos de registro. <br /> La API del servidor HTTP crea una subcarpeta denominada "HTTPERR" en la carpeta especificada en la que se colocan los archivos de registro. Esta subcarpeta y los archivos de registro reciben la misma configuración de permisos, lo que significa que las cuentas de administrador y del sistema local tienen acceso completo, mientras que otros usuarios no tienen acceso.<br /> Si no se especifica una carpeta en el Registro, la carpeta predeterminada es la siguiente:<br /> "%SystemRoot%\System32\LogFiles"<br /><blockquote>[!Note]<br />El valor de cadena ErrorLoggingDir debe ser una ruta de acceso completa, pero puede contener "%SystemRoot%".</blockquote><br /><br /> | 




 

 

 





