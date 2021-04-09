---
description: 'Más información acerca de: estructura de JET_SETCOLUMN'
title: Estructura de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809038"
---
# <a name="jet_setcolumn-structure"></a>Estructura de JET_SETCOLUMN


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>Estructura de JET_SETCOLUMN

La estructura **JET_SETCOLUMN** contiene los parámetros de entrada y salida de [JetSetColumns](./jetsetcolumns-function.md). Los campos de la estructura describen qué valor de columna se va a establecer, cómo se establece y dónde se obtienen los datos del conjunto de columnas.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Miembros

**columnid**

Identificador de columna de una columna que se va a establecer.

**pvData**

Puntero a los datos que se van a establecer en una columna.

**cbData**

Tamaño de la asignación, en bytes, que empieza en **pvData** en bytes.

**grbit**

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Anexa datos a una columna de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Se puede lograr el mismo comportamiento determinando el tamaño del valor Long existente y especificando <strong>ibLongValue</strong> en <strong>psetinfo</strong>. Sin embargo, es más fácil usar este <em>grbit</em>, ya que no es necesario conocer el tamaño del valor de la columna existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Reemplaza el valor Long existente por los nuevos datos. Cuando se usa esta opción, es como si el valor Long existente se hubiera establecido en la longitud 0 (cero) antes de establecer los datos nuevos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Interpreta el búfer de entrada como un número entero de bytes que se establecerá como la longitud del valor largo descrito por el columnid determinado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño dado es mayor que el valor de columna existente, la columna se extenderá con 0s. Si el tamaño es menor que el valor de la columna existente, el valor se truncará.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Establece un valor de longitud cero. Normalmente, un valor de columna se establece en NULL pasando un cbMax de 0. Sin embargo, para algunos tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valor de columna puede tener una longitud de 0 en lugar de NULL, y esta opción se usa para diferenciar entre NULL y 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Fuerza un valor Long, columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, que se almacenarán por separado del resto de datos de registro. Esto ocurre normalmente cuando el tamaño del valor Long impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar el almacenamiento del valor largo por separado. Tenga en cuenta que no se puede forzar la separación de los valores largos de cuatro bytes o de menor tamaño. En estos casos, se omite la opción.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Aplica valores distintos en una columna con varios valores. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Aplica valores distintos en una columna con varios valores. Esta opción compara la transformación normalizada de datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, no se pueden proporcionar también JET_bitSetAppendLv, JET_bitSetOverwriteLV y JET_bitSetSizeLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Hace que la columna devuelva el valor de columna predeterminado en operaciones de recuperación de columnas posteriores. Se quitan todos los valores de columna existentes. Esta opción solo es aplicable para columnas etiquetadas, dispersas o con varios valores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Mantiene el valor largo, las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o JET_coltypeLongBinary, que se almacenan con los datos de registro restantes si es posible. Normalmente, las columnas de tipo Long se almacenan por separado cuando su longitud supera los 1024 bytes o, de lo contrario, haría que la longitud del registro superara su límite de tamaño de página relacionado. Sin embargo, si se establece esta opción, la operación establecer columna producirá un error JET_errColumnTooBig en lugar de almacenar el valor de esta columna de forma independiente de los datos de registro restantes.</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md), o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Describe el número de secuencia de un valor en una columna con varios valores. Un valor de **itagSequence** de 0 indica que el conjunto de valores de columna debe agregarse como una nueva instancia de una columna con varios valores.

**ERR**

Códigos de error y advertencias devueltos por la operación establecer columna.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
