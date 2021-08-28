---
description: 'Más información sobre: JetSetColumns (Función)'
title: Función JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a62c3fee0b961268c11974e0a6064f091474d34
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984348"
---
# <a name="jetsetcolumns-function"></a>Función JetSetColumns


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetcolumns-function"></a>Función JetSetColumns

La **función JetSetColumns** tiene un comportamiento similar al de [JetSetColumn,](./jetsetcolumn-function.md) pero permite a una aplicación establecer varios valores de columna en una sola operación. Se usa una [matriz](./jet-setcolumn-structure.md) de JET_SETCOLUMN estructura para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada para cada valor de columna que se va a establecer.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*psetcolumn*

Puntero a una matriz de una o varias [JET_SETCOLUMN](./jet-setcolumn-structure.md) estructura. Cada estructura incluye descripciones de qué valor de columna se va a establecer y de dónde obtener los datos de columna que se establecerán.

*csetcolumn*

Número de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) en la matriz especificada por *psetcolumn*.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errBadColumnId</p> | <p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Igual que JET_errNullInvalid.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el <em>columnid</em> dado no existe en la tabla.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Se intentó actualizar un valor largo durante una operación de actualización original de eliminación de copia de inserción.</p> | 
| <p>JET_errColumnTooBig</p> | <p>Los datos de valor de columna especificados en el búfer de entrada superan la limitación de tamaño natural para una columna de longitud fija o están configurados para columnas binarias o de texto de longitud fija. Este error también se devuelve cuando se pasan más de 1024 bytes de datos para una columna larga y se establece la marca JET_bitSetIntrinsicLV datos.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>El tamaño de datos del valor de columna especificado no coincide con lo que es natural para el tipo de datos de longitud fija.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Se intentó actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien actualizar una columna de versión durante una operación de reemplazo.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Las opciones proporcionadas son desconocidas o una combinación no conocida de la configuración de bits conocida.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El psetinfo- &gt; cbStruct especificado no es un tamaño válido para la <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> estructura.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>La operación set column intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Se intentó actualizar un valor de columna largo cuando la sesión de llamada no estaba en una transacción.</p> | 
| <p>JET_errNullInvalid</p> | <p>Se intentó establecer una columna que no es NULL en NULL.</p> | 
| <p>JET_errRecordTooBig</p> | <p>El valor de columna no se pudo establecer en el valor del búfer de entrada porque habría hecho que el registro superara su limitación de tamaño de página relacionada. Las columnas de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse por separado de los datos de registro restantes. Sin embargo, otras columnas deben almacenarse con el registro y pueden hacer que se supere la limitación de tamaño del registro. Incluso las columnas largas requieren 5 bytes de espacio dentro del registro como vinculación y esto también puede provocar que JET_errRecordTooBig se devuelvan.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>El cursor no está actualmente en proceso de insertar un nuevo registro o de actualizar uno existente.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>El valor de columna del búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</p> | 



Si se ejecuta correctamente, para cada columna descrita en las psetcolumns, la parte deseada del valor de columna se establece con los datos copiados del búfer de entrada. Es posible que el conjunto de datos de columna se haya truncado si superó la longitud máxima especificada para una columna de longitud variable.

En caso de error, la ubicación del cursor se deja sin cambios y no se actualizan datos de valor de columna en el búfer de copia.

#### <a name="remarks"></a>Observaciones

Si alguna operación de establecer columna individual devuelve un error, toda la **operación JetSetColumns** devolverá un error. Las advertencias, en general, se devuelven en el error psetcolumns- y no en \> el código de retorno de esta función. Sin embargo, si el último conjunto de columnas tiene una advertencia, esta advertencia se devolverá desde **el propio JetSetColumns.**

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
