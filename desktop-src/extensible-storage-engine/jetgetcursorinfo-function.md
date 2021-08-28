---
description: 'Más información sobre: JetGetCursorInfo (Función)'
title: JetGetCursorInfo (Función)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6c26aa69f1ac51cdd9d70ca93c4fc42df5356ee
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987668"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo (Función)

La **función JetGetCursorInfo** se usa para determinar si una actualización del registro actual de un cursor dará lugar a un conflicto de escritura, en función del estado de actualización actual del registro. Es posible que, en última instancia, se devuelva un conflicto de escritura incluso si **JetGetCursorInfo** devuelve JET_errSuccess, ya que otra sesión puede actualizar el registro antes de que la sesión actual pueda actualizar el mismo registro.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se usará para esta llamada.

*tableid*

Cursor que se usará para esta llamada.

*pvResult*

Reservado para uso futuro.

*cbMax*

Debe establecerse en 0 (cero), de lo contrario, no se debe usar. Está presente para futuras funcionalidades.

*InfoLevel*

Debe establecerse en 0 (cero), de lo contrario, no se debe usar. Está presente para futuras funcionalidades.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>CbMax <em>no</em> es 0 (cero) o <em>InfoLevel</em> no es 0 (cero).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está actualmente en un registro y, como resultado, no se puede devolver información sobre un registro lógico.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errWriteConflict</p> | <p>Otra sesión ha actualizado el registro actual del cursor y una actualización de este registro por parte de esta sesión provocará un conflicto de escritura.</p> | 



Si se ejecuta correctamente, esta operación no tiene ningún efecto en la ubicación del cursor, pero solo indica que ninguna otra sesión ha actualizado actualmente este registro.

En caso de error, si se devuelve un código de error negativo, no hay ningún efecto en el cursor o la base de datos.

#### <a name="remarks"></a>Observaciones

Esta operación no afecta al estado del cursor ni de los datos. Solo devuelve un código de error que describe si se sabe que una actualización del registro actual por parte de la sesión que realiza la llamada da lugar a un JET_errWriteConflict o si se desconoce si se devuelve JET_errWriteConflict. Si otra sesión ya ha actualizado este registro para usarlo, es seguro que una actualización de este registro por esta sesión dará lugar a un conflicto de escritura. Esto será así hasta que esta sesión confirme o revierte sus transacciones al nivel de transacción 0 (cero). Sin embargo, si **JetGetCursorInfo** devuelve JET_errSuccess, es posible que otra sesión actualice este registro antes de la sesión actual y, por tanto, sigue siendo posible que una actualización del registro actual por parte de esta sesión en su transacción actual proscriba un conflicto de escritura.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
