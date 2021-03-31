---
title: Configuración del registro de errores de la API del servidor HTTP
description: El registro de errores de la API del servidor HTTP se controla mediante tres valores del registro bajo una \\ clave http Parameters.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API de servidor HTTP, configurar registros de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418676"
---
# <a name="configuring-http-server-api-error-logging"></a>Configuración del registro de errores de la API del servidor HTTP

El registro de errores de la API del servidor HTTP se controla mediante tres valores del registro bajo una clave **http** \\ **Parameters** , que se encuentra en:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> La ubicación y la forma de los valores de configuración pueden cambiar en versiones futuras del sistema operativo Windows.

 

Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del registro y ver o modificar los archivos de registro y la carpeta que los contiene.

La información de configuración de los valores del registro se lee cuando se inicia el controlador de la API del servidor HTTP. Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores. Esto puede realizarse mediante los siguientes comandos de la consola:

**net stop http**

**net start http**

Los nombres de los archivos de registro se denominan mediante la Convención siguiente:

**httperr +** *SequenceNumber* **+. log**

Por ejemplo: "httperr4. log".

Los archivos de registro se recorren cuando alcanzan el tamaño máximo especificado por el valor del registro **ErrorLogFileTruncateSize** y el valor no puede ser inferior a un megabyte (MB).

Si la configuración del registro de errores no es válida o se produce algún tipo de error al escribir en los archivos de registro, la API del servidor HTTP utiliza el registro de eventos para notificar a los administradores que no se ha producido el registro de errores.

En la tabla siguiente se describen los valores de configuración del registro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor del registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging<br/></td>
<td>Un <strong>valor DWORD</strong> que se puede establecer en <strong>true</strong> para habilitar el registro de errores o <strong>false</strong> para deshabilitarlo. El valor predeterminado es <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize<br/></td>
<td><strong>DWORD</strong> que especifica el tamaño máximo de un archivo de registro de errores, en bytes. El valor predeterminado es 1 MB (0x100000).<br/>
<blockquote>
[!Note]<br />
El valor especificado no puede ser menor que el valor predeterminado.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir<br/></td>
<td><strong>Cadena</strong> que especifica la carpeta en la que la API del servidor http coloca los archivos de registro. <br/> La API del servidor HTTP crea una subcarpeta denominada &quot; HTTPERR &quot; en la carpeta especificada en la que se colocan los archivos de registro. Esta subcarpeta y los archivos de registro reciben la misma configuración de permisos, lo que significa que las cuentas de administrador y del sistema local tienen acceso completo, mientras que otros usuarios no tienen acceso.<br/> Si no se especifica una carpeta en el registro, la carpeta predeterminada es la siguiente:<br/> &quot;%SystemRoot%\System32\LogFiles&quot;<br/>
<blockquote>
[!Note]<br />
El valor de cadena ErrorLoggingDir debe ser una ruta de acceso completa, pero puede contener &quot; % systemroot% &quot; .
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





