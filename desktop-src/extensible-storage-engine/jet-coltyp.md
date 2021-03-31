---
description: 'Más información acerca de: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
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
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912682"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_coltyp"></a>JET_COLTYP

El **JET_COLTYP** grupo de constantes describen todos los tipos de columna posibles que se pueden encontrar en una tabla.

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
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Un tipo de columna no válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Un tipo de columna que permite tres valores: <strong>true</strong>, <strong>false</strong>o <strong>null</strong>. Este tipo de columna tiene un byte de longitud y tiene un tamaño fijo. <strong>False</strong> se ordena antes que <strong>true</strong>. Tenga en cuenta que el tamaño de este tipo no coincide con el tamaño del tipo booleano Variant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Entero de 1 byte sin signo que puede tomar valores entre 0 (cero) y 255.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Entero de 2 bytes con signo que puede tomar valores entre-32768 y 32767. Los valores negativos se ordenan antes que los valores positivos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Entero de 4 bytes con signo que puede tomar valores entre-2147483648 y 2147483647. Los valores negativos se ordenan antes que los valores positivos.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Entero de 8 bytes con signo que puede tomar valores entre-9223372036854775808 y 9223372036854775807. Los valores negativos se ordenan antes que los valores positivos. Este tipo de columna es idéntico al tipo de divisa variante. Este tipo de columna también se puede utilizar como un entero de 8 bytes con signo nativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Número de punto flotante de precisión sencilla (4 bytes).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Número de punto flotante de doble precisión (8 bytes).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Número de punto flotante de doble precisión (8 bytes) que representa una fecha en días fraccionarios desde el año 1900. Este tipo de columna es idéntico al tipo de fecha Variant.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Columna binaria sin formato de longitud fija o variable que puede tener hasta 255 bytes de longitud.</p>
<p>Este tipo de columna se puede usar para implementar un GUID si se configura como una columna binaria de 16 bytes de longitud fija. La única ADVERTENCIA es que la ordenación relativa de los valores de un índice en una columna de este tipo no coincidirá con el orden relativo de la representación de la cadena del registro estándar de un GUID (es decir, &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Columna de texto de longitud fija o variable que puede tener hasta 255 caracteres ASCII de longitud o 127 caracteres Unicode de longitud.</p>
<p>Todas las cadenas se almacenan como un número de caracteres contado. No es necesario que las cadenas terminen en NULL. Además, no es necesario que el recuento incluya un terminador nulo. Por último, se pueden almacenar los caracteres nulos incrustados.</p>
<p>Las cadenas ASCII siempre se tratan como no distinguir mayúsculas de minúsculas para la ordenación y la búsqueda. Además, solo se tienen en cuenta los caracteres que preceden al primer carácter nulo (si existen) para la ordenación y la búsqueda.</p>
<p>Las cadenas Unicode usan la API de Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> para crear claves de ordenación que se utilizan posteriormente para ordenar y buscar los datos. De forma predeterminada, las cadenas Unicode se consideran en la configuración regional de Inglés de EE. UU. y se ordenan y se buscan mediante las siguientes marcas de normalización: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH. En Windows 2000, es posible personalizar estas marcas por índice para incluir también NORM_IGNORENONSPACE. En Windows XP y versiones posteriores, es posible solicitar cualquier combinación de las siguientes marcas de normalización por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH y SORT_STRINGSORT.</p>
<p>En todas las versiones, es posible personalizar la configuración regional por índice. Se puede usar cualquier configuración regional siempre que se haya instalado en el equipo el paquete de idioma adecuado. Por último, se omiten por completo cualquier carácter nulo que se encuentre en una cadena Unicode.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Columna binaria sin formato de longitud fija o variable que puede tener hasta 2147483647 bytes de longitud. Este tipo se considera un valor largo. Un valor largo es especial porque puede ser grande y porque se puede tener acceso a él como un flujo. De lo contrario, este tipo es idéntico a JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Columna de texto de longitud fija o variable que puede tener hasta 2147483647 caracteres ASCII de longitud o 1073741823 caracteres Unicode de longitud. Este tipo se considera un valor largo. Un valor largo es especial porque puede ser grande y porque se puede tener acceso a él como un flujo. De lo contrario, este tipo es idéntico a JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Este tipo de columna está obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Entero de 4 bytes sin signo que puede tomar valores entre 0 (cero) y 4294967295.</p>
<p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Entero de 8 bytes con signo que puede tomar valores entre-9223372036854775808 y 9223372036854775807. Los valores negativos se ordenan antes que los valores positivos.</p>
<p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Columna binaria de 16 bytes de longitud fija que representa de forma nativa el tipo de datos GUID. Los valores de las columnas GUID se ordenan de la misma manera en que esos valores se ordenarían como cadenas en formato estándar (es decir, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p>
<p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Entero de 2 bytes sin signo que puede tomar valores entre 0 y 65535.</p>
<p><strong>Windows Vista y Windows Server 2008:</strong>  Este tipo de columna es compatible con Windows Vista, Windows Server 2008 y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Constante que describe el tipo de columna máximo (es decir, uno más allá del mayor válido) admitido por el motor.</p>
<p>Este valor debe usarse con cuidado porque cambiará a medida que se admitan nuevos tipos de columna. Por ejemplo, tiene un valor literal diferente en Windows 2000 que en Windows XP y versiones posteriores.</p></td>
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


### <a name="see-also"></a>Consulte también

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
