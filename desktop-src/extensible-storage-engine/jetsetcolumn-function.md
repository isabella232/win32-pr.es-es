---
description: 'Más información sobre: JetSetColumn (Función)'
title: Función JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8517a70f8dd5de95bd9c16782759339b22ff4130
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359072"
---
# <a name="jetsetcolumn-function"></a>Función JetSetColumn


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetcolumn-function"></a>Función JetSetColumn

La **función JetSetColumn** modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual. Puede sobrescribir un valor existente, agregar un nuevo valor a una secuencia de valores de una columna con varios valores, quitar un valor de una secuencia de valores de una columna de varios valores o actualizar todo o parte de un valor largo, una columna de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*columnid*

El [JET_COLUMNID](./jet-columnid.md) de la columna que se va a recuperar. Como alternativa, se puede especificar un valor de *columnid* de 0 (cero). Cuando *se da columnid* 0 (cero), todas las columnas etiquetadas, columnas dispersas y con varios valores, se tratan como una sola columna. Esto facilita la recuperación de todas las columnas dispersas que están presentes en un registro.

*pvData*

Búfer de entrada que contiene los datos que se usarán para el valor de columna.

*cbData*

Tamaño en bytes del búfer de entrada.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Esta opción se usa para anexar datos a una columna de <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. El mismo comportamiento se puede lograr determinando el tamaño del valor long existente y especificando <em>ibLongValue</em> en <em>psetinfo</em>. Sin embargo, es más sencillo usar este <em>grbit,</em> ya que no es necesario conocer el tamaño del valor de columna existente.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Esta opción se usa para reemplazar el valor long existente por los datos recién proporcionados. Cuando se usa esta opción, es como si el valor long existente se hubiera establecido en 0 (cero) longitud antes de establecer los nuevos datos.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Esta opción solo es aplicable a las columnas etiquetadas, dispersas o con varios valores. Hace que la columna devuelva el valor de columna predeterminado en las operaciones de recuperación de columnas posteriores. Se quitan todos los valores de columna existentes.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Esta opción se usa para forzar que un valor largo, las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, se almacenen por separado del resto de datos de registro. Esto sucede normalmente cuando el tamaño del valor largo impide que se almacene con los datos de registro restantes. Sin embargo, esta opción se puede usar para forzar que el valor long se almacene por separado. Tenga en cuenta que no se puede forzar la separación de los valores largos de cuatro bytes de tamaño menor. En tales casos, se omite la opción .</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Esta opción se usa para interpretar el búfer de entrada como un número entero de bytes para establecer como la longitud del valor largo descrito por el <em>columnid</em> especificado y, si se proporciona, el número de secuencia en psetinfo- &gt; itagSequence. Si el tamaño especificado es mayor que el valor de columna existente, la columna se ampliará con 0s. Si el tamaño es menor que el valor de columna existente, el valor se truncará.</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Esta opción se usa para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara los datos de la columna de origen, sin ninguna transformación, con otros valores de columna existentes y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Esta opción se usa para exigir que todos los valores de una columna con varios valores sean distintos. Esta opción compara la transformación normalizada de clave de los datos de columna con otros valores de columna existentes transformados de forma similar y se devuelve un error si se encuentra un duplicado. Si se proporciona esta opción, JET_bitSetAppendLV, JET_bitSetOverwriteLV y JET_bitSetSizeLV también se pueden proporcionar.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Esta opción se usa para establecer un valor en longitud cero. Normalmente, un valor de columna se establece <strong>en NULL</strong> pasando cbMax de 0 (cero). Sin embargo, para algunos tipos, <a href="gg269213(v=exchg.10).md">como JET_coltypText</a>, un valor de columna puede tener una longitud de <strong></strong> 0 (cero) en lugar de <strong>NULL</strong>y esta opción se usa para diferenciar entre null y 0 (cero) longitud.</p><p><strong>Nota</strong>  En general, si la columna es una columna de longitud fija, este bit se omite y la columna se establece en <strong>NULL.</strong> Sin embargo, si la columna es una columna etiquetada de longitud fija, la longitud de la columna se establece en 0. Cuando la columna etiquetada de longitud fija se establece en 0 longitud, los intentos de recuperar la columna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> se realizarán correctamente, pero la longitud real que se devuelve en el <em>parámetro cbActual</em> es 0.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Esta opción se usa para almacenar todo el valor largo en el registro.</p> | 
| <p>JET_bitSetCompressed</p> | <p>Esta opción se usa para intentar la compresión de datos al almacenar los datos.</p><p><strong>Windows 7:</strong>  JET_bitSetCompressed se introdujo en Windows 7.</p> | 
| <p>JET_bitSetUncompressed</p> | <p>Esta opción se usa para no intentar la compresión al almacenar los datos.</p><p><strong>Windows 7:</strong>  JET_bitSetUnCompressed se introdujo en Windows 7.</p> | 



