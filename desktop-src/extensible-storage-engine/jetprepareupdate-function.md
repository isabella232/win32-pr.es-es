---
description: 'Más información acerca de: JetPrepareUpdate (función)'
title: JetPrepareUpdate función)
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
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649277"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate función)

La función **JetPrepareUpdate** es la primera operación de realizar una actualización, con el fin de insertar un nuevo registro o reemplazar un registro existente con nuevos valores. Las actualizaciones se realizan llamando a **JetPrepareUpdate**, llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) cero o más veces y finalmente llamando a [JetUpdate](./jetupdate-function.md) para completar la operación. **JetPrepareUpdate** y [JetUpdate](./jetupdate-function.md) establecen los límites para una operación de actualización y son importantes para tener solo el estado de actualización final de un registro escrito en los índices. Esto es más eficaz, pero también es necesario en los casos en los que los datos deben coincidir con un estado válido a través de más de en la operación de establecer columna.

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

*TABLEID*

Cursor que se va a usar para esta llamada.

*porcentaje*

Las opciones que se pueden usar para preparar una actualización, que incluyen lo siguiente.

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
<td><p>JET_prepCancel</p></td>
<td><p>Esta marca hace que <strong>JetPrepareUpdate</strong> cancele la actualización de este cursor.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsert</p></td>
<td><p>Esta marca hace que el cursor se prepare para una inserción de un nuevo registro. Todos los datos se inicializan en el estado predeterminado del registro. Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza en última instancia, si se produce un error o se cancela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepInsertCopy</p></td>
<td><p>Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente. Debe haber un registro actual si se usa esta opción. El estado inicial del nuevo registro se copia del registro actual. Los valores Long que se almacenan fuera de registro se copian de manera virtual.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsertCopyDeleteOriginal</p></td>
<td><p>Esta marca hace que el cursor se prepare para una inserción del mismo registro, y una eliminación o el registro original. Se utiliza en casos en los que la clave principal ha cambiado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepReplace</p></td>
<td><p>Esta marca hace que el cursor se prepare para un reemplazo del registro actual. Si la tabla tiene una columna de versión, la columna versión se establece en el valor siguiente en su secuencia. Si esta actualización no se completa, el valor de versión del registro no se verá afectado. Se realiza un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_prepReplaceNoLock</p></td>
<td><p>Esta marca es similar a JET_prepReplace, pero no se realiza ningún bloqueo para evitar que otras sesiones actualicen este registro. En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a <a href="gg269288(v=exchg.10).md">JetUpdate</a> para completar la actualización.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>Se llamó a <strong>JetPrepareUpdate</strong> con una marca válida para Prep pero no JET_prepCancel y el cursor ya estaba en el estado preparado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>La marca de preparación especificada no es una marca válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Se llamó a <strong>JetPrepareUpdate</strong> para reemplazar un registro que tenía columnas SLV. Columnas SLV. Tenga en cuenta que las columnas de SLV son una característica no diseñada para el uso general. Esta característica se usa para admitir la infraestructura de Microsoft Exchange y no está pensada para usarse en la aplicación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError</p></td>
<td><p>Se llamó a <strong>JetPrepareUpdate</strong> con JET_prepCancel pero no se pudieron revertir todos los cambios realizados en las columnas de tipo JET_coltypLongText y/o las columnas de tipo JET_coltypLongBinary.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Esta marca no se puede usar con la misma sesión desde más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Se llamó a <strong>JetPrepareUpdate</strong> con JET_prepCancel pero el cursor no estaba en el estado preparado.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, el cursor cambia al estado preparado para el propósito de la actualización deseada, o en el caso de JET_prepCancel, el cursor se revierte al estado no preparado y se descartan los cambios.

En caso de error, el estado del cursor se deja sin modificar. Si el error se JET_errRollbackError, el estado del cursor cambia al estado no preparado pero no se han revertido todos los cambios.

#### <a name="remarks"></a>Observaciones

Insertar una copia de un registro es una optimización importante cuando los registros comparten datos de tipo JET_coltypLongText o JET_coltypLongBinary. Estos datos se almacenan de forma no grabada cuando son grandes y es posible que varios registros compartan la misma representación física de los datos. En este caso, los datos se pueden actualizar desde cualquier registro, pero si lo hace, se producirán ráfagas de datos de modo que cada registro tenga su propia copia. No es posible cambiar los datos en un registro mediante una modificación de otro registro. Además, no es posible bloquear una actualización de un registro mediante una actualización de otro registro. Se trata de una característica central de ESE y se conoce como bloqueo de nivel de registro.

Las operaciones de [JetUpdate](./jetupdate-function.md) que producen un error dejan el cursor en el estado de la preparación de la actualización. Esto es para permitir la corrección de algunos errores, como un valor de columna incorrecto, sin necesidad de volver a crear el estado de actualización. Esto significa que, en todos los casos en los que un cursor abandone una actualización, debe llamar explícitamente a **JetPrepareUpdate** con JET_prepCancel.

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
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
