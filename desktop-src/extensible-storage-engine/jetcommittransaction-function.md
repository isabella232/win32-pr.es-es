---
description: 'Más información sobre: JetCommitTransaction (Función)'
title: Función JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9592c9b596a7794cc130b7ed599b7c8562ff8b2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477631"
---
# <a name="jetcommittransaction-function"></a>Función JetCommitTransaction


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcommittransaction-function"></a>Función JetCommitTransaction

La **función JetCommitTransaction** confirma los cambios realizados en el estado de la base de datos durante el punto de guardado actual y los migra al punto de guardado anterior. Si se confirma el punto de guardado más externo, los cambios realizados durante ese punto de guardado se confirman en el estado de la base de datos y la sesión cerrará la transacción.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada. Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad. Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación de bloqueos durante la siguiente llamada a <a href="gg294068(v=exchg.10).md">JetInit</a>.</p><p>Si JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, se omite esta opción.</p><p>Si esta llamada a <strong>JetCommitTransaction</strong> no coincide con la primera llamada a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para esta sesión, se omite esta opción. Esto se debe a que la acción final que se produce en el punto de guardado más externo es el factor determinante para determinar si toda la transacción se confirma realmente en el disco.</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>Todas las transacciones confirmadas previamente por cualquier sesión que aún no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</p><p>Esta opción se puede usar incluso si la sesión no está actualmente en una transacción.</p><p>Esta opción no se puede usar en combinación con ninguna otra opción.</p><p>Esta opción solo está disponible a partir de Windows Server 2003.</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>Si la sesión ha confirmado previamente las transacciones y aún no se han vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora quiere vaciarlas todas en el disco.</p><p>Esta opción se puede usar incluso si la sesión no está actualmente en una transacción.</p><p>Esta opción no se puede usar en combinación con ninguna otra opción.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida o no se implementó. <strong>JetCommitTransaction</strong> devolverá este error cuando:</p><ul><li><p>Se especifica <em>un grbit</em> no es posible.</p></li><li><p>JET_bitWaitLastLevel0Commit se especificó en combinación con otro <em>bit grbit</em>.</p></li><li><p>JET_bitWaitAllLevel0Commit se especificó en combinación con otro <em>bit grbit</em>.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Error en la operación porque la sesión dada no está en una transacción.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se realiza correctamente, se confirman los cambios realizados en la base de datos durante el punto de guardado actual de la sesión determinada y ese punto de guardado finalizará. Si se finalizó el último punto de guardado de la sesión, la transacción se vaciará opcionalmente en el archivo de registro de transacciones y la sesión cerrará la transacción.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos. La aplicación debe llamar a [JetRollback para](./jetrollback-function.md) anular la transacción.

#### <a name="remarks"></a>Comentarios

Debe haber una llamada a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
