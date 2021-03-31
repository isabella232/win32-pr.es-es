---
description: 'Más información acerca de: JET_ENUMCOLUMN propiedades'
title: Propiedades de JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907932"
---
# <a name="jet_enumcolumn-properties"></a>Propiedades de JET_ENUMCOLUMN

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expone los siguientes miembros.

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Obtiene el tamaño del valor que se enumeró para la columna. Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Obtiene el número de valores de columna enumerados para la columna. Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Obtiene el identificador de columnid que se enumeró.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">ERR</a></td>
<td>Obtiene el código de estado de la columna que es el resultado de la enumeración.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Obtiene el valor que se enumeró para la columna. Este miembro solo se utiliza si el valor de <a href="dn335086(v=exchg.10).md">Err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Esto apunta a la memoria asignada con la devolución de llamada de asignador <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> pasada a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. Recuerde liberar la memoria cuando termine.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Obtiene los valores de la columna enumerada para la columna. Este miembro solo se utiliza si <a href="dn335086(v=exchg.10).md">Err</a> no es <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN (clase)](./jet-enumcolumn-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
