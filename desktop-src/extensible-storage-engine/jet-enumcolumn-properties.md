---
description: 'Más información sobre: JET_ENUMCOLUMN propiedades'
title: JET_ENUMCOLUMN propiedades
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ee11c050d558fbefb15be4783a08b1808744718d043de038b297fdc5ebd9e3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667925"
---
# <a name="jet_enumcolumn-properties"></a>JET_ENUMCOLUMN propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expone los miembros siguientes.

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
<td>Obtiene el tamaño del valor enumerado para la columna. Este miembro solo se usa si <a href="dn335086(v=exchg.10).md">err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Obtiene el número de valores de columna enumerados para la columna. Este miembro solo se usa si <a href="dn335086(v=exchg.10).md">err</a> no <a href="hh557250(v=exchg.10).md">es ColumnSingleValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Obtiene el identificador de columnid que se enumeró.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Obtiene el código de estado de columna que resulta de la enumeración .</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Obtiene el valor enumerado para la columna. Este miembro solo se usa si <a href="dn335086(v=exchg.10).md">err</a> es igual a <a href="hh557250(v=exchg.10).md">ColumnSingleValue.</a> Esto apunta a la memoria asignada con la devolución de llamada del asignador de JET_PFNREALLOC pasada <a href="hh566077(v=exchg.10).md">a</a> <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit).</a> No olvide liberar la memoria cuando haya terminado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Obtiene los valores de columna enumerados para la columna. Este miembro solo se usa si <a href="dn335086(v=exchg.10).md">err</a> no <a href="hh557250(v=exchg.10).md">es ColumnSingleValue.</a></td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_ENUMCOLUMN clase](./jet-enumcolumn-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
