---
description: 'Más información acerca de: JetDefragment (función)'
title: JetDefragment función)
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361586"
---
# <a name="jetdefragment-function"></a>JetDefragment función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetdefragment-function"></a>JetDefragment función)

La función **JetDefragment** inicia y detiene las tareas de desfragmentación de bases de datos que mejoran la organización de datos en una base de datos. Esto se hace para limitar el crecimiento de la base de datos mediante la asignación de disco existente de forma más eficaz en la base de datos. También puede reducir el espacio de trabajo asegurándose de que los datos se empaquetan con mayor precisión. Por último, puede mejorar el rendimiento de la aplicación al acelerar las operaciones comunes a través de una mejor organización de datos.

La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como operaciones de consulta o actualizaciones de datos. **JetDefragment** tampoco realiza una copia de todos los datos existentes. En su lugar, desfragmenta una base de datos en su lugar. Por último, **JetDefragment** recupera el espacio interno de la base de datos para su reutilización, pero no libera espacio sobrante en el sistema de archivos del sistema operativo.

El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo. La desfragmentación se limita a liberar páginas de base de datos para que se vuelvan a usar, que contienen datos que ya se han eliminado lógicamente. La desfragmentación también hace que las páginas de base de datos estén disponibles para su reutilización en algunos casos mediante la combinación de datos de dos páginas cuando quepa en una sola página.

Esta operación es diferente de [JetCompact](./jetcompact-function.md) , que realiza una copia de una base de datos de solo lectura en una forma muy óptima.

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*DBID*

Base de datos que se va a desfragmentar.

*szTableName*

Parámetro sin usar. La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.

*pcPasses*

Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada establece el número máximo de pasos de desfragmentación. Al detener una tarea de desfragmentación con conexión, este búfer de salida se establece en el número de pasos realizados.

Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.

*pcSeconds*

Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada establece el tiempo máximo de desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida se establece en el período de tiempo utilizado para la desfragmentación.

Cuando este parámetro se establece en NULL o si *pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Desfragmenta la parte de espacio disponible de la asignación de espacio de la base de datos de ESE. El espacio de la base de datos se divide en dos tipos, espacio de propiedad y espacio disponible. El espacio de propiedad se asigna a una tabla o un índice mientras que el espacio disponible está listo para su uso en la tabla o el índice, respectivamente. El espacio disponible es mucho más dinámico en el comportamiento y requiere una desfragmentación en línea más que el espacio de propiedad o los datos de la tabla o el índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Inicia una nueva tarea de desfragmentación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Detiene una tarea de desfragmentación.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ningún modo, incluida la desfragmentación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>La sesión determinada está en el estado preparado para confirmar y no puede iniciar nuevas actualizaciones hasta que la transacción actual se confirma o se revierte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>El identificador de base de datos especificado no coincide con una base de datos conocida en la instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sesión determinada solo tiene privilegios de solo lectura y no puede iniciar una tarea que pueda realizar una actualización, incluida la desfragmentación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>Se ha pasado la opción de JET_bitDefragmentBatchStart pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos dada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>Se pasó la opción de JET_bitDefragmentBatchStop, pero no se está ejecutando ninguna tarea de desfragmentación.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.

En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea. No se produce ningún otro efecto secundario.

#### <a name="remarks"></a>Observaciones

La desfragmentación con conexión se controla a través de una configuración de parámetros, así como de esta API. El valor predeterminado del parámetro System es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos compatibles. Sin embargo, el uso de [JetSetSystemParameter](./jetsetsystemparameter-function.md)es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para los árboles de espacio de base de datos, solo para las bases de datos, archivos de streaming o cualquier combinación de estas opciones. Si la configuración del sistema para desfragmentación en línea se establece en una configuración obsoleta, **JetDefragment** tratará la configuración como JET_OnlineDefragAll.

Puede haber como máximo una tarea que se ejecute para cada base de datos. La tarea se ejecuta como un subproceso en el proceso que hospeda ESE.

La sesión utilizada para iniciar la tarea de desfragmentación con conexión se puede utilizar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, porque la tarea de desfragmentación asigna su propia sesión. La sesión determinada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetDefragmentW</strong> (Unicode) y <strong>JetDefragmentA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment2](./jetdefragment2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
