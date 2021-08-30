---
description: 'Más información sobre: JET_COLUMNCREATE estructura'
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
ms.openlocfilehash: 93664c518b8a63651fc0b93cba6f050e9fea5586
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477182"
---
# <a name="jet_columncreate-structure"></a>Estructura de JET_COLUMNCREATE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_columncreate-structure"></a>Estructura de JET_COLUMNCREATE

La **JET_COLUMNCREATE** describe una columna para crear en una base de datos.

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

Tamaño de la estructura, en bytes. Este campo debe inicializarse en **sizeof( JET_COLUMNCREATE )**.

**szColumnName**

Nombre de la columna que se creará. El nombre debe cumplir los criterios siguientes:

  - Debe tener menos de JET_cbNameMost de longitud, sin incluir el valor NULL final.

<!-- end list -->

  - Solo debe contener caracteres de los siguientes conjuntos: de 0 a 9, de la A a la Z, de la a la z y de todos los demás signos de puntuación, excepto el signo de exclamación ( ), la coma (,), el corchete de apertura ( ) y el corchete de cierre (), es decir, los caracteres ASCII 0x20, 0x22 a través de 0x2d, 0x2f a \! \[ \] 0x5a, 0x5c, 0x5d a 0x7f.

<!-- end list -->

  - No puede comenzar con un espacio.

<!-- end list -->

  - Debe contener al menos un carácter que no sea de espacio.

**coltyp**

Tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, [vea JET_COLTYP](./jet-coltyp.md).

**cbMax**

Longitud máxima, en bytes, de una columna de longitud variable. Longitud de la columna para las columnas de longitud fija.

**grbit**

Grupo de bits que contienen las opciones de esta estructura y que incluyen cero o más de los valores siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La columna es fija. Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se almacenen en la columna. JET_bitColumnFixed se puede usar con JET_bitColumnTagged. Este bit no se puede usar con valores <strong>largos, como JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La columna está etiquetada. Las columnas etiquetadas no ocupa ningún espacio en la base de datos si no contienen datos. Este bit no se puede usar con JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La columna nunca debe establecerse en un valor NULL.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La columna se incrementa automáticamente. El número es un número creciente y se garantiza que es único dentro de una tabla. Sin embargo, es posible que el número no sea continuo. Por ejemplo, si se insertan cinco filas en una tabla, la columna de autoincremento podría contener los valores { 1, 2, 6, 7, 8 }.</p><p><strong>Windows 2000:</strong> Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong>.</p><p><strong>Windows Server 2003 y versiones posteriores:</strong> Este bit solo se puede usar en columnas de <strong>tipo JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Este bit solo es válido en las llamadas <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a></p> | 
| <p>JET_bitColumnTTKey</p> | <p>Este bit solo es válido en las llamadas <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Este bit solo es válido en las llamadas <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican mediante el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben etiquetarse como columnas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>La columna es una columna de actualización de custodia. Diferentes sesiones con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> pueden actualizar simultáneamente una columna de actualización de custodia y mantener la coherencia transaccional.</p><ul><li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li><li><p>Una columna de actualización de custodia debe ser de <strong>tipo JET_coltypLong.</strong></p></li><li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es <strong>decir, cbDefault</strong> debe ser positivo).</p></li><li><p>JET_bitColumnEscrowUpdate se puede usar junto con las siguientes constantes:</p><ul><li><p>JET_bitColumnTagged</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li></ul></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La columna se crea sin una versión. Se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn.</a> No se puede usar dentro de una transacción.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize. JET_bitColumnFinalize especifica que se puede finalizar una columna. Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que alcanza cero, se eliminará la fila. En su lugar, las versiones futuras pueden invocar una función de devolución de llamada. Para obtener más información, <a href="gg294098(v=exchg.10).md">vea JET_CALLBACK</a>. Una columna que se puede finalizar debe ser una columna de actualización de custodia. JET_bitColumnFinalize se puede usar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>El valor predeterminado de una columna lo proporciona la función de devolución de llamada , <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que tenga un valor predeterminado definido por el usuario debe ser una columna etiquetada. <strong>pvDefault</strong> debe apuntar a una <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> estructura y <strong>cbDefault</strong> debe establecerse en sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p><p>JET_bitColumnUserDefinedDefault se puede usar junto con las siguientes constantes:</p><ul><li><p>JET_bitColumnFixed</p></li><li><p>JET_bitColumnNotNULL</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li><li><p>JET_bitColumnUpdatable</p></li><li><p>JET_bitColumnEscrowUpdate</p></li><li><p>JET_bitColumnFinalize</p></li><li><p>JET_bitColumnDeleteOnZero</p></li><li><p>JET_bitColumnMaybeNull</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La columna es una columna de actualización de custodia y, cuando llegue a cero, se eliminará el registro. Un uso común para una columna que se puede finalizar es usarla como campo de recuento de referencias y, cuando el campo alcanza cero, se elimina el registro. JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize. Una columna delete-on-zero debe ser una columna de actualización de custodia. JET_bitColumnDeleteOnZero se puede usar con JET_bitColumnFinalize. JET_bitColumnDeleteOnZero no se puede usar con columnas predeterminadas definidas por el usuario.</p> | 



**pvDefault**

Apunta a un búfer que será el valor predeterminado de una columna. La longitud del búfer es **cbDefault.** Si no hay ningún valor predeterminado, **pvDefault** debe establecerse en NULL y **cbDefault** debe establecerse en cero. Si *grbit* tiene JET_bitColumnUserDefinedDefault, **pvDefault** se interpretará como un puntero a una JET_USERDEFINEDDEFAULT estructura. Los valores predeterminados no pueden tener más de 255 bytes. Si un valor predeterminado es mayor que 255 bytes, se truncará en modo silencioso.

**cbDefault**

Tamaño, en bytes, del búfer especificado por **pvDefault**.

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**columnid**

Si se ejecuta correctamente, el identificador de columna de la columna recién creada se pasará de nuevo en este campo. En caso de error, el valor es indefinido.

**Err**

El **campo err** contendrá el estado de creación de esta columna. Consulte [JetAddColumn para](./jetaddcolumn-function.md) obtener una lista de valores devueltos probables.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_COLUMNCREATE_W</strong> (Unicode) <strong>y JET_COLUMNCREATE_A</strong> (ANSI).</p> | 



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
