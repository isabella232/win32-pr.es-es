---
description: 'Más información sobre: Propiedades columnvalue'
title: Propiedades de ColumnValue
TOCTitle: ColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100998
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 5a9819d052bc2142cdbae6caedbda6678dc54cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476032"
---
# <a name="columnvalue-properties"></a>Propiedades de ColumnValue

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo ColumnValue](./columnvalue-class.md) expone los miembros siguientes.

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
<td>Obtiene o establece el columnid que se va a establecer o recuperar.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error</a></td>
<td>Obtiene la advertencia generada al recuperar o establecer esta columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtiene o establece la secuencia de itag de columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334213(v=exchg.10).md">Duración</a></td>
<td>Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con el tamaño de las columnas de tamaño fijo y representa la longitud de bytes del valor real para las columnas de tamaño variable (es decir, binario y cadena). Para las cadenas, la longitud se determina en suposición de dos bytes por carácter.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtiene o establece las opciones de recuperación de columnas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtiene o establece las opciones de actualización de columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propiedad protegida" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Tamaño</a></td>
<td>Obtiene el tamaño del valor de la columna. Esto devuelve 0 para las columnas de tamaño variable (es decir, binario y cadena).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn334214(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtiene el último valor establecido o recuperado de la columna. El valor se devuelve como un objeto genérico.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[ColumnValue (clase)](./columnvalue-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
