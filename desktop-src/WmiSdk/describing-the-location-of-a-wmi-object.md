---
description: Conceptualmente similar a un localizador uniforme de recursos (URL), una ruta de acceso de objeto WMI es una cadena que identifica de forma única el espacio de nombres en un servidor, una clase dentro de un espacio de nombres o instancias de una clase.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Describir la ubicación de un objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715832"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Describir la ubicación de un objeto WMI

Conceptualmente similar a un localizador uniforme de recursos (URL), una ruta de acceso de objeto WMI es una cadena que identifica de forma única el espacio de nombres en un servidor, una clase dentro de un espacio de nombres o instancias de una clase. Una ruta de acceso de objeto es jerárquica y contiene varios elementos que describen la ubicación del objeto en cuestión. Al igual que las rutas de acceso de archivo, las rutas de objeto WMI se pueden describir en su totalidad o se especifican como una ruta de acceso relativa.

El espacio de nombres de un objeto WMI se muestra en la página de referencia WMI. Por ejemplo, la ubicación de la mayoría de las clases admitidas por los [proveedores WMI de CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) se encuentra en el \\ espacio de \\ nombres root cimv2. El siguiente código de PowerShell describe una llamada para recuperar el objeto [**\_ ComputerSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) en el equipo local:

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

Como alternativa, una instancia específica de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) puede tener la siguiente ruta de acceso de la propiedad [**SWbemObject. Path \_**](swbemobject-path-.md) .

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

En el ejemplo siguiente se muestra la ruta de acceso relativa a esta instancia, tal como se muestra al mostrar la propiedad [**Relpath**](swbemobjectpath-relpath.md) del objeto [**SWbemObjectPath**](swbemobjectpath.md) devuelto por la llamada a [**SWbemObject. \_ path**](swbemobject-path-.md).

`Win32_LogicalDisk.DeviceID="A:"`

Tenga en cuenta que **DeviceID** es la propiedad clave de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

## <a name="c"></a>C++

En la tabla siguiente se enumeran los tipos de ruta de acceso de objeto y los métodos asociados que requieren rutas de objeto.



<table>
<thead>
<tr class="header">
<th>Tipo de ruta de objeto</th>
<th>Método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Espacio de nombres</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: Opennamespace (</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Clase</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a><br />
[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Clase</a> o <a href="describing-an-instance-object-path.md">instancia</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a><br />
[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Instancia</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a><br />
[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Script

Las rutas de acceso a objetos se pueden construir de varias maneras:

-   Recupere la propiedad de un método que devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) .
-   Recupere la propiedad [**SWbemObject \_ . Path**](swbemobject-path-.md) .
-   Cree una variable de cadena que contenga la ruta de acceso del objeto.

En la tabla siguiente se enumeran los objetos de scripting que requieren rutas de objeto.



<table>
<thead>
<tr class="header">
<th>Scripting (objeto)</th>
<th>Método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a><br />
[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)<br />
[<strong>Eliminar</strong>] (swbemservices-delete.md)<br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)<br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)<br />
[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)<br />
[<strong>Obtener</strong>] (swbemservices-get.md)<br />
[<strong>GetAsync</strong>] (swbemservices-getasync.md)<br />
[<strong>Referencias a</strong>] (swbemservices-referencesto.md)<br />
[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Elemento</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
