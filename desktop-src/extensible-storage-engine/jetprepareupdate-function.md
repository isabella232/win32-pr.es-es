---
description: 'Más información sobre: JetPrepareUpdate (Función)'
title: JetPrepareUpdate (Función)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af1f14d3588077ebc293ab35aeb143cc99b8e440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882700"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate (Función)

La **función JetPrepareUpdate** es la primera operación para realizar una actualización, con el fin de insertar un nuevo registro o reemplazar un registro existente por nuevos valores. Las actualizaciones se realizan llamando a **JetPrepareUpdate,** llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) cero o más veces y, por último, llamando a [JetUpdate](./jetupdate-function.md) para completar la operación. **JetPrepareUpdate** y [JetUpdate](./jetupdate-function.md) establecen los límites de una operación de actualización y son importantes para tener solo el estado de actualización final de un registro especificado en índices. Esto es más eficaz, pero también necesario en los casos en los que los datos deben coincidir con un estado válido a través de más que en la operación de establecer columna.

Hay algunas opciones diferentes para insertar o reemplazar registros y se describen con más detalle a continuación.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*Preparación*

Las opciones que se pueden usar para prepararse para una actualización, que incluyen lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_prepCancel</p> | <p>Esta marca hace <strong>que JetPrepareUpdate</strong> cancele la actualización de este cursor.</p> | 
| <p>JET_prepInsert</p> | <p>Esta marca hace que el cursor se prepare para una inserción de un nuevo registro. Todos los datos se inicializan en el estado predeterminado del registro. Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza correctamente, se produce un error o se cancela.</p> | 
| <p>JET_prepInsertCopy</p> | <p>Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente. Debe haber un registro actual si se usa esta opción. El estado inicial del nuevo registro se copia del registro actual. Los valores largos que se almacenan fuera de registro se copian virtualmente.</p> | 
| <p>JET_prepInsertCopyDeleteOriginal</p> | <p>Esta marca hace que el cursor se prepare para una inserción del mismo registro y una eliminación o el registro original. Se usa en casos en los que la clave principal ha cambiado.</p> | 
| <p>JET_prepReplace</p> | <p>Esta marca hace que el cursor se prepare para reemplazar el registro actual. Si la tabla tiene una columna de versión, la columna de versión se establece en el siguiente valor de su secuencia. Si esta actualización no se completa, el valor de versión del registro no se verá afectado. Se toma un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</p> | 
| <p>JET_prepReplaceNoLock</p> | <p>Esta marca es similar a JET_prepReplace, pero no se toma ningún bloqueo para impedir que otras sesiones actualicen este registro. En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a <a href="gg269288(v=exchg.10).md">JetUpdate</a> para completar la actualización.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores ese, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p><strong>Se llamó a JetPrepareUpdate</strong> con una marca válida para la preparación, pero no JET_prepCancel y el cursor ya estaba en estado preparado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La marca de preparación dada no es una marca válida.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p><strong>Se llamó a JetPrepareUpdate</strong> para reemplazar un registro que tenía columnas SLV. Columnas SLV. Tenga en cuenta que las columnas SLV son una característica que no está pensada para uso general. Esta característica se usa para admitir la infraestructura Exchange Microsoft y no está pensada para usarse en la aplicación.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRollbackError</p> | <p><strong>Se llamó a JetPrepareUpdate</strong> con JET_prepCancel pero no se pudieron revertir todos los cambios realizados en columnas de tipo JET_coltypLongText o columnas de tipo JET_coltypLongBinary.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Esta marca no se puede usar con la misma sesión de más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><strong>Se llamó a JetPrepareUpdate</strong> con JET_prepCancel pero el cursor no estaba en estado preparado.</p> | 



Si el cursor se ejecuta correctamente, se cambia al estado preparado para la actualización deseada o, en el caso de JET_prepCancel, el cursor se revierte al estado no preparado y se descartan los cambios.

En caso de error, el estado del cursor se deja sin modificar. Si el error se JET_errRollbackError, el estado del cursor cambia al estado no preparado, pero no todos los cambios se han revertido.

#### <a name="remarks"></a>Observaciones

Insertar una copia de un registro es una optimización importante cuando los registros comparten datos de tipo JET_coltypLongText o JET_coltypLongBinary. Estos datos se almacenan sin registro cuando son grandes y es posible que varios registros compartan la misma representación física de los datos. En este caso, los datos se pueden actualizar desde cualquier registro, pero si lo hace, los datos se ráfagarán de forma que cada registro tenga su propia copia. No es posible cambiar los datos de un registro mediante una modificación de otro registro. Además, no es posible bloquear una actualización de un registro mediante una actualización de otro registro. Esta es una característica central de ESE y se conoce como bloqueo de nivel de registro.

[Las operaciones JetUpdate](./jetupdate-function.md) que no se pueden realizar dejan el cursor en estado preparado para la actualización. Esto es para permitir la corrección de algunos errores, como un valor de columna incorrecto, sin necesidad de volver a crear el estado de actualización. Esto significa que, en todos los casos en los que un cursor abandona una actualización, debe llamar explícitamente a **JetPrepareUpdate** con JET_prepCancel.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
