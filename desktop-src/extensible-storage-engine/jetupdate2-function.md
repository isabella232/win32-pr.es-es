---
description: 'Más información acerca de: JetUpdate2 (función)'
title: Función JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809007"
---
# <a name="jetupdate2-function"></a>Función JetUpdate2


_**Se aplica a:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>Función JetUpdate2

La función **JetUpdate2** realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. Esta función contiene una lista de opciones de *grbit* que se pueden establecer al realizar una actualización. La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete](./jetdelete-function.md).

**Windows server 2003: JetUpdate2** se incorporó en windows Server 2003.

**JetUpdate2** es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a [JetPrepareUpdate](./jetprepareupdate-function.md) y llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o varias veces para establecer el estado del registro. Por último, se llama a **JetUpdate2** para completar la operación de actualización. Los índices solo se actualizan mediante [JetUpdate](./jetupdate-function.md) o **JetUpdate2** y no durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Puntero a un marcador devuelto para una fila insertada.

*cbBookmark*

Tamaño del búfer al que apunta *pvBookmark*.

*pcbActual*

Tamaño devuelto del marcador de la fila insertada que se devuelve en *pvBookmark*.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.

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
<td><p>JET_bitUpdateCheckESE97Compatibility</p></td>
<td><p>Esta marca hace que la actualización devuelva un error si la actualización no hubiera sido posible en la versión de Windows 2000 de ESE, que aplicó un número máximo menor de instancias de columna multivalor en cada registro que en versiones posteriores de ESE. Esto solo es importante para las aplicaciones que desean replicar datos entre aplicaciones hospedadas en Windows 2000 y aplicaciones hospedadas en Windows Server 2003 o versiones posteriores de ESE. No debe ser necesario para la mayoría de las aplicaciones.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>El búfer especificado para el marcador de registro no es lo suficientemente grande como para almacenar el marcador de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>La operación de actualización requiere el crecimiento del archivo de base de datos o la asignación del archivo de registro, pero la unidad de disco donde reside el archivo de base de datos o la serie de registro está llena. Como alternativa, el archivo de base de datos se encuentra en un volumen con formato FAT32 y el archivo de base de datos ya está 4GBytes, el límite por archivo para FAT32.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>El parámetro <em>Prep</em> proporcionado en la función <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> no es una marca válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Una clave de índice para este registro es un duplicado de otra clave de índice para otro registro que ya está en la tabla y el índice no permite duplicados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated</p></td>
<td><p>El registro insertado o actualizado tiene uno o más índices para los que la clave generada habría superado el tamaño máximo permitido. Como resultado, la operación no ha podido evitar el truncamiento de claves.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>El registro insertado o actualizado tiene una columna de varios valores indizada con dos o más valores que son idénticos en el tamaño de la clave de longitud máxima establecido para el índice. Como resultado, el registro tiene dos entradas idénticas en el índice que no son válidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Una o más columnas del registro que se van a insertar o en el estado actualizado de un registro que se va a reemplazar es <strong>null</strong> , lo que infringe la restricción definida para esas columnas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Uno o más índices están definidos para no permitir una clave <strong>null</strong> y el estado insertado o actualizado de un registro que se está reemplazando infringe esta restricción definida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Una operación de reemplazo de registro ha actualizado la clave principal. Las actualizaciones de las columnas de clave principal se deben realizar a través de la eliminación del registro existente e inserción de un nuevo registro con los datos deseados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Se llamó a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> con JET_prepCancel pero el cursor no estaba en el estado preparado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>Una operación de reemplazo de registros para la que aún no se ha asignado un bloqueo de escritura puede producir un conflicto de escritura en el momento de la actualización.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se completa la operación de actualización abierta en el cursor. Si se define una columna de incremento automático para la tabla, este valor se establece para los registros insertados. Si se define una columna de versión para la tabla, su valor se inicializa para los registros recién insertados o se incrementa cada vez que se reemplaza un registro. Se actualizan todos los índices, incluidos los índices agrupados y no clúster.

En caso de error, no se realiza ningún cambio de ningún tipo en la base de datos. Antes de que se haya llamado a las funciones de devolución de llamada Insert y Before, no se habrá llamado a las devoluciones de llamada Insert y After Replace, ya que este último no puede hacer que se produzca un error en una actualización. El búfer de copia del cursor se deja en su estado preparado, por lo que existe la oportunidad de corregir incrementalmente los problemas que provocaron errores y volver a intentar la operación de actualización.

#### <a name="remarks"></a>Observaciones

Las limitaciones de tamaño de registro se aplican mediante [JetSetColumn](./jetsetcolumn-function.md)y no en general por [JetUpdate](./jetupdate-function.md). La única excepción es cuando se utiliza la marca de compatibilidad de JET_bitUpdateCheckESE97Compatibility. En este caso, se comprueba el registro completo, ya que una operación individual de [JetSetColumn](./jetsetcolumn-function.md) que superó el límite se puede compensar mediante una llamada subsiguiente a [JetSetColumn](./jetsetcolumn-function.md).

Vea la sección Comentarios en [JetUpdate](./jetupdate-function.md) para obtener más información.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
