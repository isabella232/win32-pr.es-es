---
description: 'Más información sobre: JET_DBINFOUPGRADE estructura'
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
ms.openlocfilehash: 57c9265f45412bd31e087a52ab2b923c9c55c430
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467662"
---
# <a name="jet_dbinfoupgrade-structure"></a>Estructura de JET_DBINFOUPGRADE


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_dbinfoupgrade-structure"></a>Estructura de JET_DBINFOUPGRADE

La **JET_DBINFOUPGRADE** contiene información sobre el estado de actualización de la base de datos. Este valor solo se recupera si **JET_DBINFOUPGRADE** a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md) Esta estructura no es necesaria para las versiones actuales del sistema operativo del motor de base de datos.

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

Se establece en el tamaño de la **estructura JET_DBINFOUPGRADE,** en bytes.

**cbFilesizeLow**

DWORD **bajo que** refleja el tamaño de archivo actual de la base de datos.

**cbFilesizeHigh**

DWORD **alto que** refleja el tamaño de archivo actual de la base de datos.

**cbFreeSpaceRequiredLow**

DWORD **bajo del** espacio en disco libre estimado necesario para una actualización local.

**cbFreeSpaceRequiredHigh**

DWORD **elevado del** espacio en disco libre estimado necesario para una actualización local.

**csecToUpgrade**

Tiempo estimado necesario para actualizar, en segundos.

**ulFlags**

Campo de bits de cero o más de las marcas siguientes: **fUpgradable**, **fAlreadyUpgraded**.

**fUpgradable**

La base de datos se puede actualizar.

**fAlreadyUpgraded**

La base de datos se actualiza al formato de base de datos actual.

### <a name="remarks"></a>Comentarios

Una **JET_DBINFOUPGRADE** estructura se rellena mediante una llamada a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo.](./jetgetdatabasefileinfo-function.md) Si la función no se realiza correctamente, el contenido de la estructura no está definido.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
