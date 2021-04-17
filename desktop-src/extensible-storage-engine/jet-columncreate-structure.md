---
description: 'Más información acerca de: estructura de JET_COLUMNCREATE'
title: Estructura de JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697404"
---
# <a name="jet_columncreate-structure"></a>Estructura de JET_COLUMNCREATE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_columncreate-structure"></a>Estructura de JET_COLUMNCREATE

La estructura **JET_COLUMNCREATE** describe una columna que se va a crear en una base de datos.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura, en bytes. Este campo debe inicializarse en **sizeof (JET_COLUMNCREATE)**.

**szColumnName**

Nombre de la columna que se va a crear. El nombre debe cumplir los siguientes criterios:

  - Debe tener menos de JET_cbNameMost caracteres de longitud, sin incluir el carácter NULL de terminación.

<!-- end list -->

  - Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de la a a la Z, de la a a la z y de todos los demás signos de puntuación, salvo el signo de exclamación ( \! ), la coma (,), el corchete de apertura () y el \[ corchete de cierre ( \] ), es decir, los caracteres ASCII 0x20, de 0x22

<!-- end list -->

  - No puede comenzar con un espacio.

<!-- end list -->

  - Debe contener al menos un carácter que no sea un espacio.

**coltyp**

El tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, vea [JET_COLTYP](./jet-coltyp.md).

**cbMax**

La longitud máxima, en bytes, de una columna de longitud variable. Longitud de la columna para las columnas de longitud fija.

**grbit**

Grupo de bits que contiene las opciones de esta estructura y que incluye cero o más de los valores siguientes.

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
<td><p>La columna es fija. Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se estén almacenando en la columna. No se puede usar JET_bitColumnFixed con JET_bitColumnTagged. Este bit no se puede usar con valores Long como <strong>JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La columna está etiquetada. Las columnas etiquetadas no ocupan espacio en la base de datos si no contienen datos. Este bit no se puede usar con JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La columna nunca se debe establecer en un valor NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La columna se incrementa automáticamente. El número es un número cada vez mayor y se garantiza que es único dentro de una tabla. Sin embargo, es posible que el número no sea continuo. Por ejemplo, si se insertan cinco filas en una tabla, la columna AutoIncrement puede contener los valores {1, 2, 6, 7, 8}.</p>
<p><strong>Windows 2000:  </strong> Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong>.</p>
<p><strong>Windows Server 2003 y versiones posteriores:  </strong> Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Este bit solo es válido en las llamadas a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican por el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>La columna es una columna de actualización de custodia. Una columna de actualización de custodia se puede actualizar simultáneamente en diferentes sesiones con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y mantener la coherencia transaccional.</p>
<ul>
<li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li>
<li><p>Una columna de actualización de custodia debe ser del tipo <strong>JET_coltypLong.</strong></p></li>
<li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es decir, <strong>cbDefault</strong> debe ser positivo).</p></li>
<li><p>JET_bitColumnEscrowUpdate no se pueden usar junto con las constantes siguientes:</p>
<ul>
<li><p>JET_bitColumnTagged</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La columna se crea sin una versión. Se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. No se puede utilizar dentro de una transacción.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize. JET_bitColumnFinalize especifica que una columna se puede finalizar. Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que llega a cero, se eliminará la fila. En su lugar, las versiones futuras pueden invocar una función de devolución de llamada. Para obtener más información, vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que se puede finalizar debe ser una columna de actualización de custodia. No se puede usar JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>La función de devolución de llamada, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>, proporciona el valor predeterminado de una columna. Una columna que tiene un valor predeterminado definido por el usuario debe ser una columna etiquetada. <strong>pvDefault</strong> debe apuntar a una estructura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p>
<p>JET_bitColumnUserDefinedDefault no se pueden usar junto con las constantes siguientes:</p>
<ul>
<li><p>JET_bitColumnFixed</p></li>
<li><p>JET_bitColumnNotNULL</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
<li><p>JET_bitColumnUpdatable</p></li>
<li><p>JET_bitColumnEscrowUpdate</p></li>
<li><p>JET_bitColumnFinalize</p></li>
<li><p>JET_bitColumnDeleteOnZero</p></li>
<li><p>JET_bitColumnMaybeNull</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La columna es una columna de actualización de custodia y, cuando llega a cero, se elimina el registro. Un uso común de una columna que se puede finalizar es usarlo como un campo de recuento de referencias y cuando el campo llega a cero, se elimina el registro. JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize. Una columna de eliminación en cero debe ser una columna de actualización de custodia. No se puede usar JET_bitColumnDeleteOnZero con JET_bitColumnFinalize. No se puede usar JET_bitColumnDeleteOnZero con columnas predeterminadas definidas por el usuario.</p></td>
</tr>
</tbody>
</table>


**pvDefault**

Apunta a un búfer que será el valor predeterminado de una columna. La longitud del búfer es **cbDefault**. Si no hay ningún valor predeterminado, **pvDefault** debe establecerse en NULL y **cbDefault** debe establecerse en cero. Si *grbit* ha establecido JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una estructura de JET_USERDEFINEDDEFAULT. Los valores predeterminados no pueden ser mayores de 255 bytes. Si un valor predeterminado es mayor que 255 bytes, se truncará silenciosamente.

**cbDefault**

Tamaño, en bytes, del búfer especificado por **pvDefault**.

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (Inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**columnid**

Si se ejecuta correctamente, el identificador de columna de la columna recién creada se devolverá en este campo. En caso de error, el valor es indefinido.

**ERR**

El campo **Err** contendrá el estado de creación de esta columna. Consulte [JetAddColumn](./jetaddcolumn-function.md) para obtener una lista de los valores devueltos probables.

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
<td><p>Se implementa como <strong>JET_COLUMNCREATE_W</strong> (Unicode) y <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
