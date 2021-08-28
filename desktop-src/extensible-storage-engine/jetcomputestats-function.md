---
description: 'Más información sobre: JetComputeStats (Función)'
title: JetComputeStats (Función)
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d990e4ded7dc2485bec6b5ecf92d9999aad57ce5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981978"
---
# <a name="jetcomputestats-function"></a>JetComputeStats (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcomputestats-function"></a>JetComputeStats (Función)

La **función JetComputeStats** recorre cada índice de una tabla para calcular exactamente el número de entradas de un índice y el número de claves distintas de un índice. Esta información, junto con el número de páginas de base de datos asignadas para un índice y la hora actual del cálculo se almacena en metadatos de índice en la base de datos. Estos datos se pueden recuperar posteriormente con operaciones de información.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se usará para esta llamada. Describe la tabla en la que se calculan las estadísticas.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRollbackError</p> | <p>Se produjo un error que requiere que esta operación revierta todos los cambios, pero se produjo un error en la reversión de la transacción.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, las estadísticas actualizadas se almacenan en los catálogos de base de datos de la tabla descrita con el cursor dado.

En caso de error, no se realiza ninguna actualización de ningún tipo en la base de datos.

#### <a name="remarks"></a>Observaciones

Esta operación puede consumir recursos, ya que cada índice de una tabla se debe seguir en su totalidad. [JetGetRecordPosition](./jetgetrecordposition-function.md) se puede usar para obtener una estimación aproximada del número de entradas de un índice, pero no puede calcular por sí misma el número de valores distintos de un índice.

Los datos calculados por esta operación comienzan a estar desactualados y la tabla se actualiza posteriormente.

Las actualizaciones de la base de datos realizadas por **JetComputeStats** se realizan de forma diferida. Esto significa que esta operación no va a ir acompañada de ningún vaciado del registro y que un bloqueo del sistema posterior a la devolución de JET_errSuccess por Parte de **JetComputeStats** puede seguir provocando la pérdida de estas actualizaciones.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)
