---
description: 'Más información acerca de: JET_SETINFO propiedades'
title: Propiedades de JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154011"
---
# <a name="jet_setinfo-properties"></a>Propiedades de JET_SETINFO

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_SETINFO](./jet-setinfo-class.md) expone los siguientes miembros.

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
<td><a href="dn351064(v=exchg.10).md">ibLongValue</a></td>
<td>Obtiene o establece el desplazamiento del primer byte que se va a establecer en una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LongText</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351037(v=exchg.10).md">itagSequence</a></td>
<td>Obtiene o establece el número de secuencia del valor de una columna con varios valores que se va a establecer. La matriz de valores se basa en uno. El primer valor es Sequence 1, no 0 (cero). Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence si ese valor se va a reemplazar. Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_SETINFO (clase)](./jet-setinfo-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
