---
description: 'Más información sobre: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: 04e59ddada8715872978ccc21da11a349e1b7c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983578"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_tableid"></a>JET_TABLEID

El JET_TABLEID tipo de datos contiene un identificador para el cursor de base de datos que se usará para una llamada a la API jet. Un cursor solo se puede usar con la sesión que se usó para abrir ese cursor.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Tipo de datos

JET_TABLEID

Null **o** [JET_tableidNil](./invalid-handle-constants.md) pueden usarse para indicar un identificador de cursor no válido.

### <a name="remarks"></a>Observaciones

Un cursor administra el uso de una tabla para el motor de base de datos. Un cursor puede realizar las siguientes tareas:

  - Examen de registros

  - Buscar registros

  - Elegir el criterio de ordenación y la visibilidad efectivos de esos registros

  - Creación, actualización o eliminación de registros

  - Modificación del esquema de la tabla

La funcionalidad admitida del cursor puede cambiar a medida que cambia el estado o el tipo de la tabla subyacente. Por ejemplo, una tabla temporal podría no permitir la búsqueda de datos cuando se abre con determinadas opciones. El cursor siempre está totalmente conectado a la tabla subyacente e interactúa directamente con los datos sin ningún almacenamiento en caché. Casi toda la funcionalidad básica de ISAM que expone este motor de base de datos funciona a través del cursor.

Se puede crear un cursor [mediante JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable.](./jetopentemptable-function.md) Un cursor se puede duplicar mediante [JetDupCursor.](./jetdupcursor-function.md) Un cursor se puede cerrar explícitamente mediante [JetCloseTable](./jetclosetable-function.md) o cerrarse implícitamente mediante [JetEndSession](./jetendsession-function.md) o [JetTerm.](./jetterm-function.md) [JetRollback](./jetrollback-function.md) también puede cerrar implícitamente un cursor si se abrió en la transacción anulada. El número máximo de cursores que se pueden crear en cualquier momento se controla mediante JET_paramMaxCursors [,](./resource-parameters.md)que se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
