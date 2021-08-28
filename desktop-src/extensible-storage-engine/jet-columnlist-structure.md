---
description: 'Más información sobre: JET_COLUMNLIST estructura'
title: Estructura de JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 6b7f874c95352ce29954adf46b1682dec89c7a9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471801"
---
# <a name="jet_columnlist-structure"></a>Estructura de JET_COLUMNLIST


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_columnlist-structure"></a>Estructura de JET_COLUMNLIST

La **JET_COLUMNLIST** estructura contiene la información necesaria para recorrer la tabla temporal creada por las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md) Cada fila de la tabla temporal describe una columna de la tabla especificada en la llamada API. Esta estructura solo se usa con [Con JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura en bytes. La llamada API actualizará este campo, por lo que el autor de la llamada debe asegurarse de que este valor coincide con sizeof( JET_COLUMNLIST ).

**tableid**

Identificador de tabla de la tabla temporal que se creó. Es responsabilidad del autor de la llamada cerrar la tabla.

**cRecord**

Número de registros de la tabla temporal que creó la llamada API.

**columnidPresentationOrder**

Identificador de columna del orden de presentación.

El orden de presentación se usa para ordenar las filas de la tabla temporal. El orden de presentación es [una](./jet-coltyp.md)JET_coltypLong . Si el nivel de información especificado no era un nivel compacto, también se marca como JET_bitColumnTTKey.

**columnidcolumnname**

Identificador de columna del nombre de la columna.

Si el nivel de información especificado no era compacto, también se marca como JET_bitColumnTTKey.

**columnidcolumnid**

Identificador de columna del identificador de columna.

El identificador de columna es un valor [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificador de columna del tipo de columna.

El tipo de columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificador de columna del código de país.

El código de país es [una](./jet-coltyp.md)JET_coltypShort .

**columnidLangid**

Identificador de columna del identificador de idioma.

El identificador de idioma es un valor [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificador de columna de la página de códigos.

La página de códigos es un valor [fijo JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificador de columna de la secuencia de intercalación.

La secuencia de intercalación es [una](./jet-coltyp.md)JET_coltypShort .

**columnidcbMax**

Identificador de columna del **campo cbMax.**

CbMax **es** un valor [fijo JET_coltypLong](./jet-coltyp.md).

**columnidgrbit**

Identificador de columna de *los bits grbits* de la columna. El *campo grbit* es una [JET_coltypLong](./jet-coltyp.md). Para obtener más información sobre estos bits, [vea JET_COLUMNDEF](./jet-columndef-structure.md).

Estos son los valores posibles **para columnidgrbit**:

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

Identificador de columna del valor predeterminado de la columna.

El valor predeterminado es un [JET_coltypLongBinary](./jet-coltyp.md).

**columnidBaseTableName**

Identificador de columna del nombre de la tabla de la que se deriva la tabla.

El nombre de la tabla es [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

Identificador de columna del nombre de la columna de la que se deriva la columna.

El nombre de columna es [un JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Identificador de columna del nombre de la definición de columna.

El nombre de definición de columna [es JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Comentarios

De forma predeterminada, el orden de las filas de la tabla temporal se ordena por el nombre de la columna. También se puede ordenar por identificador de columna. Para obtener más información sobre cómo ordenar por identificador de columna, vea [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)

La llamada a [JetGetColumnInfo o](./jetgetcolumninfo-function.md) [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) podría especificar una forma compacta de resultados. Si alguna columna se ha heredado de una tabla de plantillas, los resultados compactos no las almacenarán.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
