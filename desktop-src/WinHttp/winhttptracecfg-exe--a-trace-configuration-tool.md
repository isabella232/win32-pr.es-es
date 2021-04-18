---
description: La herramienta de configuración de seguimiento de servicios HTTP de Microsoft Windows (WinHTTP), WinHttpTraceCfg.exe, se usa para configurar las capacidades de seguimiento para la depuración y el examen de paquetes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715158"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a>WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento

La herramienta de configuración de seguimiento de [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, se usa para configurar las capacidades de seguimiento para la depuración y el examen de paquetes. Es importante la capacidad de supervisar las funciones WinHTTP y el tráfico de red correspondiente. La depuración de aplicaciones que usan protocolos de conexión cifrados, como Capa de sockets seguros (SSL), impide el examen de paquetes en la capa de transporte de red y requiere la capacidad de interceptar el tráfico entre el cliente y el servidor una vez descifrado. Los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan una utilidad de seguimiento que tiene una gran variedad de capacidades para interceptar el flujo de tráfico entre el cliente y el servidor.

Esta utilidad de seguimiento puede ser una valiosa herramienta para la depuración. Se puede usar, por ejemplo, para ver los parámetros que se pasan a varias llamadas de función, así como para ver los datos reales enviados y recibidos por una aplicación WinHTTP.

-   [Uso de la utilidad de seguimiento](#using-the-trace-facility)
-   [Interpretar los datos de seguimiento](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a>Uso de la utilidad de seguimiento

WinHTTP obtiene los parámetros de control de seguimiento del registro. Estos parámetros de control afectan a cómo WinHTTP produce la salida del seguimiento y cómo se da formato a esa salida. Todas las aplicaciones que usan WinHTTP comparten la misma configuración.

Una herramienta de configuración de las instalaciones de seguimiento, WinHttpTraceCfg.exe, está disponible como descarga en el sitio web de [herramientas del kit de recursos de Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . La herramienta de configuración establece o recupera los valores del registro de la utilidad de seguimiento en función de los parámetros de línea de comandos especificados.

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

En la tabla siguiente se enumeran los posibles parámetros de la herramienta de configuración de.



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
<td>Muestra datos de sintaxis.<br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Especifica si la utilidad de seguimiento está habilitada o deshabilitada. <br/> 
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
<p><<em>prefijo</em> > -< <em>nombre de la aplicación</em> > . <<em>Time</em> > . log</p>
<p>Si no se especifica un prefijo, se usa una cadena vacía. Especifique &quot; * &quot; para eliminar un prefijo existente.</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td><p>Especifica si el resultado del seguimiento se muestra en un depurador o se escribe en un archivo.</p>

<table>
<tbody>
<tr class="odd">
<td>0</td>
<td>Configuración predeterminada. Escribe en el archivo de registro.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Muestra en un depurador.</td>
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
<td>Configuración predeterminada. Muestra el tráfico de red en formato American National Standards Institute (ANSI).</td>
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
<td>Configuración predeterminada. No se registran las llamadas de función.</td>
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
<td><p>Especifica el tamaño máximo, en bytes, de un archivo de registro generado por la utilidad de seguimiento. Si se especifica esta opción sin un tamaño, el valor mínimo es 65.535 bytes. Si un archivo de registro alcanza el tamaño máximo, se borra el contenido del archivo. Los datos de seguimiento continúan escribiendo en el archivo de registro.</p></td>
</tr>
</tbody>
</table>



 

La ejecución de la herramienta de configuración de la utilidad de seguimiento y la especificación de ningún parámetro recupera y muestra la configuración actual del registro.

> [!Note]  
> Los archivos de registro crecen rápidamente y reducen el rendimiento de la aplicación. Asegúrese de que el espacio de la unidad de disco duro necesario está disponible antes de habilitar el servicio de seguimiento.

 

## <a name="interpreting-trace-data"></a>Interpretar los datos de seguimiento

El flujo de datos de las instalaciones de seguimiento refleja las funciones WinHTTP llamadas en la aplicación y los datos HTTP enviados o recibidos. En algunos casos, también se muestran las funciones a las que se llama internamente en WinHTTP.

En la imagen siguiente se muestra una parte de un archivo de registro generado por la utilidad de seguimiento. Varios elementos se resaltan y etiquetan.

![seguimiento de ejemplo](images/ss-tracer-wco.png)

Cada línea de la salida del seguimiento contiene información en tres columnas. La primera columna muestra la fecha y la hora en que se registró la entrada. La segunda columna muestra un identificador de solicitud (ID.) que se puede utilizar para diferenciar entre varias solicitudes. Si la entrada de registro no se corresponde con una solicitud específica, \* \* se muestra "sesión" en esta columna. Puede ser útil ordenar el archivo de registro en función de este identificador para ver solo los eventos que se producen para una única solicitud. En el ejemplo siguiente se muestra un comando que puede usar para ordenar el archivo de registro.

**Findstr 00000001 LogFile. log**

La tercera columna muestra una llamada de función, el tráfico HTTP o un mensaje de estado incluido para ayudar a interpretar el seguimiento.

Cuando una entrada de registro corresponde a una llamada de función, también se registran los parámetros de la función. Las direcciones de memoria se muestran en formato hexadecimal mientras que todos los demás valores se muestran como una cadena ASCII. La utilidad de seguimiento registra también el tiempo y el valor de retorno de cada función.

El formato de los datos HTTP depende de la configuración del registro especificada con la herramienta de configuración del servicio de seguimiento. Cuando se cifran los datos HTTP, los datos descifrados también se muestran en el resultado del seguimiento.

 

 




