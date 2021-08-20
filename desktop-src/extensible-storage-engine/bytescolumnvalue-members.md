---
description: 'Más información sobre: Miembros BytesColumnValue'
title: Miembros BytesColumnValue
TOCTitle: BytesColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100914
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b5c82031298f5cf1bee82e424401bb8994a414353c1ccd04cb8aa0fbb75ac557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084171"
---
# <a name="bytescolumnvalue-members"></a>Miembros BytesColumnValue

Incluir miembros protegidos  
Incluir miembros heredados  

Valor de columna de matriz de bytes.

El [tipo BytesColumnValue](./bytescolumnvalue-class.md) expone los miembros siguientes.

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
<td><a href="dn334168(v=exchg.10).md">BytesColumnValue</a></td>
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
<td><a href="dn334126(v=exchg.10).md">Duración</a></td>
<td>Obtiene la longitud de bytes de un valor de columna, que es cero si column es NULL; de lo contrario, coincide con la longitud real de la matriz de bytes. (Invalida <a href="dn334213(v=exchg.10).md">ColumnValue.Length</a>).</td>
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
<td><a href="dn334176(v=exchg.10).md">Tamaño</a></td>
<td>Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binario y cadena). (Invalida <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Valor</a></td>
<td>Obtiene o establece el valor de la columna. Use <a href="dn334138(v=exchg.10).md">SetColumns(JET_SESID, JET_TABLEID, []) para</a> actualizar un registro con el valor de columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">ValueAsObject</a></td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
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
<td><a href="dn334173(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue. (Invalida <a href="dn334208(v=exchg.10).md">ColumnValue.GetValueFromBytes([], Int32, Int32, Int32)</a>).)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334124(v=exchg.10).md">ToString</a></td>
<td>Devuelve un <a href="/dotnet/api/system.string">objeto String</a> que representa el <a href="dn334170(v=exchg.10).md">objeto BytesColumnValue actual.</a> (Invalida <a href="dn334163(v=exchg.10).md">ColumnValue.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase BytesColumnValue](./bytescolumnvalue-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
