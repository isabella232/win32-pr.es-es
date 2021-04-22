---
description: 'Más información sobre: JetDefragment2 (Función)'
title: JetDefragment2 (Función)
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
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838809"
---
# <a name="jetdefragment2-function"></a>JetDefragment2 (Función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2 (Función)

La **función JetDefragment2** inicia y detiene las tareas de desfragmentación de la base de datos, lo que mejora la organización de datos dentro de una base de datos, con un parámetro de devolución de llamada disponible para informar del progreso de la desfragmentación. Esto se hace para limitar el crecimiento de la base de datos mediante el uso de la asignación de disco existente de forma más eficaz dentro de la base de datos. También puede reducir el conjunto de trabajo asegurándose de que los datos están más empaquetados. Por último, puede mejorar el rendimiento de la aplicación acelerando las operaciones comunes a través de una mejor organización de datos.

**Windows XP:**  **JetDefragment2** se introdujo en Windows XP.

**JetDefragment2 también** contiene un parámetro de función de devolución de llamada que se usa para informar sobre el progreso del proceso de desfragmentación.

La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como las operaciones de consulta o las actualizaciones de datos. **JetDefragment2** tampoco realiza una copia de todos los datos existentes. En su lugar, desfragmenta una base de datos en su lugar. Por último, **JetDefragment2** recupera el espacio interno de la base de datos para volver a usarlo, pero no libera espacio excesivo en el sistema de archivos del sistema operativo.

El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo. La desfragmentación se limita a liberar páginas de base de datos para volver a usar que contienen datos que ya se han eliminado lógicamente. La desfragmentación también hace que las páginas de base de datos estén disponibles para su uso de nuevo en algunos casos mediante la combinación de datos de dos páginas cuando caben en una sola página.

Esta operación es diferente de [JetCompact,](./jetcompact-function.md) que convierte una copia de una base de datos de solo lectura en un formato muy óptimo.

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

*Dbid*

Base de datos que se desfragmenta.

*szTableName*

A *veces se requiere szTableName* y, a veces, está prohibido:

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Debe ser `NULL`. |
| `JET_bitDefragmentBTree` | Especifica el nombre de la tabla o el árbol B que se va a desfragmentar. |
| *Otro* | Debe ser `NULL`. |
 
La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.

*pcPasses*

Al iniciar una tarea de desfragmentación en línea, este parámetro de entrada opcional establece el número máximo de pases de desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el número de pases realizados.

Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.

*pcSeconds*

Al iniciar una tarea de desfragmentación en línea, este parámetro de entrada opcional establece el tiempo máximo para la desfragmentación. Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el período de tiempo utilizado para la desfragmentación.

Cuando este parámetro se establece en NULL o *si pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.

*devolución de llamada*

Función de devolución de llamada que llama periódicamente a la desfragmentación para informar del progreso.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Debe ser `NULL`. |
| `JET_bitDefragmentBTree` | Debe ser `NULL`. |
| *Otro* | Opcional.


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
<td><p>Esta opción se usa para desfragmentar la parte de espacio disponible de la asignación de espacio de base de datos ese. El espacio de base de datos se divide en dos tipos: espacio de propiedad y espacio disponible. El espacio de propiedad se asigna a una tabla o índice, mientras que el espacio disponible está listo para su uso dentro de la tabla o el índice, respectivamente. El espacio disponible es mucho más dinámico en el comportamiento y requiere desfragmentación en línea más que los datos de espacio o tabla o índice en propiedad.</p></td>
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
<td><p>Esta opción se usa para desfragmentar un árbol B, especificado por szTableName.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBTreeBatch</p></td>
<td><p>Esta opción se usa para llamar a OLD2 en toda la base de datos.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Errores extensibles del motor](./extensible-storage-engine-errors.md) de almacenamiento y Parámetros de control de [errores.](./error-handling-parameters.md)

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
<td><p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ninguna manera, incluida la desfragmentación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>La sesión dada está en el estado preparado para confirmarse y no puede iniciar nuevas actualizaciones hasta que se confirme o revierte la transacción actual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>El identificador de base de datos especificado no coincide con una base de datos conocida de la instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
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
<td><p>La JET_bitDefragmentBatchStart se ha pasado, pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>Se ha JET_bitDefragmentBatchStop la opción de desfragmentación, pero actualmente no se está ejecutando ninguna tarea de desfragmentación.</p></td>
</tr>
</tbody>
</table>


Si se realiza correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.

En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea. No se producen otros efectos secundarios.

#### <a name="remarks"></a>Observaciones

La desfragmentación en línea se controla mediante una configuración de parámetros, así como mediante esta API. El valor predeterminado del parámetro del sistema es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos admitidas. Sin embargo, con [JetSetSystemParameter](./jetsetsystemparameter-function.md), es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para árboles de espacio de base de datos, solo bases de datos, solo archivos de streaming o cualquier combinación de estas opciones. Si la configuración del sistema para la desfragmentación en línea es una configuración obsoleta, **JetDefragment2** tratará la configuración como JET_OnlineDefragAll.

Puede haber como máximo una tarea en ejecución para cada base de datos. La tarea se ejecuta como un subproceso en el proceso que hospeda ese.

La sesión utilizada para iniciar la tarea de desfragmentación en línea se puede usar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, porque la tarea de desfragmentación asigna su propia sesión. La sesión dada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa <strong>como JetDefragment2W</strong> (Unicode) y <strong>JetDefragment2A</strong> (ANSI).</p></td>
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
