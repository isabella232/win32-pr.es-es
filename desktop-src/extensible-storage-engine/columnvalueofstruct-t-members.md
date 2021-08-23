---
description: 'Más información sobre: Miembros <T> ColumnValueOfStruct'
title: Miembros ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334217(v=EXCHG.10)
ms:contentKeyID: 55101002
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 290a6180765992b23a386bb36ba4d5be85efaf1183875eeca0b02543bb1f1c08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042353"
---
# <a name="columnvalueofstructt-members"></a>Miembros \<T\> ColumnValueOfStruct

Incluir miembros protegidos  
Incluir miembros heredados  

Establezca una columna de un tipo de estructura (por ejemplo, Int32/Guid).

El [tipo ColumnValueOfStruct \<T\> ](./columnvalueofstruct-t-class.md) expone los miembros siguientes.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn334175(v=exchg.10).md">ColumnValueOfStruct &lt; T&gt;</a></td>
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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Obtiene o establece el columnid que se va a establecer o recuperar. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error</a></td>
<td>Obtiene la advertencia generada al recuperar o establecer esta columna. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtiene o establece la secuencia de itag de columna. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Duración</a></td>
<td>Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es NULL; de lo contrario, coincide con el tamaño de esta columna de tamaño fijo. (Invalida <a href="dn334213(v=exchg.10).md">ColumnValue.Length</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtiene o establece las opciones de recuperación de columnas. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtiene o establece las opciones de actualización de columna. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Tamaño</a></td>
<td>Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binario y cadena). (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtiene o establece el valor de la estructura .</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtiene el último valor establecido o recuperado de la columna. El valor se devuelve como un objeto genérico. (Invalida <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject</a>).</td>
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
<td><a href="dn334178(v=exchg.10).md">CheckDataCount</a></td>
<td>Asegúrese de que los datos recuperados son exactamente el tamaño necesario para la estructura. Se produce una excepción si hay un error de coincidencia.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn334208(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334223(v=exchg.10).md">ToString</a></td>
<td>Obtiene una representación de cadena de este objeto . (Invalida <a href="dn334163(v=exchg.10).md">ColumnValue.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[ColumnValueOfStruct \<T\> (clase)](./columnvalueofstruct-t-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
