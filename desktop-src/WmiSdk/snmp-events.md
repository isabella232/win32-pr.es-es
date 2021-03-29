---
description: El proveedor SNMP permite escribir en archivos de registro y en el depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos de SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648279"
---
# <a name="snmp-events"></a>Eventos de SNMP

El proveedor SNMP permite escribir en archivos de registro y en el depurador.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Un número de claves y valores del registro define el nivel y el tipo de registro que se está generando actualmente:

-   Depuración

    La clave del registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging** contiene el valor de registro que indica si la información se puede escribir en el depurador. El valor de registro se establece en 0 para deshabilitar la salida de la depuración o en 1 para habilitarla. El registro es un \_ valor de REG DWORD.

-   Registro

    La clave del registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging \\ WBEMSNMP** contiene toda la información de registro específica del proveedor SNMP. En la tabla siguiente se enumeran los valores asociados a esta clave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo</td>
<td><strong>REG_SZ</strong><br/> Toma uno de los siguientes valores:<br/> &quot;File &quot; = (valor predeterminado) envía la salida de depuración a un archivo.<br/> &quot;Debugger &quot; = envía la salida de depuración al depurador.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Toma valores enteros de 1024 a 2 ^ 32-1. El valor es el tamaño máximo permitido en bytes para el archivo de registro. Si es menor que 1024, el mecanismo de registro usa un valor de 1024. Se recomienda un tamaño mínimo de 8 KB para este valor. Cuando el archivo alcanza el tamaño especificado por MaxFileSize, el nombre de archivo se antepone con un carácter ' ~ ' y se crea un archivo nuevo. Por lo tanto, el espacio en disco máximo necesario para el registro es el doble de este valor.<br/></td>
</tr>
<tr class="odd">
<td>Archivo</td>
<td><strong>REG_SZ</strong><br/> Define el nombre del archivo al que se envía la salida de depuración cuando el tipo de registro se establece en ' file '. El valor predeterminado es " <WBEMLOGS> \wbemsnmp.log.". Si <WBEMLOGS> no se puede determinar el directorio en la sección del registro WMI, el valor predeterminado es "c:\wbemsnmp.log". Si se usa un recurso compartido, como \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log, donde M: es \\ machine\share, la cuenta de sistema local en la que se ejecuta WMI debe tener derechos de acceso de lectura y escritura en \\ machine\share.<br/></td>
</tr>
<tr class="even">
<td>Nivel</td>
<td><strong>REG_DWORD</strong><br/> Toma valores enteros de 0 a 2 ^ 32-1. El valor es una máscara lógica que consta de 32 bits. Las siguientes máscaras de bits se combinan para definir el tipo de salida de depuración generada:<br/>
<ul>
<li>0: invocación del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de clases SNMP</li>
<li>1: implementación del proveedor de clase SNMP</li>
<li>2: invocaciones del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de instancias SNMP</li>
<li>3: implementación del proveedor de instancias SNMP</li>
<li>4: biblioteca de clases SNMP</li>
<li>5: SNMP SMIR</li>
<li>6: correlación de SNMP</li>
<li>7: código de asignación de tipo de SNMP</li>
<li>8: código de subprocesos SNMP</li>
<li>9: implementación e interfaces del proveedor de eventos SNMP</li>
</ul>
Establezca el nivel en (2 ^ 0 + 2 ^ 8 =) 257 para las operaciones que implican llamadas a los métodos <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de clase SNMP y las operaciones que usan código de subprocesos SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




