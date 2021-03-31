---
description: 'Más información acerca de: estructura de JET_RECORDLIST'
title: Estructura de JET_RECORDLIST
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912990"
---
# <a name="jet_recordlist-structure"></a>Estructura de JET_RECORDLIST


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_recordlist-structure"></a>Estructura de JET_RECORDLIST

La estructura **JET_RECORDLIST** encuentra los registros que se encuentran en la intersección de los intervalos de índice especificados cuando se usan con la función [JetIntersectIndexes](./jetintersectindexes-function.md) .

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

Tamaño de la estructura de **JET_RECORDLIST** , en bytes.

**TABLEID**

Identificador de tabla de una tabla temporal que contiene los marcadores de los resultados de la consulta. La tabla se cerrará automáticamente si la transacción actual se revierte con [JetRollback](./jetrollback-function.md); de lo contrario, debe cerrarse con [JetCloseTable](./jetclosetable-function.md).

**cRecord**

Número de filas de la tabla temporal.

**columnidBookmark**

El identificador de columna de la columna de marcador en la tabla temporal.

### <a name="remarks"></a>Observaciones

La tabla temporal identificada por **TABLEID** tiene una sola columna. Esa columna única contiene marcadores y cada registro debe caber en un búfer de tamaño JET_cbBookmarkMost bytes.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
