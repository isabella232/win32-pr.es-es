---
description: 'Más información acerca de: JetRetrieveColumns (función)'
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
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278935"
---
# <a name="jetretrievecolumns-function"></a>Función JetRetrieveColumns


_**Se aplica a:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>Función JetRetrieveColumns

La función **JetRetrieveColumns** Recupera varios valores de columna del registro actual en una sola operación. Una matriz de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) se utiliza para describir el conjunto de valores de columna que se va a recuperar y para describir los búferes de salida de cada valor de columna que se va a recuperar.

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

*TABLEID*

Cursor que se va a usar para esta llamada.

*pretrievecolumn*

Puntero a una matriz de una o varias estructuras de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Cada estructura incluye descripciones de qué valor de columna recuperar y dónde almacenar los datos devueltos.

*cretrievecolumn*

El número de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) en la matriz dada por *pretrievecolumn*.

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>Se pasó un valor de número de secuencia de columna con varios valores no válido en pretinfo- &gt; itagSequence. Los valores válidos para los números de secuencia de valores de columna con varios valores son 1 o superior. Un valor de 0 (cero) es válido para esta función, pero no es válido para <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Las columnas indizadas como subcadenas no se pueden recuperar del índice, puesto que solo una pequeña parte de la columna está presente normalmente en cada entrada de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>En algunos casos, el búfer proporcionado para la columna de recuperación debe tener el tamaño suficiente para poder devolver cualquier cantidad de valor de columna. Por ejemplo, las columnas actualizables de custodia se ajustan para ser coherentes con el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada. Si se proporciona espacio en búfer insuficiente, se devuelve JET_errInvalidBufferSize y no se devuelve ningún dato de columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno o varios de los parámetros especificados no son correctos. Esto puede ocurrir si retinfo. cbStruct es más pequeño que el tamaño de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>No se pudo recuperar el valor de columna completo porque el búfer especificado es menor que el tamaño de la columna.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devuelven los datos de columnas y el tamaño de columna en los búferes proporcionados descritos en la matriz de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Si un *itagSequence* se ha establecido en 0 (cero) para indicar que se desea el número de instancias de un campo con varios valores en lugar de los datos de la columna, el número de instancias de una columna con varios valores se devuelve en el propio campo *itagSequence* . Cada estructura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) tiene un campo de error que contiene advertencias para la columna recuperada. Si el valor de la columna era **null** , el código de error se establecerá en JET_wrnColumnNull.

En caso de error, la ubicación del cursor se deja sin modificar y no se copia ningún dato en el búfer proporcionado.

#### <a name="remarks"></a>Observaciones

**JetRetrieveColumns** admite una característica que [JetRetrieveColumn](./jetretrievecolumn-function.md) no. Se trata de la capacidad de recuperar el número de instancias de una columna con varios valores. La finalidad de esta característica es permitir que una aplicación recupere todos los valores de una columna. Esto se puede hacer determinando primero el número de valores que tiene una columna. A continuación, se pueden determinar sus longitudes llamando a **JetRetrieveColumns** de nuevo con una [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) estructura asignada para cada valor para determinar la longitud de los datos de la columna. Esto se puede hacer pasando los punteros **null**_pvData_ con *cbMax* de 0 (cero) y recuperando la longitud de la columna en *cbActual*. La tercera y última llamada se puede realizar con memoria asignada para los datos del valor de la columna.

Si alguna columna recuperada se trunca debido a un búfer de longitud insuficiente, la API devolverá JET_wrnBufferTruncated. Sin embargo, otros errores, JET_wrnColumnNull se devuelven solo en el campo error de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). La razón de esto es que las aplicaciones suelen querer asegurarse de que todos los datos se han recuperado y devolver este error de **JetRetrieveColumns** facilita esta comprensión.

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
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
