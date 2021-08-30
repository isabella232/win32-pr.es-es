---
description: 'Más información sobre: JET_COLUMNDEF estructura'
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
ms.openlocfilehash: 61977bb003de70d2810d1492508bf3213f086895
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984018"
---
# <a name="jet_columndef-structure"></a>Estructura de JET_COLUMNDEF


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_columndef-structure"></a>Estructura de JET_COLUMNDEF

La **JET_COLUMNDEF** estructura define los datos que se pueden almacenar en una columna.

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

Tamaño de la estructura, en bytes. Debe establecerse en sizeof( JET_COLUMNDEF).

**columnid**

Reservado. **columnid** debe establecerse en 0 (cero).

**coltyp**

Tipo de la columna (por ejemplo, texto, binario o numérico). Para obtener más información, [vea JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. **wCountry** debe establecerse en 0 (cero).

**langid**

Obsoleto. **langid** debe establecerse en 0 (cero).

**cp**

Página de códigos de la columna. Los únicos valores válidos para las columnas de texto son inglés (1252) y Unicode (1200). Un valor de cero significa que se usará el valor predeterminado (inglés, 1252). Si la columna no es una columna de texto, la página de códigos se establece automáticamente en cero.

**wCollate**

Reservado. **wCollate** debe establecerse en 0 (cero).

**cbMax**

Longitud máxima, en bytes, de una columna de longitud variable o longitud de una columna de longitud fija.

**grbit**

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de los valores siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La columna se solucionará. Siempre usará la misma cantidad de espacio en una fila, independientemente de la cantidad de datos que se almacenen en la columna. JET_bitColumnFixed no se puede usar con JET_bitColumnTagged. Este bit no se puede usar con valores long (es decir, <strong>JET_coltypLongText</strong> y <strong>JET_coltypLongBinary</strong>).</p> | 
| <p>JET_bitColumnTagged</p> | <p>La columna se etiquetará. Las columnas etiquetadas no ocupa ningún espacio en la base de datos si no contienen datos. Este bit no se puede usar con JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La columna nunca debe establecerse en un valor NULL.</p> | 
| <p>JET_bitColumnVersion</p> | <p>La columna es una columna de versión que especifica la versión de la fila. El valor de esta columna comienza en cero y se incrementará automáticamente para cada actualización de la fila.</p><p>Este bit solo se puede aplicar a <strong>JET_coltypLong</strong> columnas. Este bit no se puede usar con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La columna se incrementará automáticamente. El número es un número creciente y se garantiza que es único dentro de una tabla. Sin embargo, es posible que los números no sean continuos. Por ejemplo, si se insertan cinco filas en una tabla, la columna "autoincrement" podría contener los valores { 1, 2, 6, 7, 8 }. Este bit solo se puede usar en columnas de tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p><p><strong>Windows 2000:</strong> En Windows 2000, este bit solo se puede usar en columnas de <strong>tipo JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Este bit solo es válido en las llamadas <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo</a>.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Este bit solo es válido en las llamadas <a href="gg294118(v=exchg.10).md">a JetOpenTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Este bit solo es válido en las llamadas <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La columna puede tener varios valores. Una columna con varios valores puede tener cero, uno o más valores asociados. Los distintos valores de una columna con varios valores se identifican mediante un número denominado miembro <strong>itagSequence,</strong> que pertenece a varias estructuras, incluidos: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>y <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Las columnas con varios valores deben ser columnas etiquetadas; es decir, no pueden ser columnas de longitud fija o de longitud variable.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Especifica que una columna es una columna de actualización de custodia. Diferentes sesiones pueden actualizar simultáneamente una columna de actualización de custodia con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> y mantendrá la coherencia transaccional. Una columna de actualización de custodia también debe cumplir las condiciones siguientes:</p><ul><li><p>Solo se puede crear una columna de actualización de custodia cuando la tabla está vacía.</p></li></ul><ul><li><p>Una columna de actualización de custodia debe ser de <strong>tipo JET_coltypLong</strong>.</p></li></ul><ul><li><p>Una columna de actualización de custodia debe tener un valor predeterminado (es <strong>decir, cbDefault</strong> debe ser positivo).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate se puede usar junto con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La columna se creará en sin información de versión. Esto significa que se producirá un error en otras transacciones que intenten agregar una columna con el mismo nombre. Este bit solo es útil con <a href="gg294122(v=exchg.10).md">JetAddColumn.</a> No se puede usar dentro de una transacción.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Use JET_bitColumnDeleteOnZero en lugar de JET_bitColumnFinalize. JET_bitColumnFinalize que se puede finalizar una columna. Cuando una columna que se puede finalizar tiene una columna de actualización de custodia que alcanza cero, se eliminará la fila. En su lugar, las versiones futuras podrían invocar una función de devolución de llamada (para obtener más información, <a href="gg294098(v=exchg.10).md">vea JET_CALLBACK</a>). Una columna que se pueda finalizar debe ser una columna de actualización de custodia. JET_bitColumnFinalize no se puede usar con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>El valor predeterminado de una columna lo proporciona una función de devolución de llamada. Vea <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una columna que tenga un valor predeterminado definido por el usuario debe ser una columna etiquetada. Especificar JET_bitColumnUserDefinedDefault significa que <strong>pvDefault</strong> debe apuntar a una estructura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> y <strong>cbDefault</strong> debe establecerse en sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p><ul><li><p>JET_bitColumnUserDefinedDefault se puede usar junto con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La columna es una columna de actualización de custodia y, cuando llegue a cero, se eliminará el registro. Un uso común de una columna que se puede finalizar es usarla como un campo de recuento de referencias y, cuando el campo alcanza cero, se elimina el registro. JET_bitColumnDeleteOnZero está relacionado con JET_bitColumnFinalize. Una columna Delete-on-zero debe ser una columna de actualización de custodia. JET_bitColumnDeleteOnZero se puede usar con JET_bitColumnFinalize. JET_bitColumnDeleteOnZero no se puede usar con columnas predeterminadas definidas por el usuario.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



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
