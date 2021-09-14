---
description: 'Más información sobre: JetGetLock (Función)'
title: JetGetLock (Función)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51509f4027d4748f32b8c9dfb8756433b5f93935
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962787"
---
# <a name="jetgetlock-function"></a>JetGetLock (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetlock-function"></a>JetGetLock (Función)

La **función JetGetLock** proporciona un medio para reservar explícitamente la capacidad de actualizar una fila, escribir bloqueo o impedir explícitamente que cualquier otra sesión actualice una fila, el bloqueo de lectura. Normalmente, los bloqueos de escritura de fila se adquieren implícitamente como resultado de la actualización de filas. Normalmente, los bloqueos de lectura no son necesarios debido al control de versiones de los registros. Sin embargo, en algunos casos, es posible que una transacción desee bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación posterior se realizará correctamente en virtud de que ya se han realizado los bloqueos necesarios.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará para esta llamada.

*tableid*

Cursor que se usará para esta llamada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitReadLock</p> | <p>Esta marca hace que se adquiera un bloqueo de lectura en el registro actual. Los bloqueos de lectura no son compatibles con los bloqueos de escritura que ya mantienen otras sesiones, pero son compatibles con los bloqueos de lectura que mantienen otras sesiones.</p> | 
| <p>JET_bitWriteLock</p> | <p>Esta marca hace que se adquiera un bloqueo de escritura en el registro actual. Los bloqueos de escritura no son compatibles con los bloqueos de escritura o lectura que mantienen otras sesiones, pero son compatibles con los bloqueos de lectura mantenidos por la misma sesión.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>El <em>grbit dado</em> no es JET_bitReadLock ni JET_bitWriteLock. Debe ser una de estas dos marcas.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor debe estar en un registro para adquirir un bloqueo. Los bloqueos siempre están en los registros.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Las sesiones de una transacción solo pueden adquirir bloqueos.</p> | 
| <p>JET_errPermissionDenied</p> | <p>El cursor no puede ser de solo lectura y adquirir un bloqueo de escritura.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sesión debe tener permisos de escritura para adquirir el bloqueo de escritura.</p> | 
| <p>JET_errWriteConflict</p> | <p>Error devuelto cuando se solicita un bloqueo en conflicto.</p> | 



Si se ejecuta correctamente, la sesión ha adquirido el bloqueo solicitado.

En caso de error, la sesión no ha adquirido el bloqueo solicitado.

#### <a name="remarks"></a>Observaciones

Los bloqueos de escritura no se pueden adquirir con sesiones o cursores que tengan permisos de solo lectura, incluso si la sesión y el cursor en última instancia no realizan una operación de actualización. Tanto la sesión como el cursor deben tener privilegios de escritura para adquirir un bloqueo de escritura.

Los bloqueos de lectura y escritura son un medio de bloqueo pesimista. El bloqueo pesimista espera que varias sesiones simultáneas entren en conflicto y adquieran bloqueos de antemano para asegurarse de que sus operaciones se ejecutan correctamente.

La mayoría de las operaciones se serializarán en virtud de los bloqueos tomados implícitamente. Sin embargo, algunas operaciones no lo harán. Para ilustrar esto, tenga en cuenta las dos transacciones:

T1: R(A), U(B)

T2: R(B), U(A)

El control de versiones de nivel de registro garantizará que cada transacción cuando se ejecute simultáneamente verá los valores originales de A y B. No hay ningún orden de ejecución en serie que pueda producir los mismos resultados para A y B en el caso de que los resultados dependan de los datos leídos. Para que la aplicación pueda serializar esta transacción, debe adquirir un bloqueo de lectura explícito en A y B en cada transacción cuando se lee el valor.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
