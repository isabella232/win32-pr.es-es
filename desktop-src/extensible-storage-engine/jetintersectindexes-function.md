---
description: 'Más información acerca de: JetIntersectIndexes (función)'
title: Función JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696219"
---
# <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes


_**Se aplica a:** Windows | Windows Server_

## <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes

La función **JetIntersectIndexes** calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios en la misma tabla. Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*rgindexrange*

Puntero a una matriz de estructuras de [JET_IndexRange](./jet-indexrange-structure.md) . Cada estructura incluye una [JET_TABLEID](./jet-tableid.md) que se ha configurado para contener uno de los intervalos de índice que se van a intersectar. Para obtener más información, vea [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

El número de estructuras [JET_IndexRange](./jet-indexrange-structure.md) en la matriz contenida en el parámetro *rgindexrange* .

*precordlist*

Puntero a una estructura de [JET_RECORDLIST](./jet-recordlist-structure.md) . Esta estructura se rellenará con información suficiente para atravesar la tabla temporal con los resultados de **JetIntersectIndexes**.

Búfer de salida que recibe una estructura de [JET_RECORDLIST](./jet-recordlist-structure.md) . La estructura contiene una descripción del conjunto de resultados de la intersección.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usó de forma incorrecta o no se implementó.</p>
<p><strong>JetIntersectIndexes</strong> devuelve este error cuando:</p>
<p>El <em>grbit</em> contenido en la estructura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> a la que apunta cualquier elemento de la matriz <em>rgindexrange</em> no es igual a JET_bitRecordInIndex.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contiene un valor inesperado o un valor incoherente cuando se combina con el valor de otro parámetro.</p>
<p>Este error lo devuelve <strong>JetIntersectIndexes</strong> por las razones siguientes:</p>
<ul>
<li><p>El parámetro <em>precordlist</em> es NULL.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de la estructura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> especificada en el parámetro <em>precordlist</em> no es igual que el tamaño de la estructura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</p></li>
<li><p>El parámetro <em>cindexrange</em> es cero.</p></li>
<li><p>El parámetro <em>cindexrange</em> es mayor que 64.</p></li>
<li><p>El miembro <strong>cbStruct</strong> de cualquier elemento de la matriz especificado por el parámetro <em>rgindexrange</em> no es igual que el tamaño de la estructura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</p></li>
<li><p>Los elementos de la matriz <em>rgindexrange</em> contienen <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s de tablas diferentes.</p></li>
<li><p>Un elemento de la matriz <em>rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que no está situado en un índice secundario.</p></li>
<li><p>Uno o varios de los elementos de la matriz <em>rgindexrange</em> contienen <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>que se colocan en el mismo índice secundario.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p>
<p>Este error no se devuelve en todas las circunstancias. Los identificadores se validan solo en función del mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran mediante una llamada a <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxCursors</em> especificado en el parámetro <em>paramid</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p>
<p><strong>JetIntersectIndexes</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host está demasiado fragmentado. El administrador de tablas temporales asignará siempre un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar. <strong>JetIntersectIndexes</strong> creará una tabla temporal para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificada en el parámetro <em>rgindexrange</em> y una tabla temporal para la salida en <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No es válido utilizar la misma sesión desde más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> especificado en el parámetro <em>paramid</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> especificado en el parámetro <em>paramid</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>No se pudo realizar la operación porque el motor no pudo asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporal se configuran mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxTemporaryTables especificado en el parámetro <em>paramid</em> .</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devuelve una nueva tabla temporal que contiene los marcadores de los registros que coinciden con los criterios representados por cada una de las descripciones del intervalo de índices de entrada.

En caso de error, no se creará la tabla temporal que contiene los resultados. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios. Se puede cambiar la posición actual del [JET_TABLEID](./jet-tableid.md)s proporcionado a esta función.

#### <a name="remarks"></a>Observaciones

**JetIntersectIndexes** se puede usar para filtrar de forma eficaz los registros de una tabla mediante varios criterios si esos criterios se pueden expresar en términos de los índices secundarios de esa tabla. Por ejemplo, supongamos que tiene una tabla muy grande que contiene personas. La tabla puede tener columnas para el ID. de usuario, el nombre, el apellido, etc. Supongamos que cada una de estas columnas se indexa por separado y que el índice principal de la tabla está por encima del identificador de usuario. Si desea buscar todos los usuarios cuyo nombre comienza por un y cuyo apellido empieza por G, debe realizar los siguientes pasos:

1.  Abra un nuevo cursor en la tabla y establezca ese cursor para usar el índice sobre la columna "First Name". A continuación, configure un intervalo de índice para todas las personas cuyo "First Name" comenzó con "A" y cree un [JET_IndexRange](./jet-indexrange-structure.md) struct que contenga este cursor.

2.  Repita el paso 1 con un nuevo cursor en el índice "Last Name" para todas las personas cuyo "Last Name" comenzó con "G".

3.  Pase estos criterios a **JetIntersectIndexes** para calcular el resultado en una tabla temporal.

4.  Recorra la tabla temporal y recupere cada uno de los registros que pasan los criterios por marcador.

La tabla temporal que contiene el conjunto de resultados es una tabla simple con una columna que contiene el marcador de cada registro que pasó todos los criterios usados para calcular la intersección. El conjunto de resultados se ordena en el mismo orden que el índice principal y no contiene entradas duplicadas. La aplicación puede enumerar los resultados de la intersección enumerando las filas de la tabla temporal, recuperando el marcador de cada resultado mediante [JetRetrieveColumn](./jetretrievecolumn-function.md)y, a continuación, visitando el registro en la base de datos llamando a [JetGotoBookmark](./jetgotobookmark-function.md) con ese marcador en un cursor situado en el índice principal.

La tabla temporal devuelta por **JetIntersectIndexes** solo se puede examinar en una dirección hacia delante. También debe cerrarse a través de [JetCloseTable](./jetclosetable-function.md) cuando se haya completado el examen. Para obtener más información acerca de las tablas temporales y cómo funcionan, vea [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes** suele ser una manera eficaz y cómoda de filtrar registros en función de varios criterios indexados. Sin embargo, hay algunas sugerencias importantes que deben seguirse para maximizar la utilidad de esta característica. Si sabe que uno de los criterios es tan restrictivo que el intervalo de índice resultante tiene muy pocos registros, probablemente sea mejor recorrer ese intervalo de índice y filtrar los registros en el nivel de aplicación. Además, si sabe que tiene criterios que son mucho menos restrictivos que otros criterios de la intersección, puede considerar la posibilidad de quitar esos criterios de la intersección de forma mucho menos restrictiva. Por último, si sabe que uno de los criterios no es estrictamente restrictivo, de modo que el intervalo de índice resultante es casi tan grande como el índice principal, es improbable que la intersección con ese intervalo de índice se beneficie (reduzca el tamaño del) del conjunto de resultados. En todos los casos, debe seleccionar los criterios de una manera que tomará el menor número posible de entradas de índice en la entrada y generará el conjunto más específico de marcadores en la salida para obtener el máximo rendimiento.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
