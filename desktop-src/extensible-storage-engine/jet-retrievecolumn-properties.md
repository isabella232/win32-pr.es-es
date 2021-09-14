---
description: 'Más información sobre: propiedades JET_RETRIEVECOLUMN datos'
title: JET_RETRIEVECOLUMN propiedades
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962876"
---
# <a name="jet_retrievecolumn-properties"></a>JET_RETRIEVECOLUMN propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) tipo expone los miembros siguientes.

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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>Obtiene el tamaño, en bytes, de los datos recuperados por una operación de recuperación de columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Obtiene o establece el tamaño del búfer <a href="dn351040(v=exchg.10).md">pvData,</a> en bytes. La operación de recuperación de columna no almacenará más datos en pvData que cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>Obtiene o establece el identificador de columna para la columna que se va a recuperar.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Obtiene el columnid de la columna etiquetada, multivalor o dispersa cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">Err</a></td>
<td>Obtiene la advertencia devuelta de la recuperación de la columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece las opciones para la recuperación de columnas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>Obtiene o establece el desplazamiento en el búfer en el que se almacenarán los datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>Obtiene o establece el desplazamiento en el primer byte que se va a recuperar de una columna de tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> <a href="hh577895(v=exchg.10).md">o LongText</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Obtiene o establece el número de secuencia de los valores contenidos en una columna con varios valores. Si itagSequence es 0, se devuelve el número de instancias de una columna con varios valores en lugar de cualquier dato de columna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Obtiene o establece el búfer que almacenará los datos que se recuperan de la columna.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_RETRIEVECOLUMN clase](./jet-retrievecolumn-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
