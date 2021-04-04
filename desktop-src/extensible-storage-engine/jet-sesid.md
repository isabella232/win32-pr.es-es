---
description: 'Más información acerca de: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
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
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907770"
---
# <a name="jet_sesid"></a>JET_SESID


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_sesid"></a>JET_SESID

El tipo de datos **JET_SESID** contiene un identificador de la sesión que se va a usar para una llamada a la API de jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipo de datos

JET_SESID

Se puede utilizar **null** o [JET_sesidNil](./invalid-handle-constants.md) para indicar un identificador de sesión no válido.

### <a name="remarks"></a>Observaciones

Una sesión es el contexto de transacción del motor de base de datos. Se puede usar para iniciar, confirmar o anular transacciones que afectan a la visibilidad y la durabilidad de los cambios realizados por esta u otras sesiones.

Una transacción se puede iniciar mediante [JetBeginTransaction](./jetbegintransaction-function.md). Se puede crear una sesión mediante [JetBeginSession](./jetbeginsession-function.md). El número máximo de sesiones que se pueden crear en un momento determinado se controla mediante [JET_paramMaxSessions](./resource-parameters.md), que se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una sesión finaliza explícitamente mediante una llamada a [JetEndSession](./jetendsession-function.md) o termina implícitamente mediante una llamada a [JetTerm](./jetterm-function.md).

Cada sesión solo puede ser utilizada por un subproceso a la vez. Además, el comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a [JetBeginTransaction](./jetbegintransaction-function.md) hasta el momento en que se realiza la llamada coincidente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) . Este comportamiento se puede cambiar para quitar esta segunda restricción mediante la configuración de un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
