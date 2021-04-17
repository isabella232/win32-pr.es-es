---
description: 'Más información acerca de: estructura de JET_DBINFOUPGRADE'
title: Estructura de JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686763"
---
# <a name="jet_dbinfoupgrade-structure"></a>Estructura de JET_DBINFOUPGRADE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>Estructura de JET_DBINFOUPGRADE

La estructura **JET_DBINFOUPGRADE** contiene información sobre el estado de actualización de la base de datos. Este valor se recupera solo si **JET_DBINFOUPGRADE** se pasó a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Esta estructura no es necesaria para las versiones actuales del sistema operativo del motor de base de datos.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Miembros

**cbStruct**

Se establece en el tamaño de la estructura **JET_DBINFOUPGRADE** , en bytes.

**cbFilesizeLow**

**Valor DWORD** inferior que refleja el tamaño actual del archivo de la base de datos.

**cbFilesizeHigh**

**Valor DWORD** alto que refleja el tamaño actual del archivo de la base de datos.

**cbFreeSpaceRequiredLow**

**Valor DWORD** inferior del espacio libre en disco estimado necesario para una actualización en contexto.

**cbFreeSpaceRequiredHigh**

**Valor DWORD** alto del espacio libre en disco estimado necesario para una actualización en contexto.

**csecToUpgrade**

El tiempo estimado necesario para la actualización, en segundos.

**ulFlags**

Un campo de bits formado por cero o más de las marcas siguientes: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

La base de datos es actualizable.

**fAlreadyUpgraded**

La base de datos se actualiza al formato de base de datos actual.

### <a name="remarks"></a>Observaciones

Una **JET_DBINFOUPGRADE** estructura se rellena mediante una llamada a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md). Si la función no se ejecuta correctamente, el contenido de la estructura es indefinido.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
