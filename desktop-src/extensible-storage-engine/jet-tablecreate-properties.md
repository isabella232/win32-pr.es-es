---
description: 'Más información sobre: JET_TABLECREATE propiedades'
title: JET_TABLECREATE propiedades
TOCTitle: JET_TABLECREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103995
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6f5802c42bbf32548e1d42e507013fc0235eafdd1bd989b75f628b43a1b327eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252159"
---
# <a name="jet_tablecreate-properties"></a>JET_TABLECREATE propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_TABLECREATE](./jet-tablecreate-class.md) expone los miembros siguientes.

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
<td><a href="dn351077(v=exchg.10).md">cbSeparateLV</a></td>
<td>Obtiene o establece el tamaño heurístico para separar un LV intrínseco del registro principal.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">cbtyp</a></td>
<td>Obtiene o establece un tipo de la función de devolución de llamada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">cColumns</a></td>
<td>Obtiene o establece el número de columnas que se crearán.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">cCreated</a></td>
<td>Obtiene o establece el recuento de objetos creados (columnas+tabla+índices+devoluciones de llamada).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">cIndexes</a></td>
<td>Obtiene o establece el número de índices que se crearán.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece las opciones de tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">pLVSpacehints</a></td>
<td>Obtiene o establece sugerencias de asignación, mantenimiento y uso de espacio para el árbol lv separado, de <a href="dn351095(v=exchg.10).md">tipo JET_SPACEHINTS</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">pSeqSpacehints</a></td>
<td>Obtiene o establece sugerencias de asignación, mantenimiento y uso de espacio para el índice secuencial predeterminado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">rgcolumncreate</a></td>
<td>Obtiene o establece una matriz de información de creación de columnas, de tipo <a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">rgindexcreate</a></td>
<td>Obtiene o establece una matriz de índices que se va a crear, de <a href="dn335112(v=exchg.10).md">tipo JET_INDEXCREATE</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">szCallback</a></td>
<td>Obtiene o establece una función de devolución de llamada que se va a usar para la tabla. Esto tiene el formato &quot; module!functionName &quot; y supone código no administrado. Consulte <strong>JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</strong> para obtener una alternativa.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">szTableName</a></td>
<td>Obtiene o establece el nombre de la tabla que se va a crear.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">szTemplateTableName</a></td>
<td>Obtiene o establece el nombre de la tabla de la que se va a heredar el DDL base.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">tableid</a></td>
<td>Obtiene o establece el tabledid devuelto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">ulDensity</a></td>
<td>Obtiene o establece la densidad de la tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">ulPages</a></td>
<td>Obtiene o establece las páginas iniciales que se asignarán a la tabla.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_TABLECREATE clase](./jet-tablecreate-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
