---
description: 'Más información sobre: JetUpdate2 (Función)'
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
ms.openlocfilehash: 34cc43aea463c186d68c0fa0cadc447ba2a02acb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983257"
---
# <a name="jetupdate2-function"></a>Función JetUpdate2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetupdate2-function"></a>Función JetUpdate2

La **función JetUpdate2** realiza una operación de actualización, incluida la inserción de una nueva fila en una tabla o la actualización de una fila existente. Esta función contiene una lista de opciones *de bits grbit* que se pueden establecer al realizar una actualización. La eliminación de una fila de tabla se realiza mediante una [llamada a JetDelete](./jetdelete-function.md).

**Windows Server 2003: JetUpdate2** se introdujo en Windows Server 2003.

**JetUpdate2** es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a [JetPrepareUpdate](./jetprepareupdate-function.md) y, a continuación, llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o varias veces para establecer el estado del registro. Por último, **se llama a JetUpdate2** para completar la operación de actualización. Los índices solo se actualizan [mediante JetUpdate](./jetupdate-function.md) o **JetUpdate2** y no durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns.](./jetsetcolumns-function.md)

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

*tableid*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Puntero a un marcador devuelto para una fila insertada.

*cbBookmark*

Tamaño del búfer al que apunta *pvBookmark*.

*actual*

Tamaño devuelto del marcador para la fila insertada devuelta en *pvBookmark*.

*grbit*

Grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitUpdateCheckESE97Compatibility</p> | <p>Esta marca hace que la actualización devuelva un error si la actualización no hubiera sido posible en la versión Windows 2000 de ESE, que aplicaba un número máximo menor de instancias de columna multivalor en cada registro que las versiones posteriores de ESE. Esto es importante solo para las aplicaciones que desean replicar datos entre aplicaciones hospedadas en Windows 2000 y aplicaciones hospedadas en Windows Server 2003 o versiones posteriores de ESE. No debe ser necesario para la mayoría de las aplicaciones.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>El búfer dado para el marcador de registros no es lo suficientemente grande como para almacenar el marcador de registro.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errDiskFull</p> | <p>La operación de actualización requiere el crecimiento del archivo de base de datos o la asignación de archivos de registro, pero la unidad de disco donde reside el archivo de base de datos o la serie de registros está llena. Como alternativa, el archivo de base de datos está en un volumen con formato FAT32 y el archivo de base de datos ya es de 4 GB, el límite por archivo para FAT32.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El parámetro <em>de preparación</em> especificado en la <a href="gg269339(v=exchg.10).md">función JetPrepareUpdate</a> no es una marca válida.</p> | 
| <p>JET_errKeyDuplicate</p> | <p>Una clave de índice para este registro es un duplicado de otra clave de índice para otro registro que ya está en la tabla y el índice no permite duplicados.</p> | 
| <p>JET_errKeyTruncated</p> | <p>El registro insertado o actualizado tiene uno o varios índices para los que la clave generada habría superado el tamaño máximo permitido. Como resultado, la operación no pudo evitar el truncamiento de claves.</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>El registro insertado o actualizado tiene una columna de varios valores indizada con dos o más valores idénticos dentro del tamaño de clave de longitud máxima establecido para el índice. Como resultado, el registro tiene dos entradas idénticas en el índice que no son válidas.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNullInvalid</p> | <p>Una o varias columnas del registro que se va a insertar o en el estado actualizado de un registro que se va a reemplazar es <strong>NULL,</strong> lo que infringe la restricción definida para esas columnas.</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>Uno o varios índices se definen para no permitir una clave <strong>NULL</strong> y el estado insertado o actualizado de un registro que se va a reemplazar infringe esta restricción definida.</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>Una operación de reemplazo de registros ha actualizado la clave principal. Las actualizaciones de las columnas de clave principal deben realizarse mediante la eliminación del registro existente y la inserción de un nuevo registro con los datos deseados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><a href="gg269339(v=exchg.10).md">Se llamó a JetPrepareUpdate</a> con JET_prepCancel pero el cursor no estaba en estado preparado.</p> | 
| <p>JET_errWriteConflict</p> | <p>Una operación de reemplazo de registros para la que aún no se ha asignado un bloqueo de escritura puede encontrar un conflicto de escritura en el momento de la actualización.</p> | 



Si se ejecuta correctamente, se completa la operación de actualización abierta en el cursor. Si se define una columna de incremento automático para la tabla, este valor se establece para los registros insertados. Si se define una columna de versión para la tabla, su valor se inicializa para los registros recién insertados o se incrementa cada vez que se reemplaza un registro. Se actualizan todos los índices, incluidos los índices agrupados y no agrupados.

En caso de error, no se realiza ningún cambio de ningún tipo en la base de datos. Es posible que se haya llamado a las funciones de devolución de llamada antes de insertar y antes de reemplazar, pero después de insertar y después de reemplazar las devoluciones de llamada no se habrán llamado, ya que esta última no puede provocar un error en una actualización. El búfer de copia de cursor se deja en su estado preparado, por lo que existe la oportunidad de corregir incrementalmente los problemas que provocaron errores y reintentar la operación de actualización.

#### <a name="remarks"></a>Observaciones

[JetSetColumn](./jetsetcolumn-function.md)aplica las limitaciones de tamaño del registro y no, en general, [JetUpdate](./jetupdate-function.md). La única excepción es cuando se JET_bitUpdateCheckESE97Compatibility marca de compatibilidad. En este caso, se comprueba todo el registro, ya que una operación [Individual JetSetColumn](./jetsetcolumn-function.md) que superó el límite puede compensarse con una llamada subsiguiente a [JetSetColumn](./jetsetcolumn-function.md).

Consulte la sección Comentarios de [JetUpdate](./jetupdate-function.md) para obtener más información.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



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
