---
description: 'Más información sobre: JetEscrowUpdate (Función)'
title: Función JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469802"
---
# <a name="jetescrowupdate-function"></a>Función JetEscrowUpdate


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetescrowupdate-function"></a>Función JetEscrowUpdate

La **función JetEscrowUpdate** realiza una operación de suma atómica en una columna. Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*columnid*

Columnid *de* la columna que se va a actualizar.

*Pv*

Puntero a un búfer que contiene el anexo de la columna.

*cbMax*

Tamaño del búfer que contiene el complemento.

*pvOld*

Búfer de salida que recibirá el valor actual de la columna tal como se almacena en la base de datos (se omite el control de versiones).

*cbOldMax*

Tamaño máximo del búfer de salida que recibirá el valor actual de la columna. Actualmente solo JET_coltypLong admite, por lo que el búfer debe tener una longitud de 4 o 0 bytes. Si *pvOld* es NULL, *cbOldMax* debe ser 0.

*pwOldActual*

Recibe la cantidad real de datos de valor sin procesar recibidos en el búfer de salida.

*grbit*

Grupo de bits que especifica cero o más de las siguientes opciones.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>Incluso si la sesión que realiza la actualización de custodia tiene su reversión de transacciones, esta actualización no se deshacerá. Tenga en cuenta que, como es posible que las entradas de registro no se vacían en el disco, las actualizaciones recientes de custodia realizadas con esta marca se pueden perder si se produce un bloqueo.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>El cursor tiene una actualización preparada con <a href="gg269339(v=exchg.10).md">JetPrepareUpdate.</a></p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Se ha pasado un tamaño de búfer no válido. Actualmente solo JET_coltypLong se admite, por lo que el búfer debe ser de 4 bytes.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Se ha especificado una columna no válida. La columna debe crearse con JET_bitColumnEscrowUpdate especificado. Solo las columnas fijas JET_coltypLong pueden especificarse como actualizables por custodia.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor debe estar en un registro para actualizar una columna.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Las actualizaciones de custodia solo las pueden realizar las sesiones de una transacción.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errPermissionDenied</p> | <p>El cursor no puede ser de solo lectura y actualizar un registro.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión desde más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sesión debe tener permisos de escritura para actualizar un registro.</p> | 
| <p>JET_errWriteConflict</p> | <p>Error devuelto cuando se solicita una actualización en conflicto.</p> | 



#### <a name="remarks"></a>Comentarios

Normalmente, si dos sesiones intentan actualizar un registro simultáneamente, la segunda sesión recibirá un error JET_errWriteConflict a menos que las sesiones se serializan completamente. Para serializar dos sesiones que actualizan el mismo registro, la segunda sesión debe iniciar su transacción después de que la primera transacción confirme su transacción. Consulte [JetBeginTransaction para](./jetbegintransaction-function.md) obtener más información.

Se pueden actualizar varias columnas del mismo registro. Las actualizaciones no se afectan entre sí.

Solo **las operaciones JetEscrowUpdate** son compatibles entre sí. Si dos sesiones diferentes intentan preparar actualizaciones o eliminar el mismo registro, se generará un conflicto de escritura.


| <p></p> | <p></p> | <p>Sesión B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>Sesión A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



Las operaciones de custodia tienen versiones y se desechan [mediante JetRollback](./jetrollback-function.md) (a menos que JET_bitEscrowNoRollback se especifique). **JetEscrowUpdate** devuelve el valor sin procesar de la columna almacenada en la base de datos, ya que es posible que una aplicación quiera realizar una acción especial cuando se llegue a un valor centinela. [JetRetrieveColumn devuelve](./jetretrievecolumn-function.md) la vista con versiones correctas de la columna, omitiendo las actualizaciones realizadas por sesiones simultáneas.

Dadas dos sesiones que funcionan en la misma columna del mismo registro, podemos ver cómo funciona. Suponga que la columna comienza con un valor de 0.


| <p>Sesión</p> | <p>Operación</p> | <p>Valor almacenado</p> | <p>Valor devuelto</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (4)</p> | <p>4</p> | <p>0</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3)</p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (2)</p> | <p>9</p> | <p>7</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (-7)</p> | <p>2</p> | <p>9</p> | 
| <p>N</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



No se recomienda reemplazar un registro en la misma transacción que realiza actualizaciones de custodia en un registro. En concreto, si se prepara una actualización en un registro [](./jet-tableid.md) con un [JET_TABLEID](./jet-tableid.md) y se usa un JET_TABLEID diferente para custodiar la actualización del registro, la custodia actualizada se perderá cuando se llame a [JetUpdate.](./jetupdate-function.md) Esto sucede incluso si la columna de custodia no se estableció durante la actualización.

Cuando una columna actualizable de custodia tiene un valor de cero, se puede desencadenar un comportamiento especial. Este comportamiento solo se produce si una **operación JetEscrowUpdate** hace que la columna tenga un valor de cero. La acción no se produce inmediatamente, pero se produce en algún momento después de la transacción que hizo que la columna tenga un valor de cero confirmaciones. La columna todavía debe tener un valor de cero (es decir, si ninguna otra sesión ha modificado la columna). Si la columna se creó JET_bitColumnDeleteOnZero, se eliminará el registro que contiene la columna. Si la columna se creó con JET_bitColumnFinalize, se emitirá una devolución de llamada. Un bloqueo puede provocar que estas acciones no se sucedan, pero el mantenimiento en línea (mediante la [función JetDefragment)](./jetdefragment-function.md) volverá a realizar correctamente las acciones.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
