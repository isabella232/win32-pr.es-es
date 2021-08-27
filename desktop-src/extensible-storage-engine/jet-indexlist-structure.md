---
description: 'Más información sobre: JET_INDEXLIST estructura'
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480051"
---
# <a name="jet_indexlist-structure"></a>Estructura de JET_INDEXLIST


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_indexlist-structure"></a>Estructura de JET_INDEXLIST

La **JET_INDEXLIST** estructura contiene la información necesaria para recorrer una tabla temporal creada por las funciones [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md) Cada fila de la tabla temporal describe una columna de un índice.

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

Tamaño de la estructura en bytes. La llamada API actualizará este campo, por lo que el autor de la llamada debe asegurarse de que este valor coincide con sizeof( JET_INDEXLIST ).

**tableid**

Identificador de tabla de la tabla temporal que se creó. Es responsabilidad del autor de la llamada cerrar la tabla.

**cRecord**

Número de registros de la tabla temporal que se creó.

**columnidindexname**

Identificador de columna del nombre del índice.

Esta columna es una [JET_coltypText](./jet-coltyp.md).

**columnidgrbitIndex**

Identificador de columna de *los grbits usados* en el índice. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener una lista de bits válidos.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcKey**

Identificador de columna del número de claves del índice.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcEntry**

Identificador de columna del número de entradas del índice.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcPage**

Identificador de columna del número de páginas que usa el índice. Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcColumn**

Identificador de columna del número total de columnas que abarca el índice.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidiColumn**

Identificador de columna del número de columnas del índice. Para obtener más información, vea la sección Comentarios de este tema.

Esta columna es una [JET_coltypLong](./jet-coltyp.md).


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>Especifica que se permiten 15 columnas.</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>Especifica que se permiten 14 columnas.</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>Especifica que se permiten 9 columnas.</p> | 



**columnidcolumnid**

Identificador de columna de la columna indizada. Para obtener más información, vea la sección Comentarios de este tema. Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidcoltyp**

Identificador de columna del coltyp de la columna que se indexa. Para obtener más información, vea la sección Comentarios de este tema. Esta columna es una [JET_coltypLong](./jet-coltyp.md).

**columnidCountry**

Identificador de columna del código de país de la columna indizada. El código de país está en desuso.

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidLangid**

Identificador de columna del identificador de idioma (LCID) con el que se creó el índice. Para obtener más información, [vea JET_INDEXCREATE](./jet-indexcreate-structure.md).

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidCp**

Identificador de columna de la página de códigos en la que se creó el índice. Para obtener más información, [vea JET_COLUMNCREATE](./jet-columncreate-structure.md).

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidCollate**

Identificador de columna de la secuencia de intercalación en la que se creó el índice. La secuencia de intercalación está en desuso.

Esta columna es un [JET_coltypShort](./jet-coltyp.md).

**columnidgrbitColumn**

Identificador de columna de *los bits grbits* que se aplican al orden de la columna en el índice.

Los datos de esta columna se pueden ordenar como JET_bitKeyAscending o JET_bitKeyDescending. Esta columna es una [JET_coltypLong](./jet-coltyp.md). Por ejemplo, un índice definido como "-column1 \\ 0+column2 0" tendrá JET_bitKeyDescending para \\ "column1" y JET_bitKeyAscending para "column2".

Las siguientes opciones son válidas para este miembro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Segmento de índice en orden ascendente.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Segmento de índice en orden descendente.</p> | 



**columnidcolumnname**

Identificador de columna del nombre de la columna.

Esta columna es una [JET_coltypText](./jet-coltyp.md).

**columnidLCMapFlags**

Identificador de columna de las marcas que se usan para crear el índice. Para obtener más información, vea **la sección dwMapFlags** [de JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Esta columna es una [JET_coltypLong](./jet-coltyp.md).

### <a name="remarks"></a>Comentarios

Cada fila de la tabla temporal corresponde a una columna de un índice determinado.

Por ejemplo, el índice "+A \\ 0+B \\ 0+C \\ 0+D \\ 0+E 0" es superior a cinco columnas y ocupará cinco filas en la \\ tabla temporal. Cada una de estas cinco filas tendrá un valor de 5 en la columna identificada por la columna columnid. Pero cada fila tendrá un valor diferente para la columna columnid, que va de 0 a 4.

El número de claves de un índice determinado corresponde al número de valores únicos para los que un autor de la llamada puede buscar y obtener una coincidencia exacta. El número de entradas es el número de filas con las que coincide un índice. Si un índice tiene una restricción de unidad, el número de claves es igual al número de entradas. Por ejemplo, si una tabla contiene la siguiente información y se crea un índice sobre la columna denominada "key", hay tres claves (100, 200 y 500), pero hay cuatro entradas ("this", "is", "an" y "example").


| <p>Clave</p> | <p>Entrada</p> | 
|------------|--------------|
| <p>100</p> | <p>"this"</p> | 
| <p>100</p> | <p>"is"</p> | 
| <p>200</p> | <p>"an"</p> | 
| <p>500</p> | <p>"ejemplo"</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



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
