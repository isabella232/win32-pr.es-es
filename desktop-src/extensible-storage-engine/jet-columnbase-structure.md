---
description: 'Más información sobre: JET_COLUMNBASE estructura'
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
ms.openlocfilehash: 603025166eed7c92d98148a43d26046308235777
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983598"
---
# <a name="jet_columnbase-structure"></a>Estructura de JET_COLUMNBASE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_columnbase-structure"></a>Estructura de JET_COLUMNBASE

La **JET_COLUMNBASE** describe los parámetros de una columna base. Las [funciones JetGetColumnInfo](./jetgetcolumninfo-function.md) [y JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usan **JET_COLUMNBASE** estructura .

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

Tamaño de esta estructura, en bytes. Establezca **cbStruct** en sizeof( JET_COLUMNBASE ).

**columnid**

Reservado. Establezca **columnid** en 0 (cero).

**coltyp**

Tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, [vea JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. Establezca en 0 (cero).

**langid**

Reservado. Establezca en 0 (cero).

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**wFiller**

Reservado. Establezca en 0 (cero).

**cbMax**

La longitud máxima, en bytes, de una columna de longitud variable o la longitud real, en bytes, de una columna de longitud fija.

**grbit**

Opciones para la columna, incluidos cero o más de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La columna es fija y ocupa la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que contenga. JET_bitColumnFixed se puede combinar con JET_bitColumnTagged y no se puede usar cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLongText</strong> o <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La columna se etiqueta y ocupa espacio en la base de datos solo si contiene datos. JET_bitColumnTagged se pueden combinar con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La columna no debe establecerse en un <strong>valor</strong> NULL.</p><p>JET_bitColumnNotNULL se puede combinar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>La columna es una columna de versión que especifica la versión de la fila. El valor de esta columna comienza en cero y se incrementa automáticamente para cada actualización de la fila.</p><p>JET_bitColumnVersion se puede usar solo cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong> y no se puede combinar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La columna se incrementa automáticamente. El número es un número creciente y se garantiza que es único dentro de una tabla. Sin embargo, es posible que los números no sean secuenciales. Por ejemplo, si se insertan cinco filas en una tabla, la columna incrementada automáticamente podría contener los valores { 1, 2, 6, 7, 8 }.</p><p>JET_bitColumnAutoincrement se puede usar solo cuando el miembro <strong>coltyp</strong> está establecido en <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong> y no se puede combinar con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o JET_bitColumnVersion.</p><p><strong>Windows 2000:</strong> JET_bitColumnVersion se puede usar solo cuando el <strong>miembro coltyp</strong> está establecido <strong>en JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Solo es válido para las llamadas <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a> JET_bitColumnUpdatable se puede combinar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Solo es válido en las llamadas <a href="gg294118(v=exchg.10).md">a JetOpenTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Solo es válido en las llamadas <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican mediante un número en el miembro <strong>itagSequence</strong> de varias estructuras, por ejemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben etiquetarse como columnas; Es decir, es posible que no sean columnas de longitud fija o de longitud variable.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Especifica que una columna es una columna de actualización de custodia que diferentes sesiones con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> pueden actualizar simultáneamente y tendrán coherencia transaccional.</p><ul><li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li></ul><ul><li><p>Para una columna de actualización de custodia, el <strong>miembro coltyp</strong> debe establecerse <strong>en JET_coltypLong.</strong></p></li></ul><ul><li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es <strong>decir, cbDefault</strong> debe ser positivo).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate se pueden combinar con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La columna se crea sin un número de versión. Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. JET_bitColumnUnversioned solo se usa con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. No se puede usar dentro de una transacción.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p><p>JET_bitColumnMaybeNull se puede combinar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>No debe usarse. Use JET_bitColumnDeleteOnZero en su lugar.</p><p>La columna se puede finalizar. Una columna que se puede finalizar es una columna de actualización de custodia que hace que la fila se elimine cuando la columna alcance cero. En su lugar, las versiones futuras pueden invocar una función de devolución de <a href="gg294098(v=exchg.10).md">llamada (vea JET_CALLBACK</a>). Una columna que se puede finalizar debe ser una columna de actualización de custodia. JET_bitColumnFinalize se puede combinar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>El valor predeterminado de una columna lo proporciona una función de devolución de llamada. Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que tenga un valor predeterminado definido por el usuario debe ser una columna etiquetada. Si JET_bitColumnUserDefinedDefault especifica , <strong>pvDefault</strong> debe apuntar a una estructura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof( JET_USERDEFINEDDEFAULT ).</p><p>JET_bitColumnUserDefinedDefault se puede combinar con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La columna es una columna de actualización de custodia y, cuando alcance cero, se eliminará el registro. Un uso común para las columnas delete-on-zero es como campos de recuento de referencias. Cuando el número de referencias cae a cero, se elimina el registro. Una columna delete-on-zero debe ser una columna de actualización de custodia.</p><p>JET_bitColumnDeleteOnZero reemplaza JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero se puede combinar con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault y no se puede usar con columnas predeterminadas definidas por el usuario.</p> | 



**szBaseTableName**

Tabla de la que la tabla actual hereda su DDL.

**szBaseColumnName**

Nombre de la columna de la tabla de plantillas.

### <a name="remarks"></a>Observaciones

**JET_COLUMNBASE** contiene gran parte de la misma información que [JET_COLUMNDEF](./jet-columndef-structure.md), pero agrega campos de cadena para describir la tabla base (si se usó un DDL jerárquico).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_COLUMNBASE_W</strong> (Unicode) <strong>y JET_COLUMNBASE_A</strong> (ANSI).</p> | 



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
