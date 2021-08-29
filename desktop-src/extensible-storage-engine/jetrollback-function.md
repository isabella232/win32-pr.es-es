---
description: 'Más información sobre: JetRollback (Función)'
title: JetRollback (Función)
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7918d1d9568848dfcd77a09ea777dba93bb2ab2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475811"
---
# <a name="jetrollback-function"></a>JetRollback (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetrollback-function"></a>JetRollback (Función)

La **función JetRollback** deshace los cambios realizados en el estado de la base de datos y vuelve al último punto de guardado. **JetRollback también** cerrará los cursores abiertos durante el punto de guardado. Si se desecha el punto de guardado más externo, la sesión cerrará la transacción.

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRollbackAll</p> | <p>Esta opción solicita que todos los cambios realizados en el estado de la base de datos durante todos los puntos de guardado se desenconsonen. Como resultado, la sesión cerrará la transacción.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Error en la operación porque la sesión dada no está en una transacción.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRollbackError</p> | <p>No era posible revertir los cambios debido a un error irrespeto.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se realiza correctamente, los cambios realizados en la base de datos durante el punto de guardado actual de la sesión determinada se deshacerán y ese punto de guardado finalizará. Si se finalizó el último punto de guardado de la sesión, la sesión cerrará la transacción.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos. Un error durante la reversión se considera un error catastrófico de la base de datos.

#### <a name="remarks"></a>Comentarios

Debe haber una llamada a [JetCommitTransaction](./jetcommittransaction-function.md) o **JetRollback** para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.

Si se han abierto cursores (por ejemplo, [con JetOpenTable)](./jetopentable-function.md)durante un punto de guardado que se va a revertir, ese cursor se cerrará.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
