---
description: 'Más información sobre: JetBeginTransaction (Función)'
title: Función JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 991f80ab346ae039c6222a508374de806d0faf2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479271"
---
# <a name="jetbegintransaction-function"></a>Función JetBeginTransaction


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbegintransaction-function"></a>Función JetBeginTransaction

La **función JetBeginTransaction** hace que una sesión escriba una transacción y cree un nuevo punto de guardado. Se puede llamar a esta función más de una vez en una sola sesión para provocar la creación de puntos de guardado adicionales. Estos puntos de guardado se pueden usar para mantener o descartar selectivamente los cambios en el estado de la base de datos.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransTooDeep</p> | <p>No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad de punto de guardado máxima que permite el motor de base de datos.</p> | 



Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción. Si la sesión estaba anteriormente dentro de una transacción, se creará un nuevo punto de guardado.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Comentarios

El motor de base de datos proporciona un modelo de aislamiento de instantáneas para sus transacciones. Esto significa que, cuando una sesión entra por primera vez en un estado transaccional, la sesión verá toda la base de datos inmovilizada a tiempo al principio de la transacción. Una sesión no necesita leer ningún dato de bloqueo porque siempre puede tener acceso a la versión adecuada de los datos. Esto significa que una sesión que actualiza los datos nunca impedirá que una sesión diferente lea los datos.

Otra implicación del uso del aislamiento de instantáneas es el modelo de bloqueo utilizado para las actualizaciones. El motor de base de datos concederá un bloqueo de escritura en un fragmento de datos determinado a la primera sesión que lo solicite. Este bloqueo de escritura se libera cuando la transacción se confirma o se anula completamente, de modo que la sesión ya no está en una transacción. Mientras una sesión contiene un bloqueo de escritura, cualquier otra sesión que solicite el mismo bloqueo de escritura no se bloqueará hasta que el bloqueo de escritura esté disponible. En su lugar, esa segunda sesión producirá un error inmediatamente con JET_errWriteConflict. Para resolver este conflicto, la segunda sesión debe anular (o confirmar) su transacción por completo, esperar un breve período de tiempo para que la primera sesión confirme o anule su transacción y, a continuación, volver a iniciarla de nuevo.

Para admitir el aislamiento de instantáneas, el motor de base de datos almacena todas las versiones de todos los datos modificados en memoria desde el momento en que se inició por primera vez la transacción activa más antigua en cualquier sesión. Esto tiene implicaciones importantes para la aplicación. Cualquier comportamiento que hace que un gran número de versiones se compile en memoria puede hacer [](./extensible-storage-engine-system-parameters.md) que la instancia agote su tamaño máximo de almacén de versiones (consulte [JET_paramMaxVerPages](./resource-parameters.md) en Parámetros del sistema para obtener más información). Este comportamiento incluye, entre otras, actualizaciones muy grandes en una sola transacción y transacciones de ejecución muy larga. Como resultado, es muy importante configurar correctamente el tamaño del almacén de versiones para la carga transaccional esperada de la aplicación. También es importante tener mucho cuidado para limitar el número de actualizaciones realizadas en una sola transacción. Además, es importante que las transacciones se realicen lo más corta posible en escenarios de carga alta.

Se recomienda encarecidamente que la aplicación siempre esté en el contexto de una transacción al llamar a las API de ESE que recuperan o actualizan datos. Si esto no se hace, el motor de base de datos encapsulará automáticamente cada llamada API ese de este tipo en una transacción en nombre de la aplicación. El costo de estas transacciones muy cortas puede sumar rápidamente en algunos casos.

El comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a **JetBeginTransaction** hasta el momento en que se realiza la llamada correspondiente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Este comportamiento se puede cambiar para quitar esta restricción estableciendo un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).

El motor de base de datos también admite modificaciones de esquema transaccional. Por ejemplo, es posible iniciar una nueva transacción, crear una tabla, agregar algunas columnas, crear un índice o dos y, a continuación, anular la transacción. Los elementos de esquema que se acaba de agregar se quitarán de la base de datos. También es posible mezclar modificaciones de esquema y actualizaciones de base de datos normales en la misma transacción.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
