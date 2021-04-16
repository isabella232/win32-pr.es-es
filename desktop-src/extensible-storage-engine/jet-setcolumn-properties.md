---
description: 'Más información acerca de: JET_SETCOLUMN propiedades'
title: Propiedades de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103854
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 43f005ce4edb909e842566e43b9b74ed80471c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497116"
---
# <a name="jet_setcolumn-properties"></a>Propiedades de JET_SETCOLUMN

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_SETCOLUMN](./jet-setcolumn-class.md) expone los siguientes miembros.

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
<td><a href="dn335266(v=exchg.10).md">cbData</a></td>
<td>Obtiene o establece el tamaño de los datos que se van a establecer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335268(v=exchg.10).md">columnid</a></td>
<td>Obtiene o establece el identificador de columna de una columna que se va a establecer.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335269(v=exchg.10).md">ERR</a></td>
<td>Obtiene el código de error o la advertencia devuelta por la operación de conjunto de columnas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335270(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece las opciones para la operación de establecer columna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335271(v=exchg.10).md">ibData</a></td>
<td>Obtiene o establece el desplazamiento de los datos que se van a establecer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335272(v=exchg.10).md">ibLongValue</a></td>
<td>Obtiene o establece el desplazamiento del primer byte que se va a establecer en una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335273(v=exchg.10).md">itagSequence</a></td>
<td>Obtiene o establece el número de secuencia del valor de una columna con varios valores que se va a establecer. La matriz de valores se basa en uno. El primer valor es Sequence 1, no 0 (cero). Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence si ese valor se va a reemplazar. Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351058(v=exchg.10).md">pvData</a></td>
<td>Obtiene o establece un puntero a los datos que se van a establecer.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_SETCOLUMN (clase)](./jet-setcolumn-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
