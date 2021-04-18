---
description: 'Más información acerca de: estructura de JET_INDEXLIST'
title: Estructura de JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360998"
---
# <a name="jet_indexlist-structure"></a>Estructura de JET_INDEXLIST


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_indexlist-structure"></a>Estructura de JET_INDEXLIST

La estructura de **JET_INDEXLIST** contiene la información necesaria para atravesar una tabla temporal creada por las funciones [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) . Cada fila de la tabla temporal describe una columna de un índice.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura en bytes. La llamada a la API actualizará este campo, por lo que el llamador debe asegurarse de que este valor coincide con sizeof (JET_INDEXLIST).

**TABLEID**

Identificador de tabla de la tabla temporal que se creó. Es responsabilidad del llamador cerrar la tabla.

**cRecord**

El número de registros de la tabla temporal que se creó.

**columnidindexname**

Identificador de columna del nombre del índice.

Esta columna es un [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Identificador de columna del *grbits* que se usa en el índice. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener una lista de bits válidos.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

Identificador de columna del número de claves del índice.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

Identificador de columna del número de entradas del índice.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificador de columna del número de páginas que usa el índice. Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

El identificador de columna del número total de columnas que abarca el índice.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Identificador de columna del número de columnas del índice. Para obtener más información, consulte la sección Comentarios de este tema.

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

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
<td><p>cIndexInfoCols<br />
15</p></td>
<td><p>Especifica que se permiten 15 columnas.</p></td>
</tr>
<tr class="even">
<td><p>cColumnInfoCols<br />
14</p></td>
<td><p>Especifica que se permiten 14 columnas.</p></td>
</tr>
<tr class="odd">
<td><p>cObjectInfoCols<br />
9</p></td>
<td><p>Especifica que se permiten 9 columnas.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnid**

El identificador de columna de la columna que está indizada. Para obtener más información, consulte la sección Comentarios de este tema. Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificador de columna del coltyp de la columna que está indizada. Para obtener más información, consulte la sección Comentarios de este tema. Esta columna es un [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificador de columna del código de país de la columna indizada. El código de país está en desuso.

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificador de columna del identificador de idioma (LCID) en el que se creó el índice. Para obtener más información, vea [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

El identificador de columna de la página de códigos en la que se creó el índice. Para obtener más información, vea [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

El identificador de columna de la secuencia de intercalación en la que se creó el índice. La secuencia de intercalación está en desuso.

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Identificador de columna del *grbits* que se aplica al orden de la columna en el índice.

Los datos de esta columna se pueden ordenar como JET_bitKeyAscending o JET_bitKeyDescending. Esta columna es un [JET_coltypLong](./jet-coltyp.md). Por ejemplo, un índice definido como "-column1 \\ 0 + columna2 \\ 0" tendrá JET_bitKeyDescending para "column1" y JET_bitKeyAscending para "columna2".

Las siguientes opciones son válidas para este miembro.

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
<td><p>JET_bitKeyAscending</p></td>
<td><p>Un segmento de índice en orden ascendente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitKeyDescending</p></td>
<td><p>Un segmento de índice en orden descendente.</p></td>
</tr>
</tbody>
</table>


**columnidcolumnname**

Identificador de columna del nombre de la columna.

Esta columna es un [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

El identificador de columna de las marcas que se usan para crear el índice. Para obtener más información, consulte la sección **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Esta columna es un [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Observaciones

Cada fila de la tabla temporal corresponde a una columna de un índice determinado.

Por ejemplo, el índice "+ A \\ 0 + B \\ 0 + C 0 \\ + D \\ 0 + E \\ 0" tiene más de cinco columnas y ocupará cinco filas en la tabla temporal. Cada una de estas cinco filas tendrá un valor de 5 en la columna identificada por la columna columnid. Pero cada fila tendrá un valor diferente para la columna columnid, que va de 0 a 4.

El número de claves de un índice determinado corresponde al número de valores únicos para los que un llamador puede buscar y obtener una coincidencia exacta. El número de entradas es el número de filas que coincide con un índice. Si un índice tiene una restricción de unicidad, el número de claves es igual al número de entradas. Por ejemplo, si una tabla contiene la siguiente información y se crea un índice sobre la columna denominada "Key", hay tres claves (100, 200 y 500), pero hay cuatro entradas ("this", "is", "a" y "example").

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Clave</p></th>
<th><p>Entrada</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>100</p></td>
<td><p>&quot;this&quot;</p></td>
</tr>
<tr class="even">
<td><p>100</p></td>
<td><p>&quot;is&quot;</p></td>
</tr>
<tr class="odd">
<td><p>200</p></td>
<td><p>&quot;alternativa&quot;</p></td>
</tr>
<tr class="even">
<td><p>500</p></td>
<td><p>&quot;example&quot;</p></td>
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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
