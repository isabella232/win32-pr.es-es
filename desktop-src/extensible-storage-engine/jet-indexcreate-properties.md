---
description: 'Más información sobre: propiedades JET_INDEXCREATE datos'
title: JET_INDEXCREATE propiedades
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269767"
---
# <a name="jet_indexcreate-properties"></a>JET_INDEXCREATE propiedades

Incluir miembros protegidos  
Incluir miembros heredados  

El [JET_INDEXCREATE](./jet-indexcreate-class.md) muestra los miembros siguientes.

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
<td>Obtiene o establece la longitud, en caracteres, de szKey, incluidos los dos valores NULL finales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice. El tamaño máximo de clave mínimo admitido es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado. El tamaño máximo de clave depende del tamaño de página de la base de <a href="hh596135(v=exchg.10).md">datos DatabasePageSize.</a> El tamaño máximo de clave se puede recuperar con <a href="dn351156(v=exchg.10).md">KeyMost.</a> Este parámetro se omite en Windows XP y Windows Server 2003. A diferencia de la API no administrada, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) no es necesario, se agregará automáticamente.</td>
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
<td><a href="dn335157(v=exchg.10).md">Err</a></td>
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
<td>Obtiene o establece las opciones de comparación unicode opcionales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtiene o establece sugerencias de asignación, mantenimiento y uso de espacio.</td>
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
<td>Obtiene o establece la descripción de la clave de índice. Se trata de una cadena doble terminada en NULL de tokens delimitados por NULL. Cada token tiene el formato [direction-specifier][column-name], donde direction-specification es &quot; + &quot; o &quot; - &quot; . Por ejemplo, un szKey de &quot; +abc\0-def\0+ghi\0 indexará las tres columnas abc (en orden &quot; &quot; &quot; ascendente), def (en orden descendente) y &quot; &quot; &quot; ghi &quot; (en orden ascendente).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Obtiene o establece la densidad del índice.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[JET_INDEXCREATE clase](./jet-indexcreate-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
