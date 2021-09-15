---
description: 'Más información sobre: JetDefragment2 (Función)'
title: Función JetDefragment2
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
ms.openlocfilehash: 08e6cf618be4f3bf7f6eee1b903559db579973c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580508"
---
# <a name="jetdefragment2-function"></a>Función JetDefragment2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdefragment2-function"></a>Función JetDefragment2

La **función JetDefragment2** inicia y detiene las tareas de desfragmentación de la base de datos, lo que mejora la organización de datos dentro de una base de datos, con un parámetro de devolución de llamada disponible para informar del progreso de la desfragmentación. Esto se hace para limitar el crecimiento de la base de datos mediante la asignación de disco existente de forma más eficaz dentro de la base de datos. También puede reducir el conjunto de trabajo asegurándose de que los datos están más empaquetados. Por último, puede mejorar el rendimiento de la aplicación acelerando las operaciones comunes a través de una mejor organización de datos.

**Windows XP:****JetDefragment2** se introdujo en Windows XP.  

**JetDefragment2 también** contiene un parámetro de función de devolución de llamada que se usa para informar sobre el progreso del proceso de desfragmentación.

La desfragmentación de la base de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como las operaciones de consulta o las actualizaciones de datos. **JetDefragment2** tampoco realiza una copia de todos los datos existentes. En su lugar, desfragmenta una base de datos en su lugar. Por último, **JetDefragment2** recupera el espacio interno de la base de datos para volver a usarlo, pero no libera espacio excesivo en el sistema de archivos del sistema operativo.

El formato resultante de los datos puede ser mucho más eficaz, pero generalmente no es óptimo. La desfragmentación se limita a liberar páginas de base de datos para volver a usarlas que contienen datos que ya se han eliminado lógicamente. La desfragmentación también hace que las páginas de base de datos estén disponibles para su uso de nuevo en algunos casos mediante la combinación de datos de dos páginas cuando caben en una sola página.

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


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Esta opción se usa para desfragmentar la parte de espacio disponible de la asignación de espacio de base de datos ESE. El espacio de base de datos se divide en dos tipos: espacio de propiedad y espacio disponible. El espacio en propiedad se asigna a una tabla o índice mientras el espacio disponible está listo para su uso dentro de la tabla o índice, respectivamente. El espacio disponible es mucho más dinámico en el comportamiento y requiere desfragmentación en línea más que los datos de espacio o tabla o índice en propiedad.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Esta opción se usa para iniciar una nueva tarea de desfragmentación.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Esta opción se usa para detener una tarea de desfragmentación iniciada existente.</p> | 
| <p>JET_bitDefragmentBTree</p> | <p>Esta opción se usa para desfragmentar un árbol B, especificado por szTableName.</p> | 
| <p>JET_bitDefragmentBTreeBatch</p> | <p>Esta opción se usa para llamar a OLD2 en toda la base de datos.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ninguna manera, incluida la desfragmentación.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>La sesión dada está preparada para confirmarse y no puede iniciar nuevas actualizaciones hasta que se confirme o revierte la transacción actual.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>El identificador de base de datos especificado no coincide con una base de datos conocida de la instancia.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sesión determinada solo tiene privilegios de solo lectura y no puede iniciar una tarea que pueda realizar una actualización, incluida la desfragmentación.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>Se JET_bitDefragmentBatchStart la opción de desfragmentación, pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos especificada.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>Se ha JET_bitDefragmentBatchStop la opción de desfragmentación, pero actualmente no se está ejecutando ninguna tarea de desfragmentación.</p> | 



Si se realiza correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.

En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea. No se producen otros efectos secundarios.

#### <a name="remarks"></a>Observaciones

La desfragmentación en línea se controla mediante una configuración de parámetros, así como mediante esta API. El valor predeterminado del parámetro del sistema es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos admitidas. Sin embargo, con [JetSetSystemParameter](./jetsetsystemparameter-function.md), es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para árboles de espacio de base de datos, solo bases de datos, solo archivos de streaming o cualquier combinación de estas opciones. Si la configuración del sistema para la desfragmentación en línea es una configuración obsoleta, **JetDefragment2** tratará la configuración como JET_OnlineDefragAll.

Como máximo puede haber una tarea en ejecución para cada base de datos. La tarea se ejecuta como un subproceso en el proceso que hospeda ESE.

La sesión usada para iniciar la tarea de desfragmentación en línea se puede usar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, ya que la tarea de desfragmentación asigna su propia sesión. La sesión dada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetDefragment2W</strong> (Unicode) y <strong>JetDefragment2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
