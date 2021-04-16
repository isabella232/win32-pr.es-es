---
description: 'Más información acerca de: JET_ENUMCOLUMNID propiedades'
title: Propiedades de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540062"
---
# <a name="jet_enumcolumnid-properties"></a>Propiedades de JET_ENUMCOLUMNID

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expone los siguientes miembros.

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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>Obtiene o establece el identificador de columnid que se va a enumerar.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Obtiene o establece el recuento de valores de columna (por índice basado en uno) que se va a enumerar para el identificador de columna especificado. Si ctagSequence es 0 (cero), se omite rgtagSequence y se enumeran todos los valores de columna para el ID. de columna especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada. Un único elemento es un itagSequence que se define en JET_RETRIEVECOLUMN. Un valor de itagSequence de 0 (cero) significa &quot; SKIP &quot; . Un itagSequence de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMNID (clase)](./jet-enumcolumnid-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
