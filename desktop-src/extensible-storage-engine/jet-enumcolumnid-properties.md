---
description: 'Más información sobre: JET_ENUMCOLUMNID propiedades'
title: JET_ENUMCOLUMNID propiedades
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240741"
---
# <a name="jet_enumcolumnid-properties"></a>JET_ENUMCOLUMNID propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) muestra los miembros siguientes.

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
<td>Obtiene o establece el recuento de valores de columna (por índice basado en uno) que se va a enumerar para el identificador de columna especificado. Si ctagSequence es 0 (cero), se omite rgtagSequence y se enumerarán todos los valores de columna para el identificador de columna especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Obtiene o establece la matriz de índices basados en uno en la matriz de valores de columna de una columna determinada. Un único elemento es una itagSequence que se define en JET_RETRIEVECOLUMN. Una itagSequence de 0 (cero) significa &quot; omitir &quot; . Una itagSequence de 1 significa devolver el primer valor de columna de la columna, 2 significa la segunda, y así sucesivamente.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMNID clase](./jet-enumcolumnid-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
