---
description: 'Más información sobre: JET_INSTANCE_INFO miembros'
title: JET_INSTANCE_INFO miembros
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 700e2d8cae5882c2c7ae4762e7b1c2d088345d6040a844a80693404deb029dc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604155"
---
# <a name="jet_instance_info-members"></a>JET_INSTANCE_INFO miembros

Incluir miembros protegidos  
Incluir miembros heredados  

Recibe información sobre la ejecución de instancias de base de datos cuando se usa con las funciones JetGetInstanceInfo y JetOSSnapshotFreeze.

El [JET_INSTANCE_INFO](./jet-instance-info-class.md) expone los miembros siguientes.

## <a name="properties"></a>Propiedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335189(v=exchg.10).md">cDatabases</a></td>
<td>Obtiene el número de bases de datos asociadas a la instancia de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335190(v=exchg.10).md">hInstanceId</a></td>
<td>Obtiene el JET_INSTANCE de la instancia especificada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></td>
<td>Obtiene una colección de cadenas, cada una de las que contiene el nombre de archivo de una base de datos asociada a la instancia de base de datos. La matriz tiene elementos cDatabases.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335194(v=exchg.10).md">szInstanceName</a></td>
<td>Obtiene el nombre de la instancia de base de datos. Este valor puede ser NULL si la instancia no tiene un nombre.</td>
</tr>
</tbody>
</table>


Superior

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335184(v=exchg.10).md">Equals(Object)</a></td>
<td>Devuelve un valor que indica si esta instancia es igual a otra instancia. (Invalida <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></td>
<td>Devuelve un valor que indica si esta instancia es igual a otra instancia.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335191(v=exchg.10).md">GetHashCode</a></td>
<td>Devuelve el código hash de esta instancia. (Invalida <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335192(v=exchg.10).md">ToString</a></td>
<td>Genere una representación de cadena de la instancia. (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INSTANCE_INFO clase](./jet-instance-info-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
