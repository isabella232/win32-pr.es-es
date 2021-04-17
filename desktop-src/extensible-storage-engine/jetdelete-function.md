---
description: 'Más información acerca de: JetDelete (función)'
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
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648537"
---
# <a name="jetdelete-function"></a>Función JetDelete


_**Se aplica a:** Windows | Windows Server_

## <a name="jetdelete-function"></a>Función JetDelete

La función **JetDelete** elimina el registro actual de una tabla de base de datos.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada de API.

*TABLEID*

Cursor en una tabla de base de datos. Se eliminará la fila actual.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>Error en la función de devolución de llamada. Por ejemplo, las infracciones de acceso de las funciones de devolución de llamada se detectan y traducen en JET_errCallbackFailed. Este error solo lo devolverá Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>El cursor especificado por <em>TABLEID</em> no admite la eliminación. Consulte la sección Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor especificado por <em>TABLEID</em> no está en un registro.</p></td>
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
<td><p>JET_errPermissionDenied</p></td>
<td><p>El motor de base de datos no tiene permisos suficientes para eliminar el registro. Esto puede ocurrir si el archivo de base de datos se abrió con acceso de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Existe un búfer de actualización (vea <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>), pero no todos los cambios realizados en las columnas de tipo JET_coltypLongText y/o las columnas de tipo JET_coltypLongBinary se pueden revertir.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No es válido utilizar la misma sesión desde más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transacción es una transacción de solo lectura y no admite eliminaciones.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no hay suficiente memoria para conservar la información transaccional acerca de la actualización.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Otra sesión ha bloqueado previamente el registro para su actualización. Se producirá un error en la actualización intentada por esta sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la moneda se deja justo antes del Registro siguiente. Si el registro eliminado fue el último de la tabla, la moneda se deja al final de la tabla (es decir, después del último registro). Si el registro eliminado era el único registro de la tabla, la moneda se establece en el principio.

Los índices adecuados se actualizan automáticamente.

Si se prepara una actualización (mediante [JetPrepareUpdate](./jetprepareupdate-function.md)), se cancelará. Se restablecerá el búfer de actualización.

En caso de error, la moneda permanece inalterada. Si se prepara una actualización (consulte [JetPrepareUpdate](./jetprepareupdate-function.md)), se puede restablecer el búfer de actualización.

#### <a name="remarks"></a>Observaciones

No todas las tablas admiten la eliminación de filas. Normalmente, una tabla temporal no admite la eliminación de filas. La eliminación de registros puede estar habilitada en tablas temporales por muchas razones, algunas de las cuales son:

  - Se especificó JET_bitTTUpdatable durante la creación.

  - Las tablas temporales grandes pueden admitir la eliminación si se crearon con JET_bitTTScrollable o JET_bitTTIndexed. El umbral en el que una tabla temporal se convierte en "grande" es actualmente de 64 kilobytes, pero se puede cambiar en futuras versiones.

Windows XP y versiones posteriores. Las funciones de devolución de llamada se pueden invocar mediante **JetDelete**, incluidos JET_cbtypBeforeDelete y JET_cbtypAfterDelete.

Es importante entender el impacto de realizar un gran número de operaciones de actualización dentro de una única transacción. El motor de base de datos debe realizar el seguimiento de cada actualización de la base de datos en el almacén de versiones. El almacén de versiones contiene un registro en directo de todas las versiones de cada entrada de registro o índice de la base de datos que pueden verse en todas las transacciones activas. Estas versiones se utilizan para admitir el control de simultaneidad con varias versiones que usa el motor de base de datos para admitir transacciones que usan el aislamiento de instantánea. Una vez que el motor de base de datos haya agotado los recursos usados para almacenar estas versiones, ya no podrá aceptar más cambios hasta que algunas transacciones hayan concluido para permitir la recuperación de estos recursos. Cuando el motor está en este estado, se producirá un error en todas las actualizaciones con JET_errVersionStoreOutOfMemory. Los recursos disponibles para el motor de base de datos para almacenar estas versiones se pueden controlar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxVerPages* y *JET_paramGlobalMinVerPages*.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
