---
description: 'Más información acerca de: JET_ENUMCOLUMN miembros'
title: Miembros de JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559712"
---
# <a name="jet_enumcolumn-members"></a>Miembros de JET_ENUMCOLUMN

Incluir miembros protegidos  
Incluir miembros heredados  

Enumera los valores de columna de un registro mediante la función JetEnumerateColumns. JetEnumerateColumns devuelve una matriz de estructuras JET_ENUMCOLUMNVALUE. La matriz se devuelve en memoria que se asignó mediante la devolución de llamada que se proporcionó a esa función.

El tipo de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expone los siguientes miembros.

## <a name="constructors"></a>Constructores

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
<td><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></td>
<td></td>
</tr>
</tbody>
</table>


Superior

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Obtiene el tamaño del valor que se enumeró para la columna. Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Obtiene el número de valores de columna enumerados para la columna. Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Obtiene el identificador de columnid que se enumeró.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">ERR</a></td>
<td>Obtiene el código de estado de la columna que es el resultado de la enumeración.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Obtiene el valor que se enumeró para la columna. Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Esto apunta a la memoria asignada con la devolución de llamada de asignador <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> pasada a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. Recuerde liberar la memoria cuando termine.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Obtiene los valores de la columna enumerada para la columna. Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
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
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335132(v=exchg.10).md">ToString</a></td>
<td>Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>actual. (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN (clase)](./jet-enumcolumn-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
