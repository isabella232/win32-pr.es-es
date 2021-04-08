---
description: 'Más información acerca de: JET_INDEXCREATE propiedades'
title: Propiedades de JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002809"
---
# <a name="jet_indexcreate-properties"></a>Propiedades de JET_INDEXCREATE

Incluir miembros protegidos  
Incluir miembros heredados  

El tipo de [JET_INDEXCREATE](./jet-indexcreate-class.md) expone los siguientes miembros.

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Obtiene o establece la longitud, en caracteres, de szKey, incluidos los dos valores NULL de terminación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice. El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado. El tamaño máximo de la clave depende del tamaño de página de la base de datos <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. El tamaño máximo de la clave se puede recuperar con <a href="dn351156(v=exchg.10).md">KeyMost</a>. Este parámetro se omite en Windows XP y Windows Server 2003. A diferencia de la API no administrada, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) no es necesario, sino que se agregará automáticamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtiene o establece la longitud máxima, en bytes, de cada columna que se va a almacenar en el índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Obtiene o establece el número de columnas condicionales.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">ERR</a></td>
<td>Obtiene o establece el código de error de la creación de este índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Obtiene o establece las opciones de creación de índices.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Obtiene o establece las opciones de comparación Unicode opcionales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtiene o establece las sugerencias de asignación, mantenimiento y uso de espacio.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Obtiene o establece las columnas condicionales opcionales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Obtiene o establece el nombre del índice que se va a crear.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Obtiene o establece la descripción de la clave de índice. Se trata de una cadena doble terminada en NULL de tokens delimitados por null. Cada token tiene la forma [Direction-Specifier] [column-Name], donde Direction-Specification es &quot; + &quot; o &quot; - &quot; . por ejemplo, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexará las tres columnas &quot; ABC &quot; (en orden ascendente), &quot; Def &quot; (en orden descendente) y &quot; GHI &quot; (en orden ascendente).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Obtiene o establece la densidad del índice.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_INDEXCREATE (clase)](./jet-indexcreate-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
