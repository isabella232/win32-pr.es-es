---
description: 'Más información sobre: JET_SESID'
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
ms.openlocfilehash: da7acc706017c0346e5a701144d60bcbbfd7cf40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882817"
---
# <a name="jet_sesid"></a>JET_SESID


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_sesid"></a>JET_SESID

El **JET_SESID** tipo de datos contiene un identificador para la sesión que se usará para una llamada a la API jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipo de datos

JET_SESID

Null **o** [JET_sesidNil](./invalid-handle-constants.md) pueden usarse para indicar un identificador de sesión no válido.

### <a name="remarks"></a>Observaciones

Una sesión es el contexto de transacción del motor de base de datos. Se puede usar para iniciar, confirmar o anular transacciones que afectan a la visibilidad y durabilidad de los cambios realizados por esta u otras sesiones.

Se puede iniciar una transacción [mediante JetBeginTransaction](./jetbegintransaction-function.md). Se puede crear una sesión mediante [JetBeginSession.](./jetbeginsession-function.md) El número máximo de sesiones que se pueden crear en cualquier momento se controla mediante JET_paramMaxSessions [,](./resource-parameters.md)que se puede configurar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Una sesión finaliza explícitamente mediante una llamada a [JetEndSession](./jetendsession-function.md) o finaliza implícitamente mediante una llamada a [JetTerm](./jetterm-function.md).

Cada sesión solo puede ser utilizada por un subproceso a la vez. Además, el comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a [JetBeginTransaction](./jetbegintransaction-function.md) hasta el momento en que se realiza la llamada correspondiente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Este comportamiento se puede cambiar para quitar esta segunda restricción estableciendo un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



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
