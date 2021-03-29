---
description: 'Más información acerca de: estructura de JET_INSTANCE_INFO'
title: Estructura de JET_INSTANCE_INFO
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
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912998"
---
# <a name="jet_instance_info-structure"></a>Estructura de JET_INSTANCE_INFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>Estructura de JET_INSTANCE_INFO

La estructura **JET_INSTANCE_INFO** recibe información sobre la ejecución de instancias de base de datos cuando se usa con las funciones [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) y [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .

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

[JET_INSTANCE](./jet-instance.md) de la instancia de especificada.

**szInstanceName**

Nombre de la instancia de la base de datos. Este valor puede ser **null** si la instancia de no tiene un nombre.

**cDatabases**

El número de bases de datos que se adjuntan a la instancia de base de datos. **cDatabases** también contiene el tamaño de las matrices de cadenas que se devuelven en **szDatabaseFileName**, **szDatabaseDisplayName** y **szDatabaseSLVFileName**.

**szDatabaseFileName**

Matriz de cadenas, cada una de las cuales contiene el nombre de archivo de una base de datos que se adjunta a la instancia de base de datos. La matriz tiene elementos **cDatabases** .

**szDatabaseDisplayName**

Matriz de cadenas, cada una de las cuales contiene el nombre para mostrar de una base de datos. Actualmente, la cadena puede ser NULL. La matriz tiene elementos **cDatabases** .

**szDatabaseSLVFileName**

Matriz de cadenas, cada una de las cuales contiene el nombre del archivo SLV que está asociado a la instancia de base de datos. La matriz tiene elementos **cDatabases** . No se admiten archivos SLV, por lo que este campo debe omitirse.

### <a name="remarks"></a>Observaciones

Cada instancia de base de datos puede tener varias bases de datos asociadas.

Para una estructura de **JET_INSTANCE_INFO** determinada, la matriz de cadenas que se devuelve para las bases de datos está en el mismo orden. Por ejemplo, "szDatabaseDisplayName \[ i \] " y "szDatabaseFileName \[ i \] " hacen referencia a la misma base de datos.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_INSTANCE_INFO_W</strong> (Unicode) y <strong>JET_INSTANCE_INFO _a</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
