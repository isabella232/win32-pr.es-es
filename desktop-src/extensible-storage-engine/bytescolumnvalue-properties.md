---
description: 'Más información sobre: Propiedades BytesColumnValue'
title: Propiedades BytesColumnValue
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7973f35a59af3cda2e8bb3bd400d2ef10e43e4f18fe9431f61ed50b62b343f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902111"
---
# <a name="bytescolumnvalue-properties"></a>Propiedades BytesColumnValue

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo BytesColumnValue](./bytescolumnvalue-class.md) expone los miembros siguientes.

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
<td>Obtiene el último conjunto o valor recuperado de la columna. El valor se devuelve como un objeto genérico. (Invalida <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase BytesColumnValue](./bytescolumnvalue-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
