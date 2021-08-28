---
description: 'Más información sobre: JetDupCursor (Función)'
title: Función JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 009b84837895ce13f63cc37e4b5b152f4274ee62
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985888"
---
# <a name="jetdupcursor-function"></a>Función JetDupCursor


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdupcursor-function"></a>Función JetDupCursor

La **función JetDupCursor** duplica un cursor abierto y devuelve un identificador al cursor duplicado. Si el cursor duplicado era de solo lectura, el cursor duplicado también es un cursor de solo lectura. Cualquier estado relacionado con la construcción de una clave de búsqueda o la actualización de un registro no se copia en el cursor duplicado. Además, la ubicación del cursor original no se duplica en el cursor duplicado. El cursor duplicado siempre se abre en el índice clúster y su ubicación siempre está en la primera fila de la tabla.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*ptableid*

Puntero a *tableid.*

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errOutOfCursors</p> | <p>No existen recursos de cursor disponibles.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta *correctamente, ptableid* se establece en un cursor duplicado.

En caso de error, no se realiza ningún cambio. El estado de *tableid* no ha cambiado.

#### <a name="remarks"></a>Observaciones

El cursor duplicado no tiene copiado todo el estado del cursor. La ubicación del cursor duplicado, incluido el índice actual, suele ser diferente del cursor especificado. El cursor duplicado siempre se devuelve en el índice clúster y en la primera fila de la tabla. Si la tabla está vacía, el cursor duplicado no está en ninguna fila.

Las tablas **abiertas con JetDupCursor** normalmente deben cerrarse [con JetCloseTable.](./jetclosetable-function.md) La excepción a esta regla se produce cuando se llama a **JetDupCursor** en una transacción y la transacción se revierte [(con JetRollback).](./jetrollback-function.md) Al revertir una transacción, el cursor se cierra automáticamente. En este caso, es un error cerrar la tabla con [JetCloseTable](./jetclosetable-function.md).

El número de tablas que se pueden abrir simultáneamente se ve afectado directamente por [JET_paramMaxOpenTables](./resource-parameters.md). Consulte [Parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener más información.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
