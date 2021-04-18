---
description: 'Más información acerca de: JetDefragment2 (función)'
title: JetDefragment2 función)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105721555"
---
# <a name="jetdefragment2-function"></a>JetDefragment2 función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2 función)

La función **JetDefragment2** inicia y detiene las tareas de desfragmentación de bases de datos que mejoran la organización de datos en una base de datos, con un parámetro de devolución de llamada disponible para informar del progreso de la desfragmentación. Esto se hace para limitar el crecimiento de la base de datos mediante la asignación de disco existente de forma más eficaz en la base de datos. También puede reducir el espacio de trabajo asegurándose de que los datos se empaquetan con mayor precisión. Por último, puede mejorar el rendimiento de la aplicación al acelerar las operaciones comunes a través de una mejor organización de datos.

**Windows XP:**  **JetDefragment2** se presentó en Windows XP.

**JetDefragment2** también contiene un parámetro de función de devolución de llamada que se usa para informar sobre el progreso del proceso de desfragmentación.

La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como operaciones de consulta o actualizaciones de datos. **JetDefragment2** tampoco realiza una copia de todos los datos existentes. En su lugar, desfragmenta una base de datos en su lugar. Por último, **JetDefragment2** recupera el espacio interno de la base de datos para su reutilización, pero no libera espacio sobrante en el sistema de archivos del sistema operativo.

El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo. La desfragmentación se limita a liberar páginas de base de datos para que se vuelvan a usar, que contienen datos que ya se han eliminado lógicamente. La desfragmentación también hace que las páginas de base de datos estén disponibles para su reutilización en algunos casos mediante la combinación de datos de dos páginas cuando quepa en una sola página.

Esta operación es diferente de [JetCompact](./jetcompact-function.md) , que realiza una copia de una base de datos de solo lectura en una forma muy óptima.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
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

Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada opcional establece el número máximo de pasos de desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el número de pasos realizados.

Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.

*pcSeconds*

Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada opcional establece el tiempo máximo de desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el período de tiempo utilizado para la desfragmentación.

Cuando este parámetro se establece en NULL o si *pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.

*devolución de llamada*

Función de devolución de llamada que la desfragmentación llama regularmente para informar del progreso.

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
<td><p>Esta opción se usa para desfragmentar la parte de espacio disponible de la asignación de espacio de base de datos de ESE. El espacio de la base de datos se divide en dos tipos, espacio de propiedad y espacio disponible. El espacio de propiedad se asigna a una tabla o un índice mientras que el espacio disponible está listo para su uso en la tabla o el índice, respectivamente. El espacio disponible es mucho más dinámico en el comportamiento y requiere una desfragmentación en línea más que el espacio de propiedad o los datos de la tabla o el índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Esta opción se usa para iniciar una nueva tarea de desfragmentación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Esta opción se usa para detener una tarea de desfragmentación iniciada existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Esta opción se usa para desfragmentar un árbol B.</p></td>
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

La desfragmentación con conexión se controla a través de una configuración de parámetros, así como de esta API. El valor predeterminado del parámetro System es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos compatibles. Sin embargo, el uso de [JetSetSystemParameter](./jetsetsystemparameter-function.md)es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para los árboles de espacio de base de datos, solo para las bases de datos, archivos de streaming o cualquier combinación de estas opciones. Si la configuración del sistema para la desfragmentación en línea es un valor obsoleto, **JetDefragment2** tratará la configuración como JET_OnlineDefragAll.

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
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
<td><p>Se implementa como <strong>JetDefragment2W</strong> (Unicode) y <strong>JetDefragment2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
