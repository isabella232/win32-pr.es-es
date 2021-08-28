---
description: 'Más información sobre: JET_RECORDLIST estructura'
title: JET_RECORDLIST estructura
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 983a0d6a73d4a3bb5e44095f46cc52d537ce15f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465102"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_recordlist-structure"></a>JET_RECORDLIST estructura

La **JET_RECORDLIST** busca registros que se encuentran en la intersección de los intervalos de índice especificados cuando se usan con la función [JetIntersectIndexes.](./jetintersectindexes-function.md)

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura **JET_RECORDLIST,** en bytes.

**tableid**

Identificador de tabla de una tabla temporal que contiene los marcadores de los resultados de la consulta. La tabla se cerrará automáticamente si la transacción actual se revierte con [JetRollback](./jetrollback-function.md); De lo contrario, se debe cerrar [con JetCloseTable.](./jetclosetable-function.md)

**cRecord**

Número de filas de la tabla temporal.

**columnidBookmark**

Identificador de columna de la columna de marcador de la tabla temporal.

### <a name="remarks"></a>Comentarios

La tabla temporal identificada por **tableid** tiene una sola columna. Esa sola columna contiene marcadores y cada registro debe caber en un búfer de tamaño JET_cbBookmarkMost bytes.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
