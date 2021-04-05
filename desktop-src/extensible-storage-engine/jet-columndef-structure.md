---
description: 'Más información acerca de: estructura de JET_COLUMNDEF'
title: Estructura de JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003083"
---
# <a name="jet_columndef-structure"></a>Estructura de JET_COLUMNDEF


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_columndef-structure"></a>Estructura de JET_COLUMNDEF

La estructura **JET_COLUMNDEF** define los datos que se pueden almacenar en una columna.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura, en bytes. Debe establecerse en sizeof (JET_COLUMNDEF).

**columnid**

Reservado. **columnid** debe establecerse en 0 (cero).

**coltyp**

El tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. **wCountry** debe establecerse en 0 (cero).

**langid**

Obsoleto. **langid** debe establecerse en 0 (cero).

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**wCollate**

Reservado. **wCollate** debe establecerse en 0 (cero).

**cbMax**

La longitud máxima, en bytes, de una columna de longitud variable o la longitud de una columna de longitud fija.

**grbit**

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los valores siguientes.

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
<td><p>Se corregirá la columna. Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se estén almacenando en la columna. No se puede usar JET_bitColumnFixed con JET_bitColumnTagged. Este bit no se puede usar con valores Long (es decir <strong>JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La columna se etiquetará. Las columnas etiquetadas no ocupan espacio en la base de datos si no contienen datos. Este bit no se puede usar con JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La columna nunca se debe establecer en un valor NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La columna es una columna de versión que especifica la versión de la fila. El valor de esta columna comienza en cero y se incrementa automáticamente para cada actualización de la fila.</p>
<p>Este bit solo se puede aplicar a columnas de <strong>JET_coltypLong</strong> . Este bit no se puede usar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La columna se incrementará automáticamente. El número es un número cada vez mayor y se garantiza que es único dentro de una tabla. Sin embargo, los números podrían no ser continuos. Por ejemplo, si se insertan cinco filas en una tabla, la &quot; columna AutoIncrement &quot; puede contener los valores {1, 2, 6, 7, 8}. Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p>
<p><strong>Windows 2000:  </strong> En Windows 2000, este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican mediante un número denominado miembro <strong>itagSequence</strong> , que pertenece a varias estructuras, entre las que se incluyen: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>y <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Especifica que una columna es una columna de actualización de custodia. Una columna de actualización de custodia se puede actualizar simultáneamente mediante sesiones diferentes con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y mantendrá la coherencia transaccional. Una columna de actualización de custodia también debe cumplir las siguientes condiciones:</p>
<ul>
<li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li>
</ul>
<ul>
<li><p>Una columna de actualización de custodia debe ser del tipo <strong>JET_coltypLong</strong>.</p></li>
</ul>
<ul>
<li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</p></li>
</ul>
<ul>
<li><p>No se puede usar JET_bitColumnEscrowUpdate junto con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La columna se creará en una sin información de versión. Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. No se puede utilizar dentro de una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize. JET_bitColumnFinalize que se puede finalizar una columna. Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que llega a cero, se eliminará la fila. En su lugar, las versiones futuras podrían invocar una función de devolución de llamada (para obtener más información, vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Una columna que se puede finalizar debe ser una columna de actualización de custodia. No se puede usar JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>La función de devolución de llamada proporcionará el valor predeterminado de una columna. Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada. Especificar JET_bitColumnUserDefinedDefault significa que <strong>pvDefault</strong> debe apuntar a una estructura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p>
<ul>
<li><p>JET_bitColumnUserDefinedDefault no se pueden usar junto con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro. Un uso común de una columna que se puede finalizar es usarlo como un campo de recuento de referencias y cuando el campo llega a cero, se elimina el registro. JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize. Una columna de eliminación en cero debe ser una columna de actualización de custodia. No se puede usar JET_bitColumnDeleteOnZero con JET_bitColumnFinalize. No se puede usar JET_bitColumnDeleteOnZero con columnas predeterminadas definidas por el usuario.</p></td>
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

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
