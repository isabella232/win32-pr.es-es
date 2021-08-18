---
title: Configuración del registro de errores de LA API del servidor HTTP
description: El registro de errores de la API del servidor HTTP se controla mediante tres valores del Registro en una clave \\ de parámetros HTTP.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API de servidor HTTP, configuración de registros de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10479a1b2bd1ebf559213b6cd4b738f6c0b9ea63c142edcce3c10f64f877dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950894"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor del Registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>DWORD <strong>que</strong> se puede establecer en <strong>TRUE para</strong> habilitar el registro de errores o <strong>FALSE</strong> para deshabilitarlo. El valor predeterminado es <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td>DWORD <strong>que</strong> especifica el tamaño máximo de un archivo de registro de errores, en bytes. El valor predeterminado es un MB (0x100000).<br/>
<blockquote>
[!Note]<br />
El valor especificado no puede ser menor que el valor predeterminado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td>Cadena <strong>que</strong> especifica la carpeta en la que la API del servidor HTTP coloca sus archivos de registro. <br/> La API del servidor HTTP crea una subcarpeta denominada HTTPERR en la carpeta especificada en la que se colocan los &quot; &quot; archivos de registro. Esta subcarpeta y los archivos de registro reciben la misma configuración de permisos, lo que significa que las cuentas de administrador y del sistema local tienen acceso completo, mientras que otros usuarios no tienen acceso.<br/> Si no se especifica una carpeta en el Registro, la carpeta predeterminada es la siguiente:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
El valor de cadena ErrorLoggingDir debe ser una ruta de acceso completa, pero puede contener &quot; %SystemRoot%. &quot;
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





