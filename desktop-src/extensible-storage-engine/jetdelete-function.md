---
description: 'Más información sobre: JetDelete (Función)'
title: Función JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 039ddcb0610b6a958e9c45be7e3a898631d2a0fc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984958"
---
# <a name="jetdelete-function"></a>Función JetDelete


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdelete-function"></a>Función JetDelete

La **función JetDelete** elimina el registro actual en una tabla de base de datos.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Cursor de una tabla de base de datos. Se eliminará la fila actual.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errCallbackFailed</p> | <p>Error de la función de devolución de llamada de alguna manera. Por ejemplo, las infracciones de acceso en las funciones de devolución de llamada se detectan y se traducen a JET_errCallbackFailed. Este error solo lo devolverá el Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIllegalOperation</p> | <p>El cursor especificado por <em>tableid</em> no admite la eliminación. Consulte la sección Comentarios.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor especificado por <em>tableid</em> no está en un registro.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errPermissionDenied</p> | <p>El motor de base de datos no tiene permisos suficientes para eliminar el registro. Esto puede ocurrir si el archivo de base de datos se abrió con acceso de solo lectura.</p> | 
| <p>JET_errRollbackError</p> | <p>Existe un búfer de actualización (consulte <a href="gg269339(v=exchg.10).md">JetPrepareUpdate),</a>pero no todos los cambios realizados en columnas de tipo JET_coltypLongText o columnas de tipo JET_coltypLongBinary se podrían revertir.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No es posible usar la misma sesión desde más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transacción es una transacción de solo lectura y no admite eliminaciones.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Error en la operación porque no hay suficiente memoria para conservar la información transaccional sobre la actualización.</p> | 
| <p>JET_errWriteConflict</p> | <p>Otra sesión ha bloqueado previamente el registro para la actualización. Se producirá un error en la actualización intentada por esta sesión.</p> | 



Si se ejecuta correctamente, la moneda se deja justo antes del siguiente registro. Si el registro eliminado fue el último de la tabla, la moneda se deja al final de la tabla (es decir, después del nuevo último registro). Si el registro eliminado era el único registro de la tabla, la moneda se establece en el principio.

Los índices adecuados se actualizan automáticamente.

Si se prepara una actualización [(mediante JetPrepareUpdate),](./jetprepareupdate-function.md)se cancelará. Se restablecerá el búfer de actualización.

En caso de error, la moneda permanece sin cambios. Si se prepara una actualización (consulte [JetPrepareUpdate),](./jetprepareupdate-function.md)se puede restablecer el búfer de actualización.

#### <a name="remarks"></a>Observaciones

No todas las tablas admiten la eliminación de filas. Normalmente, una tabla temporal no admite la eliminación de filas. La eliminación de registros puede habilitarse en tablas temporales por muchas razones, algunas de las cuales son:

  - JET_bitTTUpdatable se especificó durante la creación.

  - Las tablas temporales de gran tamaño pueden admitir la eliminación si se crearon JET_bitTTScrollable o JET_bitTTIndexed. El umbral en el que una tabla temporal se convierte en "grande" es actualmente de 64 kilobytes, pero puede cambiarse en versiones futuras.

Windows XP y versiones posteriores. JetDelete puede invocar funciones de devolución de llamada, incluidas JET_cbtypBeforeDelete y JET_cbtypAfterDelete.

Es importante comprender el impacto de realizar un gran número de operaciones de actualización dentro de una única transacción. El motor de base de datos debe realizar el seguimiento de cada actualización de la base de datos en el almacén de versiones. El almacén de versiones contiene un registro activo de todas las distintas versiones de cada entrada de registro o índice de la base de datos que pueden ver todas las transacciones activas. Estas versiones se usan para admitir el control de simultaneidad con varias versiones en uso por parte del motor de base de datos para admitir transacciones mediante el aislamiento de instantáneas. Una vez que el motor de base de datos ha agotado los recursos usados para almacenar estas versiones, ya no puede aceptar más cambios hasta que algunas transacciones se han cerrado para permitir que se reclamen estos recursos. Cuando el motor está en este estado, se producirá un error en todas las actualizaciones JET_errVersionStoreOutOfMemory. Los recursos disponibles para el motor de base de datos para almacenar estas versiones se pueden controlar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) *con* JET_paramMaxVerPages y *JET_paramGlobalMinVerPages*.

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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
