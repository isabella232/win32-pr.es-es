---
description: 'Más información sobre: JET_INSTANCE_INFO estructura'
title: JET_INSTANCE_INFO estructura
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0954aa944cfc30c2fc1ce7b078445b44683b9d97
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984128"
---
# <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO estructura

La **JET_INSTANCE_INFO** recibe información sobre la ejecución de instancias de base de datos cuando se usa con las funciones [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) y [JetOSSnapshotFreeze.](./jetossnapshotfreeze-function.md)

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Miembros

**hInstanceId**

El [JET_INSTANCE](./jet-instance.md) de la instancia especificada.

**szInstanceName**

Nombre de la instancia de la base de datos. Este valor puede ser **NULL** si la instancia no tiene un nombre.

**cDatabases**

Número de bases de datos que están asociadas a la instancia de base de datos. **cDatabases también** contiene el tamaño de las matrices de cadenas que se devuelven en **szDatabaseFileName**, **szDatabaseDisplayName** y **szDatabaseSLVFileName**.

**szDatabaseFileName**

Matriz de cadenas, cada una de las que contiene el nombre de archivo de una base de datos asociada a la instancia de base de datos. La matriz tiene **elementos cDatabases.**

**szDatabaseDisplayName**

Matriz de cadenas, cada una con el nombre para mostrar de una base de datos. Actualmente, la cadena puede ser NULL. La matriz tiene **elementos cDatabases.**

**szDatabaseSLVFileName**

Matriz de cadenas, cada una de las que contiene el nombre de archivo del archivo SLV que está asociado a la instancia de base de datos. La matriz tiene **elementos cDatabases.** No se admiten archivos SLV, por lo que este campo debe omitirse.

### <a name="remarks"></a>Observaciones

Cada instancia de base de datos puede tener varias bases de datos asociadas.

Para una estructura **JET_INSTANCE_INFO,** la matriz de cadenas que se devuelve para las bases de datos está en el mismo orden. Por ejemplo, "szDatabaseDisplayName \[ \] i" y "szDatabaseFileName \[ \] i" hacen referencia a la misma base de datos.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JET_INSTANCE_INFO_W</strong> (Unicode) <strong>y JET_INSTANCE_INFO _A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
