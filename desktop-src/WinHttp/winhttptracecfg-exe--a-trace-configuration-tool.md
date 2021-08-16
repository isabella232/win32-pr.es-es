---
description: La herramienta de configuración de seguimiento de microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, se usa para configurar funcionalidades de seguimiento con fines de depuración y de búsqueda de paquetes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7747e0b2fe023ab3c2c86d19a722059482aed19062cf2a450b8d0f237a8b3a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562423"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento

La herramienta de configuración de seguimiento de servicios [HTTP de Microsoft Windows (WinHTTP),](about-winhttp.md) WinHttpTraceCfg.exe, se usa para configurar funcionalidades de seguimiento con fines de depuración y de búsqueda de paquetes. La capacidad de supervisar las funciones WinHTTP y su tráfico de red correspondiente es importante. Las aplicaciones de depuración que usan protocolos de conexión cifrados, como Capa de sockets seguros (SSL), impiden el análisis de paquetes en la capa de transporte de red y requieren la capacidad de interceptar el tráfico entre el cliente y el servidor después de que se haya descifrado. Microsoft Windows HTTP Services (WinHTTP) proporciona una instalación de seguimiento que tiene una variedad de funcionalidades para interceptar el flujo de tráfico entre el cliente y el servidor.

Esta instalación de seguimiento puede ser una herramienta valiosa para la depuración. Se puede usar, por ejemplo, para ver los parámetros pasados a varias llamadas de función, así como para ver los datos reales enviados y recibidos por una aplicación WinHTTP.

-   [Uso de la instalación de seguimiento](#using-the-trace-facility)
-   [Interpretación de datos de seguimiento](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Uso de la instalación de seguimiento

WinHTTP obtiene los parámetros de control de seguimiento del Registro. Estos parámetros de control afectan a cómo WinHTTP genera la salida de seguimiento y cómo se formatee esa salida. Todas las aplicaciones que usan WinHTTP comparten la misma configuración.

Una herramienta de configuración de la instalación de seguimiento, WinHttpTraceCfg.exe, está disponible como descarga en el sitio web Windows Resource Kit Tools de [Windows Server 2003.](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) La herramienta de configuración establece o recupera la configuración del Registro de la instalación de seguimiento en función de los parámetros de línea de comandos especificados.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

En la tabla siguiente se enumeran los posibles parámetros de la herramienta de configuración.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Muestra los datos de sintaxis.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Especifica si la instalación de seguimiento está habilitada o deshabilitada. <br/> 
<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuración predeterminada. Deshabilita el seguimiento.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita el seguimiento.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-l</td>
<td><p>Especifica un prefijo para el archivo de registro. El prefijo puede incluir una ruta de acceso. El archivo de registro se escribe en el directorio actual o en el directorio especificado en el prefijo y tiene el formato siguiente.</p>
<p><<em></em> > prefijo -< <em>nombre de la aplicación</em> > . <<em>.log de</em> > tiempo</p>
<p>Si no se especifica un prefijo, se usa una cadena vacía. Especifique &quot; * &quot; para eliminar un prefijo existente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Especifica si la salida de seguimiento se muestra en un depurador o se escribe en un archivo.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuración predeterminada. Escribe en el archivo de registro.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Se muestra en un depurador.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-S</td>
<td><p>Especifica cómo se muestra el tráfico de red (solicitudes y respuestas).</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Solo muestra los encabezados HTTP.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Configuración predeterminada. Muestra el tráfico de red American National Standards Institute (ANSI).</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Muestra el tráfico de red en formato hexadecimal.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>-T</td>
<td><p>Especifica si las llamadas de función de nivel superior se registran en el seguimiento.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuración predeterminada. Las llamadas de función no se registran.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Se registran las llamadas de función de nivel superior.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>-M</td>
<td><p>Especifica el tamaño máximo, en bytes, de un archivo de registro generado por la instalación de seguimiento. Si esta opción se especifica sin un tamaño, el valor mínimo es 65 535 bytes. Si un archivo de registro alcanza el tamaño máximo, se borra el contenido del archivo. Los datos de seguimiento se siguen escribendo en el archivo de registro.</p></td>
</tr>
</tbody>
</table>



 

La ejecución de la herramienta de configuración de la instalación de seguimiento y la especificación de ningún parámetro recupera y muestra la configuración actual del Registro.

> [!Note]  
> Los archivos de registro crecen rápidamente y degradan el rendimiento de la aplicación. Asegúrese de que el espacio necesario en la unidad de disco duro esté disponible antes de habilitar la instalación de seguimiento.

 

## <a name="interpreting-trace-data"></a>Interpretación de datos de seguimiento

El flujo de datos de la instalación de seguimiento refleja las funciones WinHTTP llamadas en la aplicación y los datos HTTP enviados o recibidos. En algunos casos, también se muestran las funciones llamadas internamente por WinHTTP.

En la imagen siguiente se muestra una parte de un archivo de registro generado por la instalación de seguimiento. Varios elementos están resaltados y etiquetados.

![seguimiento de ejemplo](images/ss-tracer-wco.png)

Cada línea de salida de seguimiento contiene información en tres columnas. La primera columna muestra la fecha y hora en que se registró la entrada. La segunda columna muestra un identificador de solicitud (ID) que se puede usar para diferenciar entre varias solicitudes. Si la entrada del registro no se corresponde con una solicitud específica, se muestra \* \* "Sesión" en esta columna. Puede ser útil ordenar el archivo de registro en función de este identificador para ver solo los eventos que se producen para una única solicitud. En el ejemplo siguiente se muestra un comando que puede usar para ordenar el archivo de registro.

**findstr 00000001 LogFile.log**

La tercera columna muestra una llamada de función, tráfico HTTP o un mensaje de estado incluido para ayudar a interpretar el seguimiento.

Cuando una entrada de registro corresponde a una llamada de función, también se registran los parámetros de la función. Las direcciones de memoria se muestran en formato hexadecimal, mientras que todos los demás valores se muestran como una cadena ASCII. La instalación de seguimiento también registra el tiempo de devolución y el valor de cada función.

El formato de los datos HTTP depende de la configuración del Registro especificada con la herramienta de configuración de la instalación de seguimiento. Cuando se cifran los datos HTTP, los datos descifrados también se muestran en la salida de seguimiento.

 

 




