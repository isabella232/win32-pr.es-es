---
description: 'Más información sobre: JetSetSessionContext (Función)'
title: JetSetSessionContext (Función)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ac368caaff5ec652a6dc7ad490e7418e62888b7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986638"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionContext (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionContext (Función)

La **función JetSetSessionContext** asocia una sesión al subproceso actual mediante el identificador de contexto especificado. Esta asociación invalida el requisito predeterminado del motor de que una transacción para una sesión determinada debe producirse completamente en el mismo subproceso.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*ulContext*

Identificador único al que se asociará esta sesión.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado. <strong>JetSetSessionContext</strong> devolverá este error en las condiciones siguientes:</p><ul><li><p><em>ulContext</em> es NULL</p></li><li><p><em>ulContext</em> es -1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>No se pudo asociar la sesión al subproceso actual porque ya se ha asociado a un subproceso.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia de asociada a la sesión.</p> | 



Si esta función se realiza correctamente, la sesión se asociará al subproceso actual. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, el estado de sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Normalmente, una sesión se enlaza a un subproceso específico mientras dura una transacción. Este comportamiento está diseñado para ayudar a las aplicaciones a detectar y evitar el uso compartido conceptualmente mal aconsejado de una sola sesión entre varios subprocesos. A veces, esta sencilla comprobación no funciona con la arquitectura de la aplicación. Por ejemplo, si la aplicación hospeda objetos del lado servidor mediante un grupo de subprocesos y las transacciones abarcan varias llamadas de servidor a un objeto determinado, esta protección puede hacer que algunas de esas llamadas no se puedan realizar con JET_errSessionSharingViolation aunque el patrón de uso sea correcto. Esta situación es común para los servidores de objetos COM.

**JetSetSessionContext** y [JetResetSessionContext](./jetresetsessioncontext-function.md) solucionan este problema haciendo que esta comprobación de uso compartido de sesión sea un poco más flexible. Cuando la aplicación comienza a realizar una serie de llamadas API de ESE mediante una sesión determinada, primero establece el contexto de sesión en un valor determinado. Esta acción asocia la sesión al subproceso que realiza la llamada. En el ejemplo dado, este contexto podría ser la dirección del objeto que contiene el identificador de sesión jet. Una vez realizadas las llamadas API de ESE, la aplicación restablece el contexto de sesión. Esta acción desasocia la sesión del subproceso que realiza la llamada. Otro subproceso puede usar el objeto y su sesión, incluso si la sesión tiene una transacción activa.

Es importante tener en cuenta que se debe llamar a **JetSetSessionContext** antes de abrir una transacción en esa sesión o la asociación no funcionará.

**JetSetSessionContext** es seguro para subprocesos. Varios subprocesos pueden intentar establecer un contexto de subproceso en la misma sesión al mismo tiempo y solo uno ganará. La aplicación puede usar este hecho como medio para asignar una sesión de un grupo sin almacenar el estado externo sobre su asignación.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
