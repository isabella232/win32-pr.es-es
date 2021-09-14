---
description: 'Más información sobre: JetUnregisterCallback (Función)'
title: JetUnregisterCallback (Función)
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87c308f4895eb3e78a35338fe39afb3d775da095
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269700"
---
# <a name="jetunregistercallback-function"></a>JetUnregisterCallback (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetunregistercallback-function"></a>JetUnregisterCallback (Función)

La **función JetUnregisterCallback permite** a la aplicación configurar el motor de base de datos para dejar de emitir notificaciones a la aplicación como se solicitó anteriormente a través de [JetRegisterCallback](./jetregistercallback-function.md).

**Windows XP:****JetUnregisterCallback** se introduce en Windows XP.  

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*cbtyp*

Máscara de bits compuesta por las razones de devolución de llamada por las que la aplicación ya no desea recibir notificaciones.

Para crear esta máscara de bits, simplemente o juntos los motivos de devolución de llamada válidos de la [JET_CBTYP](./jet-cbtyp.md) enumeración.

*hCallbackId*

Identificador de la devolución de llamada registrada devuelta por [JetRegisterCallback.](./jetregistercallback-function.md)

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irrevocado que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque todavía no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia asociada a la sesión.</p> | 



Si esta función se realiza correctamente, se anulará el registro de la devolución de llamada especificada por los motivos de devolución de llamada especificados con la tabla asociada al cursor especificado. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, la devolución de llamada especificada no se anulará del registro. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

La máscara de bits especificada debe coincidir exactamente con la máscara de bits que se especifica al registrar la devolución de llamada. El motor de base de datos no admite actualmente la eliminación de un subconjunto de estas notificaciones y no devuelve un error cuando se intenta.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetStopService](./jetstopservice-function.md)
