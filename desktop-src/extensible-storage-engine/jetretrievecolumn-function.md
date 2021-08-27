---
description: 'Más información sobre: JetRetrieveColumn (Función)'
title: Función JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7457e747a0539965efe0fab9ebfd69660178a2ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480341"
---
# <a name="jetretrievecolumn-function"></a>Función JetRetrieveColumn


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetretrievecolumn-function"></a>Función JetRetrieveColumn

La **función JetRetrieveColumn** recupera un valor de columna única del registro actual. El registro es ese registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia de cursor. Esta función también puede recuperar datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de columna real, **JetRetrieveColumn** también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de columna para que los búferes de la aplicación se puedan dimensionar correctamente.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*columnid*

El [JET_COLUMNID](./jet-columnid.md) de la columna que se recuperará.

Se puede dar un valor de *columnid* de 0 (cero) que no hace referencia a ninguna columna individual. Cuando *se da columnid* 0 (cero), todas las columnas etiquetadas, dispersas y de varios valores se tratan como una sola columna. Esto facilita la recuperación de todas las columnas dispersas que están presentes en un registro.

*pvData*

Búfer de salida que recibe el valor de columna.

*cbData*

Tamaño máximo, en bytes, del búfer de salida.

*actual*

Recibe el tamaño real, en bytes, del valor de columna.

Si este parámetro es **NULL,** no se devolverá el tamaño real del valor de columna.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Esta marca hace que la columna retrieve recupere el valor modificado en lugar del valor original. Si el valor no se ha modificado, se recupera el valor original. De este modo, se puede recuperar un valor que aún no se ha insertado o actualizado durante el funcionamiento de la inserción o actualización de un registro.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Esta opción se usa para recuperar valores de columna del índice, si es posible, sin tener acceso al registro. De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice. En los casos en los que el valor de la columna original no se puede recuperar del índice, debido a transformaciones irreversibles o truncamiento de datos, se accederá al registro y se recuperarán los datos de la forma habitual. Se trata de una opción de rendimiento y solo se debe especificar cuando es probable que el valor de columna se pueda recuperar del índice. Esta opción no debe especificarse si el índice actual es el índice clúster, ya que las entradas de índice para el índice clúster o principal son los propios registros. Este bit no se puede establecer si JET_bitRetrieveFromPrimaryBookmark también está establecido.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Esta opción se usa para recuperar valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece tanto en el índice principal como en el índice actual. Esta opción no debe especificarse si el índice actual es el índice agrupado o principal. Este bit no se puede establecer si JET_bitRetrieveFromIndex también está establecido.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Esta opción se usa para recuperar el número de secuencia de un valor de columna multivalor en pretinfo- &gt; itagSequence. El campo itagSequence es normalmente una entrada para recuperar valores de columna multivalor de un registro. Sin embargo, al recuperar valores de un índice, también es posible asociar la entrada de índice a un número de secuencia determinado y recuperar también este número de secuencia. Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</p> | 
| <p>JET_bitRetrieveNull</p> | <p>Esta opción se usa para recuperar valores NULL de <strong>columna multivalor.</strong> Si no se especifica esta opción, los valores <strong>NULL</strong> de columna multivalor se omitirán automáticamente.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Esta opción solo afecta a las columnas con varios valores y hace que se devuelva un valor <strong>NULL</strong> cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Esta marca es solo para uso interno y no está pensada para usarse en la aplicación.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Esta marca es solo para uso interno y no está pensada para usarse en la aplicación.</p> | 
| <p>JET_bitRetrieveTuple</p> | <p>Esta marca permitirá la recuperación de un segmento de tupla del índice. Este bit debe especificarse con JET_bitRetrieveFromIndex.</p> | 



*pretinfo*

Si *pretinfo* se da como **NULL,** la función se comporta como si se hubieran dado una *itagSequence* de 1 y un *ibLongValue* de 0 (cero). Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y recupere datos largos en el desplazamiento 0 (cero).

