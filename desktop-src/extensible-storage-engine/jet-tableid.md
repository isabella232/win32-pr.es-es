---
description: 'Más información acerca de: JET_TABLEID'
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697448"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_tableid"></a>JET_TABLEID

El tipo de datos JET_TABLEID contiene un identificador para el cursor de base de datos que se va a usar para una llamada a la API de JET. Un cursor solo se puede usar con la sesión que se usó para abrir ese cursor.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Tipo de datos

JET_TABLEID

Se puede utilizar **null** o [JET_tableidNil](./invalid-handle-constants.md) para indicar un identificador de cursor no válido.

### <a name="remarks"></a>Observaciones

Un cursor administra el uso de una tabla para el motor de base de datos. Un cursor puede realizar las tareas siguientes:

  - Examinar registros

  - Buscar registros

  - Elegir el criterio de ordenación y la visibilidad efectivos de esos registros

  - Crear, actualizar o eliminar registros

  - Modificar el esquema de la tabla

La funcionalidad admitida del cursor puede cambiar a medida que cambia el estado o el tipo de la tabla subyacente. Por ejemplo, una tabla temporal podría no permitir la búsqueda de datos cuando se abre con determinadas opciones. El cursor siempre está totalmente conectado a la tabla subyacente e interactúa directamente con esos datos sin almacenamiento en caché. Casi toda la funcionalidad de ISAM básica que expone este motor de base de datos funciona a través del cursor.

Se puede crear un cursor mediante [JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable](./jetopentemptable-function.md). Un cursor se puede duplicar mediante [JetDupCursor](./jetdupcursor-function.md). Un cursor se puede cerrar explícitamente mediante [JetCloseTable](./jetclosetable-function.md) o cerrarse implícitamente mediante [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md). [JetRollback](./jetrollback-function.md) también puede cerrar implícitamente un cursor si estaba abierto en la transacción que se ha anulado. El número máximo de cursores que se pueden crear en cualquier momento se controla mediante [JET_paramMaxCursors](./resource-parameters.md), que puede configurarse mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

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

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
