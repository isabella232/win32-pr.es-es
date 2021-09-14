---
description: 'Más información sobre: JetRetrieveColumns (Función)'
title: Función JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f70aa5914c6a0612adfa9ec6c8037059c8fb04a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360736"
---
# <a name="jetretrievecolumns-function"></a>Función JetRetrieveColumns


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetretrievecolumns-function"></a>Función JetRetrieveColumns

La **función JetRetrieveColumns** recupera varios valores de columna del registro actual en una sola operación. Se usa una [matriz](./jet-retrievecolumn-structure.md) de estructuras JET_RETRIEVECOLUMN para describir el conjunto de valores de columna que se va a recuperar y para describir los búferes de salida de cada valor de columna que se va a recuperar.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pretrievecolumn*

Puntero a una matriz de una o varias [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) estructura. Cada estructura incluye descripciones de qué valor de columna se va a recuperar y dónde almacenar los datos devueltos.

*cretrievecolumn*

Número de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) en la matriz dada por *pretrievecolumn*.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Se ha pasado un valor de número de secuencia de columna multivalor no válido en pretinfo- &gt; itagSequence. Los valores válidos para los números de secuencia de valores de columna multivalor son 1 o superior. Un valor de 0 (cero) es válido para esta función, pero no es válido para <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</p> | 
| <p>JET_errBadColumnId</p> | <p>El identificador de columna especificado está fuera de los límites legales de un identificador de columna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna descrita por el <em>columnid</em> dado no existe en la tabla.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Las columnas indizadas como subcadenas no se pueden recuperar del índice, ya que solo una pequeña parte de la columna suele estar presente en cada entrada de índice.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>En algunos casos, el búfer especificado para la columna de recuperación debe tener el tamaño suficiente para devolver cualquier cantidad del valor de columna. Por ejemplo, las columnas que se pueden custodiar se ajustan para ser coherentes con el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada. Si no se proporciona suficiente espacio en búfer, JET_errInvalidBufferSize devuelve y no se devuelve ningún dato de columna.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Las opciones proporcionadas son desconocidas o son una combinación no conocida de la configuración de bits conocida.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno o varios de los parámetros dados son incorrectos. Esto puede ocurrir si retinfo.cbStruct es menor que el <a href="gg294049(v=exchg.10).md">tamaño de JET_RETINFO</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca actualmente después del último registro en el índice actual.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>No se pudo recuperar el valor completo de la columna porque el búfer especificado es menor que el tamaño de la columna.</p> | 



Si se ejecuta correctamente, los datos de las columnas y el tamaño de columna se devuelven en los búferes proporcionados descritos en la matriz [de JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) columnas. Si se estableció una *itagSequence* en 0 (cero) para indicar que se deseaba el número de instancias de un campo con varios valores en lugar de los datos de columna, el número de instancias de una columna con varios valores se devuelve en el propio campo *itagSequence.* Cada [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) estructura tiene un campo de error que contiene advertencias para la columna recuperada. Si la columna tenía **un valor NULL,** el código de error se establecerá en JET_wrnColumnNull.

En caso de error, la ubicación del cursor se deja sin cambios y no se copia ningún dato en el búfer proporcionado.

#### <a name="remarks"></a>Observaciones

**JetRetrieveColumns** admite una característica que [JetRetrieveColumn](./jetretrievecolumn-function.md) no admite. Esta es la capacidad de recuperar el número de instancias de una columna con varios valores. El propósito de esta característica es permitir que una aplicación recupere todos los valores de una columna. Esto se puede hacer determinando primero el número de valores que tiene una columna. A continuación, sus longitudes se pueden determinar llamando [a](./jet-retrievecolumn-structure.md) **JetRetrieveColumns** de nuevo con una estructura JET_RETRIEVECOLUMN asignada para cada valor a fin de determinar la longitud de los datos de columna. Esto se puede hacer pasando **punteros NULL**_pvData_ con *cbMax* de 0 (cero) y recuperando la longitud de columna *en cbActual.* La tercera y la última llamada se pueden realizar con memoria asignada para los datos de valor de columna.

Si alguna columna recuperada se trunca debido a un búfer de longitud insuficiente, la API devolverá JET_wrnBufferTruncated. Sin embargo, otros errores, JET_wrnColumnNull solo se devuelven en el campo de error [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). El motivo es que las aplicaciones a menudo quieren asegurarse de que se han recuperado todos los datos y devolver este error de **JetRetrieveColumns** facilita esta comprensión.

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
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
