---
description: 'Más información sobre: Propiedades boolColumnValue'
title: Propiedades boolColumnValue
TOCTitle: BoolColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BoolColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100954
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d338418b8855b8ba45e38b42f192cb7b1352f345f48e301eb78b1d0dc75534a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902276"
---
# <a name="boolcolumnvalue-properties"></a>Propiedades boolColumnValue

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo BoolColumnValue](./boolcolumnvalue-class.md) expone los miembros siguientes.

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
<td>Obtiene la longitud de bytes de un valor de columna, que es cero si column es NULL; de lo contrario, coincide con el tamaño de esta columna de tamaño fijo. (Se hereda de <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T). &gt; </a></td>
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
<td><a href="dn334107(v=exchg.10).md">Tamaño</a></td>
<td>Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binario y cadena). (Invalida <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valor</a></td>
<td>Obtiene o establece el valor de la estructura . (Se hereda de <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T). &gt; </a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334157(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtiene el último conjunto o valor recuperado de la columna. El valor se devuelve como un objeto genérico. (Invalida <a href="dn334226(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; . ValueAsObject</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase BoolColumnValue](./boolcolumnvalue-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