*psetinfo*

Puntero a parámetros de entrada opcionales que se pueden establecer para esta función mediante la [JET_SETINFO](./jet-setinfo-structure.md) estructura.

Si *psetinfo* se especifica como **NULL,** la función se comporta como si se hubieran dado una *itagSequence* de 1 y *un valor ibLongValue* de 0 (cero). Esto hace que el conjunto de columnas establezca el primer valor de una columna con varios valores y que establezca datos largos a partir del desplazamiento 0 (cero).

Se pueden establecer las siguientes opciones para este parámetro:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Desplazamiento binario en un valor de columna largo donde deben comenzar los datos establecidos.</p> | 
| <p>itagSequence</p> | <p>Número de secuencia del valor de columna multivalor deseado que se establecerá. Si <em>itagSequence</em> se establece en 0 (cero), el valor proporcionado se debe anexar al final de la secuencia de valores multivalor. Si el número de secuencia proporcionado es mayor que el último valor multivalor existente, se anexa de nuevo el valor especificado al final de la secuencia de valores. Si el número de secuencia corresponde a un valor existente, ese valor se reemplaza por el valor especificado.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBadColumnId</p> | <p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el <em>columnid</em> dado no existe en la tabla.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Se intentó actualizar un valor largo durante una operación de actualización original de eliminación de copia de inserción.</p> | 
| <p>JET_errColumnTooBig</p> | <p>Los datos de valor de columna especificados en el búfer de entrada superan la limitación de tamaño natural para una columna de longitud fija o están configurados para columnas binarias o de texto de longitud fija. Este error también se devuelve cuando se pasan más de 1024 bytes de datos para una columna larga y se establece JET_bitSetIntrinsicLV marca.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>El tamaño de datos del valor de columna especificado no coincide con lo que es natural para el tipo de datos de longitud fija.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Se intentó actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien actualizar una columna de versión durante una operación de reemplazo.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Las opciones proporcionadas son desconocidas o son una combinación no conocida de la configuración de bits conocida.</p> | 
| <p>JET_errInvalidParameter</p> | <p>El valor psetinfo- &gt; cbStruct especificado no es un tamaño válido para la <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> estructura.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>La operación de establecer columna intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Se realizó un intento no válido de actualizar un valor de columna largo cuando la sesión de llamada no estaba en una transacción.</p> | 
| <p>JET_errNullInvalid</p> | <p>Se intentó establecer una columna que no es<strong>NULL</strong> en <strong>NULL.</strong></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Igual que JET_errNullInvalid.</p> | 
| <p>JET_errRecordTooBig</p> | <p>No se pudo establecer el valor de columna en el valor del búfer de entrada porque habría provocado que el registro superara su limitación de tamaño de página relacionada. Las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongBinary</a> pueden almacenarse por separado de los datos de registro restantes. Sin embargo, otras columnas deben almacenarse con el registro y pueden hacer que se supere la limitación de tamaño del registro. Incluso las columnas largas requieren 5 bytes de espacio dentro del registro como vinculación y esto también puede provocar que JET_errRecordTooBig se devuelvan.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>El cursor no está actualmente en proceso de insertar un nuevo registro o de actualizar uno existente.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>El valor de columna en el búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se trunó.</p> | 



Si se ejecuta correctamente, la parte deseada de un valor de columna para la columna especificada se establece con los datos copiados del búfer de entrada. Es posible que el conjunto de datos se haya truncado si superó la longitud máxima especificada para una columna de longitud variable.

En caso de error, la ubicación del cursor se deja sin cambios y no se actualizan datos de valores de columna en el búfer de copia.

#### <a name="remarks"></a>Observaciones

Establecer valores largos, valores para columnas [JET_coltypLongBinary](./jet-coltyp.md) de tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), solo debe realizarse cuando la sesión de llamada está en una transacción. Si la sesión de llamada no está en una transacción, las modificaciones en los valores largos que se almacenan por separado pueden estar totalmente confirmadas incluso cuando la operación de actualización se cancele más adelante. Si la sesión de llamada está en una transacción, los efectos de la actualización se pueden revertir completamente cancelando la actualización y revierte la transacción de sesión.

Las actualizaciones de índice no se realizan como resultado de **las operaciones de JetSetColumn.** En su lugar, los índices solo se actualizan una vez completadas todas las modificaciones de columna y se [llama a JetUpdate.](./jetupdate-function.md) Esto permite la actualización más eficaz de los índices cuando los índices implican la modificación de más de una columna.

Un registro tiene un tamaño limitado en función del tamaño de página de la base de datos. Los valores long del registro de más de cinco bytes se almacenarán independientes del registro si los datos del registro superan su límite como resultado de una **operación JetSetColumn.** El error JET_errRecordTooBig solo se devolverá después de que todos los datos de la columna de registro separable se hayan almacenado por separado del registro y el registro supere el límite de tamaño del registro.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
