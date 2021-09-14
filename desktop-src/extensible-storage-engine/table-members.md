---
description: 'Más información sobre: Miembros de tabla'
title: 'Miembros de Table '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969011"
---
# <a name="table-members"></a>Miembros de Table 

Incluir miembros protegidos  
Incluir miembros heredados  

Clase que encapsula un JET_TABLEID en un objeto descartable. Se abrirá una tabla existente. Para crear una tabla, use el método JetCreateTable.

El [tipo](./table-class.md) Table expone los miembros siguientes.

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
<td><a href="dn351234(v=exchg.10).md">Tabla</a></td>
<td>Inicializa una nueva instancia de la clase Table. La tabla se abre desde la base de datos especificada.</td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>Obtiene un valor que indica si el recurso subyacente está asignado actualmente. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351171(v=exchg.10).md">JetTableid</a></td>
<td>Obtiene el JET_TABLEID que contiene esta tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351170(v=exchg.10).md">Nombre</a></td>
<td>Obtiene el nombre de esta tabla.</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Produce una excepción si se ha eliminado este objeto. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn351235(v=exchg.10).md">Cerrar</a></td>
<td>Cierre la tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose()</a></td>
<td>Elimine este objeto y libere el recurso subyacente de Esent. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></td>
<td>Lo llaman Dispose y el finalizador. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalizar</a></td>
<td>Finalizará una instancia de la clase EsentResource. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn351168(v=exchg.10).md">ReleaseResource</a></td>
<td>Liberar el valor JET_TABLEID. (Invalida <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Lo llama una subclase cuando se asigna un recurso. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Lo llama una subclase cuando se libera un recurso. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn351237(v=exchg.10).md">ToString</a></td>
<td>Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa la tabla <a href="dn351163(v=exchg.10).md">actual.</a> (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
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
<td><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></td>
<td>Operador de conversión implícita de una tabla a un JET_TABLEID. Esto permite usar una tabla con API que esperan un JET_TABLEID.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Table (clase)](./table-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
