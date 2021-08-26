---
description: 'Más información sobre: JetBeginTransaction2 (Función)'
title: Función JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c228f7ac0c1b796cc3c6c489e9e83766ada5d716
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466363"
---
# <a name="jetbegintransaction2-function"></a>Función JetBeginTransaction2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbegintransaction2-function"></a>Función JetBeginTransaction2

La **función JetBeginTransaction2** hace que una sesión escriba una transacción y cree un nuevo punto de guardado. Se puede llamar a esta función más de una vez en una sola sesión para crear puntos de guardado adicionales. Estos puntos de guardado se pueden usar de forma selectiva para mantener o descartar cambios en la base de datos.

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>La transacción no modificará la base de datos. Si se intenta realizar una actualización, se producirá un error en esa operación JET_errTransReadOnly. Esta opción se omite a menos que se solicite cuando la sesión determinada no está ya en una transacción. Esta opción solo está disponible a Windows XP.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransTooDeep</p> | <p>No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima de punto de guardado que permite el motor de base de datos.</p> | 



Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción. Si la sesión estaba anteriormente dentro de una transacción, se creará un nuevo punto de guardado.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo funcionan las transacciones, [vea JetBeginTransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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
