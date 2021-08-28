---
description: 'Más información sobre: JetBeginTransaction3 (Función)'
title: Función JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca07ad3957efadfb86ac5df9b1994d5c4525c7a2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989048"
---
# <a name="jetbegintransaction3-function"></a>Función JetBeginTransaction3


_**Se aplica a:** Windows | Windows Servidor_

La **función JetBeginTransaction3** hace que una sesión escriba una transacción y cree un nuevo punto de guardado. Se puede llamar a esta función más de una vez en una sola sesión para crear puntos de guardado adicionales. Estos puntos de guardado se pueden usar de forma selectiva para mantener o descartar cambios en la base de datos.

La **función JetBeginTransaction3** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*trxid*

Identificador opcional proporcionado por el usuario para identificar la transacción.

*grbit*

Grupo de bits que especifica cero o más de los valores de opción de llamada enumerados en la tabla siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>La transacción no modificará la base de datos. Si se intenta realizar una actualización, se producirá un error en esa operación JET_errTransReadOnly código de respuesta. Esta opción se omite a menos que se solicite cuando la sesión determinada no está ya en una transacción. Esta opción está disponible en las versiones del Windows operativo a partir de Windows XP.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a la <a href="gg269240(v=exchg.10).md">función JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este código devuelto lo devuelven las versiones de Windows a partir de Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error lo devuelven las versiones de Windows a partir de Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransTooDeep</p> | <p>No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima de punto de guardado que permite el motor de base de datos.</p> | 



Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción. Si la sesión estaba anteriormente dentro de una transacción, se creará un nuevo punto de guardado.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Para obtener más información sobre cómo funcionan las transacciones, [vea JetBeginTransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
