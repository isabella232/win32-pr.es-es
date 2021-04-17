---
description: 'Más información acerca de: JET_OPENTEMPORARYTABLE propiedades'
title: Propiedades de JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562082"
---
# <a name="jet_opentemporarytable-properties"></a>Propiedades de JET_OPENTEMPORARYTABLE

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expone los siguientes miembros.

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
<td>Obtiene o establece el tamaño máximo para una clave que representa una fila determinada. Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves. El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas. Si este parámetro se establece en 0 o 255, el tamaño de clave máximo y su semántica permanecerán idénticos al tamaño máximo de clave admitido por Windows Server 2003. Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Vea <a href="dn335292(v=exchg.10).md">KeyMost</a> para obtener más información.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtiene o establece la cantidad máxima de datos que se usarán de cualquier variable lengthcolumn para construir una clave para una fila determinada. Este parámetro se puede utilizar para controlar la cantidad de espacio de clave consumida por una columna de clave determinada. Este límite se encuentra en bytes. Si este parámetro es cero o es igual que la propiedad <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , no se aplica ningún límite.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Obtiene o establece el número de columnas de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece las opciones de la tabla temporal.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Obtiene o establece el identificador de configuración regional y las marcas de normalización que se van a utilizar para comparar los datos de columna de clave Unicode en la tabla temporal. Cuando este parámetro es null, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional en Inglés de EE. UU. Cuando este parámetro es null, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal. Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Obtiene o establece las definiciones de columna para las columnas creadas en la tabla temporal.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Obtiene o establece el búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal. Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">TABLEID</a></td>
<td>Obtiene el identificador de tabla para la tabla temporal creada como resultado de una llamada correcta a JetOpenTemporaryTable.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_OPENTEMPORARYTABLE (clase)](./jet-opentemporarytable-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
