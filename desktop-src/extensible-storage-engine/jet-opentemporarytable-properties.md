---
description: 'Más información sobre: JET_OPENTEMPORARYTABLE propiedades'
title: JET_OPENTEMPORARYTABLE propiedades (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbba2937283ab9a3d008d3bad04329d1fd42b84e0de4a1a42e2e100d99a03854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016725"
---
# <a name="jet_opentemporarytable-properties"></a>JET_OPENTEMPORARYTABLE propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expone los miembros siguientes.

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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtiene o establece el tamaño máximo de una clave que representa una fila determinada. El tamaño máximo de la clave se puede establecer para controlar cómo se truncan las claves. El truncamiento de claves es importante porque puede afectar cuando se considera que las filas son distintas. Si este parámetro se establece en 0 o 255, el tamaño máximo de clave y su semántica seguirán siendo idénticos al tamaño máximo de clave admitido por Windows Server 2003. Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la <a href="hh596135(v=exchg.10).md">instancia DatabasePageSize</a>. Vea <a href="dn335292(v=exchg.10).md">KeyMost para</a> obtener más información.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtiene o establece la cantidad máxima de datos que se usarán desde cualquier columna lengthcolumn variable para construir una clave para una fila determinada. Este parámetro se puede usar para controlar la cantidad de espacio de claves consumido por cualquier columna de clave determinada. Este límite está en bytes. Si este parámetro es cero o es el mismo que la <a href="dn335290(v=exchg.10).md">propiedad cbKeyMost,</a> no hay ningún límite en vigor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Obtiene o establece el número de columnas de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece opciones para la tabla temporal.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Obtiene o establece el identificador de configuración regional y las marcas de normalización que se usarán para comparar los datos de columna de clave Unicode de la tabla temporal. Cuando este parámetro es NULL, se usará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional del inglés de EE. UU. Cuando este parámetro es NULL, se usarán las marcas de normalización predeterminadas para comparar los datos de las columnas de clave Unicode de la tabla temporal. Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Obtiene o establece las definiciones de columna para las columnas creadas en la tabla temporal.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Obtiene o establece el búfer de salida que recibe la matriz de los id. de columna generados durante la creación de la tabla temporal. Los id. de columna de esta matriz se corresponderán exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">tableid</a></td>
<td>Obtiene el identificador de tabla para la tabla temporal creada como resultado de una llamada correcta a JetOpenTemporaryTable.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_OPENTEMPORARYTABLE clase](./jet-opentemporarytable-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
