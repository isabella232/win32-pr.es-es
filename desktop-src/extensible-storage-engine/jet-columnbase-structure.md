---
description: 'Más información acerca de: estructura de JET_COLUMNBASE'
title: Estructura de JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678505"
---
# <a name="jet_columnbase-structure"></a>Estructura de JET_COLUMNBASE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>Estructura de JET_COLUMNBASE

La estructura **JET_COLUMNBASE** describe los parámetros de una columna base. Las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usan la estructura **JET_COLUMNBASE** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura, en bytes. Establezca **cbStruct** en sizeof (JET_COLUMNBASE).

**columnid**

Reservado. Establezca **columnid** en 0 (cero).

**coltyp**

El tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. Se establece en 0 (cero).

**langid**

Reservado. Se establece en 0 (cero).

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**wFiller**

Reservado. Se establece en 0 (cero).

**cbMax**

La longitud máxima, en bytes, de una columna de longitud variable, o la longitud real, en bytes, de una columna de longitud fija.

**grbit**

Opciones de la columna, incluidos cero o más de los valores siguientes.

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
<td><p>JET_bitColumnFixed</p></td>
<td><p>La columna es fija y ocupa la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que contenga. JET_bitColumnFixed no se pueden combinar con JET_bitColumnTagged y no se pueden usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLongText</strong> o <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La columna está etiquetada y ocupa espacio en la base de datos solo si contiene datos. JET_bitColumnTagged no se pueden combinar con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La columna no se debe establecer en un valor <strong>null</strong> .</p>
<p>JET_bitColumnNotNULL no se pueden combinar con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La columna es una columna de versión que especifica la versión de la fila. El valor de esta columna comienza en cero y se incrementa automáticamente para cada actualización de la fila.</p>
<p>JET_bitColumnVersion solo se puede usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong> y no se puede combinar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La columna se incrementa automáticamente. El número es un número cada vez mayor y se garantiza que es único dentro de una tabla. Sin embargo, los números no pueden ser secuenciales. Por ejemplo, si se insertan cinco filas en una tabla, la columna incrementada automáticamente puede contener los valores {1, 2, 6, 7, 8}.</p>
<p>JET_bitColumnAutoincrement solo se puede usar cuando el miembro <strong>coltyp</strong> se establece en <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong> y no se puede combinar con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o JET_bitColumnVersion.</p>
<p><strong>Windows 2000:  </strong> JET_bitColumnVersion solo se puede usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Válido solo para llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>. JET_bitColumnUpdatable no se pueden combinar con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Solo es válido en las llamadas a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican por un número en el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben ser columnas etiquetadas; es decir, puede que no sean columnas de longitud fija o de longitud variable.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Especifica que una columna es una columna de actualización de custodia que se puede actualizar simultáneamente mediante sesiones diferentes con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y tendrá coherencia transaccional.</p>
<ul>
<li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li>
</ul>
<ul>
<li><p>En el caso de una columna de actualización de custodia, el miembro <strong>coltyp</strong> debe establecerse en <strong>JET_coltypLong.</strong></p></li>
</ul>
<ul>
<li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate no se pueden combinar con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La columna se crea sin un número de versión. Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. JET_bitColumnUnversioned solo se usa con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. No se puede utilizar dentro de una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Reservado para uso futuro.</p>
<p>JET_bitColumnMaybeNull no se pueden combinar con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>No debe usarse. En su lugar, use JET_bitColumnDeleteOnZero.</p>
<p>La columna se puede finalizar. Una columna que se puede finalizar es una columna de actualización de custodia que hace que se elimine la fila cuando la columna llega a cero. En su lugar, las versiones futuras pueden invocar una función de devolución de llamada (vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Una columna que se puede finalizar debe ser una columna de actualización de custodia. JET_bitColumnFinalize no se pueden combinar con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>La función de devolución de llamada proporcionará el valor predeterminado de una columna. Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada. Si se especifica JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> debe apuntar a una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof (JET_USERDEFINEDDEFAULT).</p>
<p>JET_bitColumnUserDefinedDefault no se pueden combinar con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro. Un uso común de las columnas delete-on-Zero es como campos de recuento de referencias. Cuando el número de referencias llega a cero, se elimina el registro. Una columna de eliminación en cero debe ser una columna de actualización de custodia.</p>
<p>JET_bitColumnDeleteOnZero reemplaza JET_bitColumnFinalize.</p>
<p>JET_bitColumnDeleteOnZero no se pueden combinar con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault, y no se pueden usar con columnas predeterminadas definidas por el usuario.</p></td>
</tr>
</tbody>
</table>


**szBaseTableName**

Tabla de la que la tabla actual hereda su DDL.

**szBaseColumnName**

Nombre de la columna de la tabla de plantilla.

### <a name="remarks"></a>Observaciones

**JET_COLUMNBASE** contiene gran parte de la misma información que [JET_COLUMNDEF](./jet-columndef-structure.md), pero agrega campos de cadena para describir la tabla base (si se ha utilizado un DDL jerárquico).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_COLUMNBASE_W</strong> (Unicode) y <strong>JET_COLUMNBASE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
