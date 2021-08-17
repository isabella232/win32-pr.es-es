---
description: 'Más información sobre: JetIntersectIndexes (Función)'
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
ms.openlocfilehash: 23d9d7bcd7d41251883313517db34f0cbca0ec8e6d2aaa5946348057cc29d844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978875"
---
# <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes

La **función JetIntersectIndexes** calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios en la misma tabla. Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice.

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

Puntero a una matriz de [JET_IndexRange](./jet-indexrange-structure.md) estructura. Cada estructura incluye un [JET_TABLEID](./jet-tableid.md) que se ha configurado para contener uno de los intervalos de índice que se van a formar una intersección. Para obtener más información, [vea JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Número de estructuras [JET_IndexRange](./jet-indexrange-structure.md) en la matriz contenida en el *parámetro rgindexrange.*

*precordlist*

Puntero a una [JET_RECORDLIST](./jet-recordlist-structure.md) estructura. Esta estructura se rellenará con suficiente información para recorrer la tabla temporal con los resultados de **JetIntersectIndexes**.

Búfer de salida que recibe una [JET_RECORDLIST](./jet-recordlist-structure.md) estructura. La estructura contiene una descripción del conjunto de resultados de la intersección.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usaba incorrectamente o no se implementaba.</p>
<p><strong>JetIntersectIndexes</strong> devuelve este error cuando:</p>
<p>El <em>grbit</em> contenido en la <a href="gg269335(v=exchg.10).md">estructura JET_IndexRange</a> a la que apunta cualquier elemento de la <em>matriz rgindexrange</em> no es igual a JET_bitRecordInIndex.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contiene un valor inesperado o un valor que es incoherente cuando se combina con el valor de otro parámetro.</p>
<p><strong>JetIntersectIndexes</strong> devuelve este error por los siguientes motivos:</p>
<ul>
<li><p>El <em>parámetro precordlist</em> es NULL.</p></li>
<li><p>El <strong>miembro cbStruct</strong> de la <a href="gg269287(v=exchg.10).md">estructura JET_RECORDLIST</a> especificada en el parámetro <em>precordlist</em> no es igual al tamaño de <a href="gg269287(v=exchg.10).md">la JET_RECORDLIST</a> estructura.</p></li>
<li><p>El <em>parámetro cindexrange</em> es cero.</p></li>
<li><p>El <em>parámetro cindexrange</em> es mayor que 64.</p></li>
<li><p>El <strong>miembro cbStruct</strong> de cualquier elemento de la matriz especificado por el parámetro <em>rgindexrange</em> no es igual al tamaño de la <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> estructura.</p></li>
<li><p>Los elementos de la <em>matriz rgindexrange</em> <a href="gg269182(v=exchg.10).md">contienen JET_TABLEID</a>de tablas diferentes.</p></li>
<li><p>Un elemento de la <em>matriz rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que no está situado en un índice secundario.</p></li>
<li><p>Uno o varios de los elementos de la <em>matriz rgindexrange</em> <a href="gg269182(v=exchg.10).md">contienen</a>JET_TABLEID están situados en el mismo índice secundario.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p>
<p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Error en la operación porque el motor no pudo asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran mediante una llamada <a href="gg294044(v=exchg.10).md">a JetSetSystemParameter</a> <em>JET_paramMaxCursors</em> especificado en el <em>parámetro paramid.</em></p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p>
<p><strong>JetIntersectIndexes</strong> puede devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host se fragmenta demasiado. El administrador de tablas temporales siempre asignará un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar. <strong>JetIntersectIndexes creará</strong> una tabla temporal para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificada en el parámetro <em>rgindexrange</em> y una tabla temporal para la salida <a href="gg269287(v=exchg.10).md">en JET_RECORDLIST</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No es posible usar la misma sesión desde más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Error en la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en <em></em> caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables especificado en el <em>parámetro paramid.</em></p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Error en la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar <em></em> en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables especificado en el <em>parámetro paramid.</em></p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>Error en la operación porque el motor no pudo asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporales se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> con JET_paramMaxTemporaryTables especificado en el <em>parámetro paramid.</em></p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se devuelve una nueva tabla temporal que contiene los marcadores de los registros que coinciden con los criterios representados por cada una de las descripciones del intervalo de índice de entrada.

En caso de error, no se creará la tabla temporal que contiene los resultados. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales que use el motor de base de datos permanecerá sin cambios. La posición actual de los [JET_TABLEID](./jet-tableid.md)proporcionados a esta función puede cambiarse.

#### <a name="remarks"></a>Comentarios

**JetIntersectIndexes** se puede usar para filtrar eficazmente los registros de una tabla por varios criterios si esos criterios se pueden expresar en términos de los índices secundarios sobre esa tabla. Por ejemplo, tenga en cuenta que tiene una tabla muy grande que contiene personas. La tabla puede tener columnas para su identificador de usuario, nombre, apellido, y así sucesivamente. Supongamos que cada una de estas columnas se indexa por separado y que el índice principal de la tabla está por encima del identificador de usuario. Si quisiera encontrar a todos los usuarios cuyo nombre empieza por A y cuyo apellido empieza por G, realizaría los pasos siguientes:

1.  Abra un nuevo cursor en la tabla y establezca ese cursor para que use el índice sobre la columna "nombre". A continuación, configure un intervalo de índice para todas las personas cuyo "nombre" empezó con ["A"](./jet-indexrange-structure.md) y cree JET_IndexRange estructura que contiene este cursor.

2.  Repita el paso 1 con un nuevo cursor en el índice "apellidos" para todas las personas cuyo "apellido" empezó con "G".

3.  Pase estos criterios a **JetIntersectIndexes para** calcular el resultado en una tabla temporal.

4.  Recorre la tabla temporal y recupera cada uno de los registros que pasan los criterios por marcador.

La tabla temporal que contiene el conjunto de resultados es una tabla simple con una columna que contiene el marcador de cada registro que pasó todos los criterios usados para calcular la intersección. El conjunto de resultados se ordena en el mismo orden que el índice principal y no contiene entradas duplicadas. La aplicación puede enumerar los resultados de la intersección enumerando las filas de la tabla temporal, recuperando el marcador para cada resultado mediante [JetRetrieveColumn](./jetretrievecolumn-function.md)y, a continuación, visitando el registro en la base de datos llamando a [JetGotoBookmark](./jetgotobookmark-function.md) con ese marcador en un cursor situado en el índice principal.

La tabla temporal devuelta **por JetIntersectIndexes** solo se puede examinar en una dirección hacia delante. También se debe cerrar a través [de JetCloseTable](./jetclosetable-function.md) cuando se haya completado el examen. Para obtener más información sobre las tablas temporales y cómo funcionan, vea [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes suele** ser una manera eficaz y cómoda de filtrar registros en función de varios criterios indexados. Sin embargo, hay algunas sugerencias importantes que se deben seguir para maximizar la utilidad de esta característica. Si sabe que uno de los criterios es tan restrictivo que el intervalo de índice resultante tiene muy pocos registros, probablemente sea mejor simplemente recorrer ese intervalo de índice y filtrar los registros en el nivel de aplicación. Además, si sabe que tiene criterios mucho menos restrictivos que otros criterios en la intersección, puede considerar la posibilidad de quitar esos criterios mucho menos restrictivos de la intersección. Por último, si sabe que uno de los criterios no es en absoluto restrictivo, de modo que el intervalo de índice resultante es casi tan grande como el índice principal, es poco probable que la intersección con ese intervalo de índice beneficie (reduzca el tamaño de) del conjunto de resultados. En todos los casos, debe seleccionar criterios de una manera que tome el menor número posible de entradas de índice en la entrada y genere el conjunto de marcadores más específico en la salida para obtener el máximo rendimiento.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
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
