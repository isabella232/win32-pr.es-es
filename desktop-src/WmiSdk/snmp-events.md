---
description: El proveedor SNMP admite la escritura en archivos de registro y en el depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos de SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efec74902039b9e196844e9d7fadbda01cd6036
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625351"
---
# <a name="snmp-events"></a>Eventos de SNMP

El proveedor SNMP admite la escritura en archivos de registro y en el depurador.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Una serie de claves y valores del Registro definen el nivel y el tipo de registro que se está generando actualmente:

-   Depuración

    La clave del Registro **HKEY \_ LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM PROVIDERS \\ \\ LOGGING** contiene el valor de registro que indica si se puede escribir información en el depurador. El valor de registro se establece en 0 para deshabilitar la salida de depuración o 1 para habilitarla. El registro es un valor \_ REG DWORD.

-   Registro

    La clave del Registro **HKEY \_ LOCAL MACHINE SOFTWARE MICROSOFT \_ \\ \\ \\ WBEM PROVIDERS \\ \\ LOGGING \\ WBEMSNMP** contiene toda la información de registro específica del proveedor SNMP. En la tabla siguiente se enumeran los valores asociados a esta clave.



<table>
<colgroup>
<col  />
<col  />
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
<td><strong>REG_SZ</strong><br/> Toma uno de los valores siguientes:<br/> &quot;Archivo &quot; = (valor predeterminado) Envía la salida de depuración a un archivo.<br/> &quot;Depurador &quot; = Envía la salida de depuración al depurador.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Toma valores enteros de 1024 a 2^32-1. El valor es el tamaño máximo permitido en bytes para el archivo de registro. Si es menor que 1024, el mecanismo de registro usa un valor de 1024. Se recomienda un tamaño mínimo de 8 KB para este valor. Cuando el archivo alcanza el tamaño especificado por MaxFileSize, el nombre de archivo se antepone con un carácter "~" y se crea un nuevo archivo. Por lo tanto, el espacio en disco máximo necesario para el registro es el doble de este valor.<br/></td>
</tr>
<tr class="odd">
<td>Archivo</td>
<td><strong>REG_SZ</strong><br/> Define el nombre del archivo al que se envía la salida de depuración cuando el tipo de registro se establece en "File". El valor predeterminado es <WBEMLOGS> "\wbemsnmp.log". Si el directorio no se puede determinar desde la sección del Registro WMI, el valor predeterminado <WBEMLOGS> es "c:\wbemsnmp.log". Si se usa un recurso compartido, como \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log donde M: es machine\share, la cuenta system local en la que se ejecuta WMI debe tener derechos de acceso de \\ \\ lectura/escritura a la máquina\recurso compartido.<br/></td>
</tr>
<tr class="even">
<td>Nivel</td>
<td><strong>REG_DWORD</strong><br/> Toma valores enteros de 0 a 2^32-1. El valor es una máscara lógica que consta de 32 bits. Las siguientes máscaras de bits se combinan para definir el tipo de salida de depuración generada:<br/>
<ul>
<li>0: Invocaciones del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de clases SNMP</li>
<li>1: Implementación del proveedor de clases SNMP</li>
<li>2: Invocaciones del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices del</strong></a> proveedor de instancias SNMP</li>
<li>3: Implementación del proveedor de instancias SNMP</li>
<li>4: Biblioteca de clases SNMP</li>
<li>5: SNMP SMIR</li>
<li>6: Correlacionador SNMP</li>
<li>7: Código de asignación de tipos SNMP</li>
<li>8: Código de subprocesos SNMP</li>
<li>9: Implementación e interfaces del proveedor de eventos SNMP</li>
</ul>
Establezca Level en (2^0 + 2^8=) 257 para las operaciones que implican llamadas al proveedor de clases SNMP <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> y operaciones que usan código de subprocesos SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