Este parámetro se usa para proporcionar una o varias de las siguientes opciones:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Proporciona un desplazamiento binario en un valor de columna largo al recuperar una parte de un valor de columna.</p> | 
| <p>itagSequence</p> | <p>Proporciona el número de secuencia del valor de columna multivalor deseado. Tenga en cuenta que este campo solo se establece si se JET_bitRetrieveTag el campo. De lo contrario, no se modificará.</p> | 
| <p>columnidNextTagged</p> | <p>Devuelve el identificador de columna del valor de columna devuelto al recuperar todas las columnas etiquetadas, dispersas y multivalor mediante el paso <em>de columnid</em> de 0 (cero).</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBadColumnId</p> | <p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Se ha pasado un valor de número de secuencia de columna multivalor no válido en pretinfo- &gt; itagSequence. Los valores válidos para los números de secuencia de valores de columna multivalor son 1 o superior. Un valor de 0 (cero) no es válido para esta función.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el <em>columnid</em> dado no existe en la tabla.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Las columnas indizadas como subcadenas no se pueden recuperar del índice, ya que solo una pequeña parte de la columna suele estar presente en cada entrada de índice.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>En algunos casos, el búfer especificado para la columna de recuperación debe tener el tamaño suficiente para devolver cualquier cantidad del valor de columna. Por ejemplo, las columnas custodiables se ajustan para que sean coherentes para el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada. Si no se proporciona suficiente espacio en búfer, se JET_errInvalidBufferSize y no se devuelve ningún dato de columna.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno o varios de los parámetros dados son incorrectos. Esto puede ocurrir si retinfo.cbStruct es menor que el tamaño de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Las opciones proporcionadas son desconocidas o una combinación no conocida de la configuración de bits conocida.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no se coloca en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>No se pudo recuperar el valor completo de la columna porque el búfer especificado es menor que el tamaño de la columna.</p> | 
| <p>JET_wrnColumnNull</p> | <p>El valor de columna recuperado es <strong>NULL.</strong></p> | 



Si se ejecuta correctamente, el valor de columna de la columna especificada se copia en el búfer especificado. Se copia menos de todo el valor de columna con la advertencia JET_wrnBufferTruncated se devuelve. Si se *ha dado el valor deactual,* se devuelve el tamaño real del valor de columna. Tenga en **cuenta que los** valores NULL tienen una longitud de 0 (cero) y, por tanto, establecerán el tamaño devuelto en 0 (cero). Si la columna recuperada era una columna con varios valores y se ha especificado *pretinfo* y JET_bitReturnTag se estableció como opción, el número de secuencia del valor de columna se devuelve en pretinfo- \> itagSequence.

En caso de error, la ubicación del cursor se deja sin cambios y no se copia ningún dato en el búfer proporcionado.

#### <a name="remarks"></a>Comentarios

Esta llamada se usa una sola vez para recuperar datos de tamaño fijo o conocido para columnas no multivalor. Sin embargo, cuando los datos de columna son de tamaño desconocido, esta llamada se suele usar dos veces. Se llama primero para determinar el tamaño de los datos para poder asignar el espacio de almacenamiento necesario. A continuación, se realiza de nuevo la misma llamada para recuperar los datos de columna. Cuando se desconoce el número real de valores, dado que una columna tiene varios valores, la llamada se suele usar tres veces. Primero para obtener el número de valores y, a continuación, dos veces más para asignar almacenamiento y recuperar los datos reales.

La recuperación de todos los valores de una columna con varios valores se puede realizar llamando repetidamente a esta función con un valor pretinfo- itagSequence a partir de 1 y aumentando en cada llamada \> posterior. Se sabe que el último valor de columna se recupera cuando se devuelve un JET_wrnColumnNull de la función. Tenga en cuenta que este método no se puede realizar si la columna de varios valores tiene valores **NULL** explícitos establecidos en su secuencia de valores, ya que estos valores se omitirían. Si una aplicación desea recuperar todos los valores de columna con varios valores, incluidos los establecidos explícitamente en **NULL,** se debe usar [JetRetrieveColumns](./jetretrievecolumns-function.md) en lugar de **JetRetrieveColumn**. Tenga en cuenta que esta función no devuelve el número de valores de una función de varios valores cuando se proporciona un valor *itagSequence* de 0 (cero). Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) devolverá el número de valores de un valor de columna cuando se pasa un valor *itagSequence* de 0 (cero).

Si se llama a esta función en el nivel de transacción 0 (cero), por ejemplo, la sesión que realiza la llamada no está en una transacción, se abre y se cierra una transacción dentro de la función. El propósito de esto es devolver resultados coherentes en el caso de que un valor largo abarque las páginas de la base de datos. Tenga en cuenta que la transacción se libera entre llamadas de función y una serie de llamadas a esta función cuando la sesión no está en una transacción puede devolver datos actualizados después de la primera llamada a esta función.

El valor de columna predeterminado se recuperará cuando la columna no se haya establecido explícitamente en otro valor, a menos que se JET_bitRetrieveIgnoreDefault la opción de columna.

Recuperar el valor de la columna de autoincremento del búfer de copia antes de la inserción es un medio común de identificar un registro de forma única para la vinculación al insertar datos normalizados en varias tablas. El valor de autoincrement se asigna cuando comienza la operación de inserción y se puede recuperar del búfer de copia en cualquier momento hasta que se complete la actualización.

Al recuperar todas las columnas etiquetadas, con varios valores y dispersas, estableciendo *columnid* en 0 (cero), las columnas se recuperan en orden de *columnid* de *columnid* más bajo a *columnid más alto.* Se devuelve el mismo orden de valores de columna cada vez que se recuperan los valores de columna. El orden es determinista.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
