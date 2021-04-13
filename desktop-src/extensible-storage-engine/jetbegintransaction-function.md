---
description: 'Más información acerca de: JetBeginTransaction (función)'
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
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360132"
---
# <a name="jetbegintransaction-function"></a>Función JetBeginTransaction


_**Se aplica a:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>Función JetBeginTransaction

La función **JetBeginTransaction** hace que una sesión escriba una transacción y cree un nuevo punto de retorno. Esta función se puede llamar más de una vez en una sola sesión para provocar la creación de puntos de almacenamiento adicionales. Estos puntos de almacenamiento se pueden usar para conservar o descartar cambios de forma selectiva en el estado de la base de datos.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima del punto de almacenamiento permitida por el motor de base de datos.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción. Si la sesión se encontraba anteriormente en una transacción, se creará un nuevo punto de retorno.

En caso de error, el estado transaccional de la sesión permanecerá sin cambios. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

El motor de base de datos proporciona un modelo de aislamiento de instantánea para sus transacciones. Esto significa que, cuando una sesión entra en un estado transaccional, la sesión verá toda la base de datos en el momento en que se inicia la transacción. Una sesión no tiene que leer bloquear los datos porque siempre puede tener acceso a la versión adecuada de los datos. Esto significa que una sesión que está actualizando los datos nunca impedirá que una sesión diferente Lea los datos.

Otra implicación del uso del aislamiento de instantánea es el modelo de bloqueo que se usa para las actualizaciones. El motor de base de datos adjudicará un bloqueo de escritura en un determinado dato a la primera sesión que lo solicite. Este bloqueo de escritura se libera cuando la transacción se confirma o se anula completamente de forma que la sesión ya no se encuentra en una transacción. Mientras una sesión mantiene un bloqueo de escritura, cualquier otra sesión que solicite el mismo bloqueo de escritura no se bloqueará hasta que el bloqueo de escritura esté disponible. En su lugar, se producirá un error inmediato en esa segunda sesión con JET_errWriteConflict. Para resolver este conflicto, la segunda sesión debe anular (o confirmar) completamente su transacción, esperar un pequeño período de tiempo para que la primera sesión confirme o anule su transacción y, a continuación, vuelva a iniciarla.

En cuanto a la compatibilidad con el aislamiento de instantánea, el motor de base de datos almacena todas las versiones de todos los datos modificados en la memoria desde el momento en que se inició por primera vez la transacción activa más antigua en cualquier sesión. Esto tiene implicaciones importantes para la aplicación. Cualquier comportamiento que cause un gran número de versiones para compilar en memoria puede hacer que la instancia agote su tamaño máximo de almacén de versiones (consulte [JET_paramMaxVerPages](./resource-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener más información). Este comportamiento incluye, pero no se limita a las actualizaciones muy grandes en una única transacción y transacciones de ejecución muy prolongada. Como resultado, es muy importante configurar correctamente el tamaño del almacén de versiones para la carga transaccional esperada de la aplicación. También es importante tener mucho cuidado para limitar el número de actualizaciones realizadas en una sola transacción. Además, es importante que las transacciones sean lo más cortas posible en situaciones de carga elevada.

Se recomienda encarecidamente que la aplicación esté siempre en el contexto de una transacción al llamar a las API de ESE que recuperan o actualizan los datos. Si no se hace esto, el motor de base de datos ajustará automáticamente cada llamada de API de ESE tipo en una transacción en nombre de la aplicación. El costo de estas transacciones muy cortas puede agregarse rápidamente en algunos casos.

El comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a **JetBeginTransaction** hasta el momento en que se realiza la llamada coincidente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) . Este comportamiento se puede cambiar para quitar esta restricción mediante la configuración de un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).

El motor de base de datos también admite modificaciones de esquema transaccionales. Por ejemplo, se puede iniciar una nueva transacción, crear una tabla, agregar algunas columnas, crear un índice o dos y, después, anular la transacción. Los elementos de esquema que se acaban de agregar se quitarán de la base de datos. También es posible mezclar las modificaciones de esquema y las actualizaciones de bases de datos normales en la misma transacción.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
