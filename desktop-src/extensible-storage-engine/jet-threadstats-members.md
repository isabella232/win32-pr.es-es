---
description: 'Más información sobre: JET_THREADSTATS miembros'
title: JET_THREADSTATS miembros (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f8b824f716d35c3039bb77af745cf6cf08dfc9cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172382"
---
# <a name="jet_threadstats-members"></a>JET_THREADSTATS miembros

Incluir miembros protegidos  
Incluir miembros heredados  

Contiene estadísticas acumulativas sobre el trabajo realizado por el motor de base de datos en el subproceso actual. Esta información se devuelve a través de JetGetThreadStats.

El [JET_THREADSTATS](./jet-threadstats-structure2.md) muestra los miembros siguientes.

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
<td><a href="hh578305(v=exchg.10).md">cbLogRecord</a></td>
<td>Obtiene el tamaño total, en bytes, de los registros de transacciones generados por el motor de base de datos en el subproceso actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">cLogRecord</a></td>
<td>Obtiene el número total de registros de transacciones generados por el motor de base de datos en el subproceso actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">cPageDirtied</a></td>
<td>Obtiene el número total de páginas de base de datos, sin cambios no escritos, que el motor de base de datos ha modificado en el subproceso actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">cPagePreread</a></td>
<td>Obtiene el número total de páginas de base de datos capturadas previamente desde el disco por el motor de base de datos en el subproceso actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">cPageRead</a></td>
<td>Obtiene el número total de páginas de base de datos capturadas del disco por el motor de base de datos en el subproceso actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">cPageRedirtied</a></td>
<td>Obtiene el número total de páginas de base de datos, con cambios no escritos, que el motor de base de datos ha modificado en el subproceso actual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">cPageReferenced</a></td>
<td>Obtiene el número total de páginas de base de datos visitadas por el motor de base de datos en el subproceso actual.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh565584(v=exchg.10).md">Add (Agregar)</a></td>
<td>Agregue las estadísticas en dos estructuras JET_THREADSTATS datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Crear</a></td>
<td>Cree un nuevo <a href="hh578565(v=exchg.10).md">JET_THREADSTATS</a> struct con el valor especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Equals(Object)</a></td>
<td>Devuelve un valor que indica si esta instancia es igual a otra instancia. (Invalida <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Equals(JET_THREADSTATS)</a></td>
<td>Devuelve un valor que indica si esta instancia es igual a otra instancia.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Devuelve el código hash de esta instancia. (Invalida <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>).</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Restar</a></td>
<td>Calcule la diferencia en las estadísticas entre dos JET_THREADSTATS estructura.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Obtiene una representación de cadena de este objeto . (Invalida <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="operators"></a>Operadores

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh163281(v=exchg.10).md">Suma</a></td>
<td>Agregue las estadísticas en dos estructuras JET_THREADSTATS datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Igualdad</a></td>
<td>Determina si dos instancias especificadas de JET_THREADSTATS son iguales.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Desigualdad</a></td>
<td>Determina si dos instancias especificadas de JET_THREADSTATS no son iguales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Resta</a></td>
<td>Calcule la diferencia en las estadísticas entre dos JET_THREADSTATS estructura.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_THREADSTATS estructura](./jet-threadstats-structure2.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
