---
description: 'Más información acerca de: propiedades de UInt64ColumnValue'
title: Propiedades de UInt64ColumnValue
TOCTitle: UInt64ColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.UInt64ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55104184
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f713b07621f6f9e13e7f642f62b452ab7591a8a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361191"
---
# <a name="uint64columnvalue-properties"></a>Propiedades de UInt64ColumnValue

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo [UInt64ColumnValue](./uint64columnvalue-class.md) expone los siguientes miembros.

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
<td>Obtiene o establece el columnid que se va a establecer o recuperar. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error</a></td>
<td>Obtiene la advertencia generada al recuperar o establecer esta columna. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtiene o establece la secuencia de iTag de columnas. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Duración</a></td>
<td>Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con el tamaño de esta columna de tamaño fijo. (Se hereda <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtiene o establece las opciones de recuperación de columnas. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtiene o establece las opciones de actualización de la columna. (Se hereda de <a href="dn334206(v=exchg.10).md">ColumnValue</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><a href="dn351260(v=exchg.10).md">Tamaño</a></td>
<td>Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binary y String). (Invalida <a href="dn334172(v=exchg.10).md">ColumnValue. Size</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtiene o establece el valor de la estructura. (Se hereda <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtiene el último valor establecido o recuperado de la columna. El valor se devuelve como un objeto genérico. (Se hereda <a href="dn334171(v=exchg.10).md">de &lt; ColumnValueOfStruct &gt; T</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase UInt64ColumnValue](./uint64columnvalue-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
