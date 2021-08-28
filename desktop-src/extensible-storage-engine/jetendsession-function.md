---
description: 'Más información sobre: JetEndSession (Función)'
title: JetEndSession (Función)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b96ae49ef907cea158d1496339a740e1026ffea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472571"
---
# <a name="jetendsession-function"></a>JetEndSession (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetendsession-function"></a>JetEndSession (Función)

La **función JetEndSession** finaliza la sesión, limpia y desasigna los recursos asociados a la sesión especificada.

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se finalizará. Los recursos asociados se liberan cuando finaliza la sesión.

*grbit*

Reservado. Este parámetro puede contener la JET_bitForceSessionClosed, pero esta marca está reservada y su configuración no tiene ningún efecto.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</p> | 
| <p>JET_errInvalidSesid</p> | <p>La sesión no era una sesión JET válida.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar memoria.</p> | 
| <p>JET_errSessionInUse</p> | <p>Esto significa que la sesión estaba en uso en otro subproceso o que la sesión no se estableció ni restablecó correctamente.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errOutOfBuffers</p> | <p>Error del sistema que indica que no hay más búferes.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, el identificador de sesión se cierra y no está disponible, y se limpian todos los recursos relacionados con esta sesión.

En caso de error, hay varios errores adicionales que podrían producirse como parte del cierre de la tabla de ordenación, el cierre del cursor y la reversión de transacciones. Estos errores son bastante improbables y muy poco probables si las sesiones no están completamente en uso cuando se llama a **JetEndSession.** Estos errores se devolverán si alguna parte de la sesión no se pudo limpiar correctamente.

#### <a name="remarks"></a>Comentarios

Esta API revertirá las transacciones abiertas (no confirmadas en el nivel 0). También se limpiarán todos los cursores asociados a esta sesión y las tablas de ordenación que se hayan creado o abierto.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
