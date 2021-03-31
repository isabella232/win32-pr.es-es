---
description: 'Más información sobre: constantes de configuración máxima'
title: Constantes de configuración máxima
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908111"
---
# <a name="maximum-settings-constants"></a>Constantes de configuración máxima


_**Se aplica a:** Windows | Windows Server_

## <a name="maximum-settings-constants"></a>Constantes de configuración máxima

Estas constantes proporcionan la configuración máxima que se permite en los elementos de una base de datos ESE.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante o valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Establece la longitud del prefijo utilizado para asignar nombre a los archivos utilizados por el motor de base de datos. Esta longitud es aplicable al nombre establecido para el parámetro del sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Establece la longitud máxima de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>Tamaño máximo predeterminado de un marcador. Es válido cuando el tamaño de la clave se deja en su valor predeterminado.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>El tamaño máximo de un marcador cuando esent está configurado para tener las claves más grandes posibles.</p>
<p><strong>Windows 7:</strong> JET_cbBookmarkMostMost se presenta en Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>La longitud máxima de un objeto, una columna, un índice o un nombre de propiedad.</p>
<p><strong>Nota:</strong>  Si es Unicode, el valor es 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>La longitud máxima de una &quot; construcción Name.Name.Name... &quot;</p>
<p><strong>Nota:</strong>  Si es Unicode, el valor es 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Este número se puede usar para calcular la cantidad máxima de un BLOB que el motor de base de datos puede almacenar en una sola página de base de datos. La fórmula es el tamaño máximo = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p>
<p>Este valor está ahora obsoleto. El tamaño del fragmento de valor largo debe recuperarse con el parámetro JET_paramLVChunkSizeMost.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>Tamaño máximo de los datos de columna que no son de valor largo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>Tamaño máximo de un valor predeterminado de la columna de valor largo (LongBinary o LongText).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>El tamaño máximo predeterminado de una clave de ordenación o de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>Tamaño máximo configurable de una clave de ordenación o de índice para cualquier tamaño de página. (Consulte JET_INDEXCREATE2. cbKeyMost)</p>
<p><strong>Windows 7:</strong> JET_cbKeyMostMost se introduce en el sistema operativo Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 2048 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage se introduce en el sistema operativo Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1000</p></td>
<td><p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 4096 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p>
<p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage se introduce en Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>El tamaño máximo configurable máximo permitido para una clave de índice en una base de datos con páginas de 8192 bytes. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage se introduce en Windows Vista</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>El tamaño máximo permitido mínimo para una clave de índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener más información.</p>
<p><strong>Windows Vista:  </strong> JET_cbKeyMostMin se introduce en Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>El tamaño máximo de la clave cuando se forma la clave mediante un límite <em>grbit</em>, como JET_bitStrLimit, que se usa en la función <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>Tamaño máximo del índice principal. Esto está ahora obsoleto.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>Tamaño máximo del índice secundario. Esto está ahora obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>Número máximo de componentes en una clave de ordenación o de índice.</p>
<p><strong>Windows Vista:  </strong> En Windows Vista y versiones posteriores de Windows, el valor es 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>Número máximo de columnas permitidas en una tabla.</p>
<p><strong>Windows XP:  </strong> El valor 0x0000fee0 se utiliza en Windows XP y versiones posteriores y versiones posteriores de Windows.</p>
<p><strong>Windows 2000:  </strong> El valor 0x00007ffe se utiliza en Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
detención</p></td>
<td><p>Número máximo de columnas fijas permitidas en una tabla; actualmente, 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>Número máximo de columnas de longitud variable que se pueden incluir en una tabla, actualmente 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000ff)</p></td>
<td><p>Número máximo de columnas etiquetadas que se pueden incluir en una tabla, actualmente 64993.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>

