---
description: 'Más información acerca de: estructura de JET_COLUMNLIST'
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715406"
---
# <a name="jet_columnlist-structure"></a>Estructura de JET_COLUMNLIST


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_columnlist-structure"></a>Estructura de JET_COLUMNLIST

La estructura de **JET_COLUMNLIST** contiene la información necesaria para recorrer la tabla temporal creada por las funciones [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) . Cada fila de la tabla temporal describe una columna de la tabla especificada en la llamada de API. Esta estructura se usa solo con [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

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

Tamaño de la estructura en bytes. La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_COLUMNLIST).

**TABLEID**

Identificador de tabla de la tabla temporal que se creó. Es responsabilidad del llamador cerrar la tabla.

**cRecord**

El número de registros de la tabla temporal que creó la llamada API.

**columnidPresentationOrder**

Identificador de columna del orden de presentación.

El orden de presentación se usa para ordenar las filas de la tabla temporal. El orden de presentación es un [JET_coltypLong](./jet-coltyp.md)fijo. Si el nivel de información que se especificó no era un nivel compacto, también se marca como JET_bitColumnTTKey.

**columnidcolumnname**

Identificador de columna del nombre de la columna.

Si el nivel de información especificado no es compacto, también se marca como JET_bitColumnTTKey.

**columnidcolumnid**

Identificador de columna del identificador de columna.

El identificador de columna es un [JET_coltypLong](./jet-coltyp.md)fijo.

**columnidcoltyp**

Identificador de columna del tipo de columna.

El tipo de columna es un [JET_coltypLong](./jet-coltyp.md)fijo.

**columnidCountry**

Identificador de columna del código de país.

El código de país es un [JET_coltypShort](./jet-coltyp.md)fijo.

**columnidLangid**

Identificador de columna del identificador de idioma.

El identificador de idioma es un [JET_coltypShort](./jet-coltyp.md)fijo.

**columnidCp**

El identificador de columna de la página de códigos.

La página de códigos es un [JET_coltypShort](./jet-coltyp.md)fijo.

**columnidCollate**

El identificador de columna de la secuencia de intercalación.

La secuencia de intercalación es un [JET_coltypShort](./jet-coltyp.md)fijo.

**columnidcbMax**

Identificador de columna del campo **cbMax** .

**CbMax** es un [JET_coltypLong](./jet-coltyp.md)fijo.

**columnidgrbit**

Identificador de columna del *grbits* de la columna. El campo *grbit* es un [JET_coltypLong](./jet-coltyp.md)fijo. Para obtener más información sobre estos bits, vea [JET_COLUMNDEF](./jet-columndef-structure.md).

A continuación se muestran los posibles valores para **columnidgrbit**:

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

El identificador de columna del nombre de la tabla de la que se derivó la tabla.

El nombre de la tabla es un [JET_coltypText](./jet-coltyp.md).

**columnidBaseColumnName**

Identificador de columna del nombre de la columna de la que se derivó la columna.

El nombre de la columna es un [JET_coltypText](./jet-coltyp.md).

**columnidDefinitionName**

Identificador de columna del nombre de la definición de columna.

El nombre de la definición de columna es un [JET_coltypText](./jet-coltyp.md).

### <a name="remarks"></a>Observaciones

De forma predeterminada, el orden de las filas de la tabla temporal se ordena por el nombre de la columna. También se puede ordenar por identificador de columna. Para obtener más información sobre cómo ordenar por identificador de columna, vea [JetGetColumnInfo](./jetgetcolumninfo-function.md) y [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

La llamada a [JetGetColumnInfo](./jetgetcolumninfo-function.md) o [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) puede especificar una forma compacta de los resultados. Si alguna columna se ha heredado de una tabla de plantilla, los resultados de Compact no las almacenarán.

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

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
