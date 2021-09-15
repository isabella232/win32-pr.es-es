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
ms.openlocfilehash: 34909de0f732a49711d316affae3eb84487420d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475976"
---
# <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetintersectindexes-function"></a>Función JetIntersectIndexes

La **función JetIntersectIndexes** calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios sobre la misma tabla. Esta operación es útil para buscar el conjunto de registros de una tabla que coincidan con dos o más criterios que se pueden expresar mediante intervalos de índice.

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

Puntero a una matriz de [JET_IndexRange](./jet-indexrange-structure.md) estructuras. Cada estructura incluye un [JET_TABLEID](./jet-tableid.md) que se ha configurado para contener uno de los intervalos de índice que se van a formar una intersección. Para obtener más información, [vea JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Número de estructuras [JET_IndexRange](./jet-indexrange-structure.md) en la matriz que se encuentra en el *parámetro rgindexrange.*

*precordlist*

Puntero a una [JET_RECORDLIST](./jet-recordlist-structure.md) estructura. Esta estructura se rellenará con suficiente información para recorrer la tabla temporal con los resultados de **JetIntersectIndexes**.

Búfer de salida que recibe una [JET_RECORDLIST](./jet-recordlist-structure.md) estructura. La estructura contiene una descripción del conjunto de resultados de la intersección.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida, se usaba incorrectamente o no se implementaba.</p><p><strong>JetIntersectIndexes</strong> devuelve este error cuando:</p><p>El <em>grbit</em> contenido en la <a href="gg269335(v=exchg.10).md">estructura JET_IndexRange</a> a la que apunta cualquier elemento de la <em>matriz rgindexrange</em> no es igual a JET_bitRecordInIndex.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contiene un valor inesperado o un valor que es incoherente cuando se combina con el valor de otro parámetro.</p><p><strong>JetIntersectIndexes</strong> devuelve este error por los siguientes motivos:</p><ul><li><p>El <em>parámetro precordlist</em> es NULL.</p></li><li><p>El <strong>miembro cbStruct</strong> de la <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> especificada en el <em>parámetro precordlist</em> no es igual al tamaño de la <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> estructura.</p></li><li><p>El <em>parámetro cindexrange</em> es cero.</p></li><li><p>El <em>parámetro cindexrange</em> es mayor que 64.</p></li><li><p>El <strong>miembro cbStruct</strong> de cualquier elemento de la matriz especificada por el parámetro <em>rgindexrange</em> no es igual al tamaño de la <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> estructura.</p></li><li><p>Los elementos de la <em>matriz rgindexrange</em> <a href="gg269182(v=exchg.10).md">contienen JET_TABLEID</a>de tablas diferentes.</p></li><li><p>Un elemento de la <em>matriz rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> que no está situado en un índice secundario.</p></li><li><p>Uno o varios de los elementos de la <em>matriz rgindexrange</em> <a href="gg269182(v=exchg.10).md">contienen</a>JET_TABLEID s situados en el mismo índice secundario.</p></li></ul> | 
| <p>JET_errInvalidSesid</p> | <p>El identificador de sesión no es válido o hace referencia a una sesión cerrada.</p><p>Este error no se devuelve en todas las circunstancias. Los identificadores solo se validan con el mejor esfuerzo.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Error en la operación porque el motor no pudo asignar los recursos necesarios para abrir un nuevo cursor. Los recursos de cursor se configuran mediante una llamada <a href="gg294044(v=exchg.10).md">a JetSetSystemParameter</a> <em>JET_paramMaxCursors</em> especificado en el <em>parámetro paramid.</em></p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar suficiente memoria para completarla.</p><p><strong>JetIntersectIndexes puede</strong> devolver JET_errOutOfMemory si el espacio de direcciones del proceso de host se fragmenta demasiado. El administrador de tablas temporales siempre asignará un fragmento de 1 MB de espacio de direcciones para cada tabla temporal creada independientemente de la cantidad de datos que se van a almacenar. <strong>JetIntersectIndexes creará</strong> una tabla temporal para cada <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> especificado en el parámetro <em>rgindexrange</em> y una tabla temporal para la salida <a href="gg269287(v=exchg.10).md">en JET_RECORDLIST</a>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No es posible usar la misma sesión desde más de un subproceso al mismo tiempo.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>Error en la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché los índices de la tabla. El número de índices cuyo esquema se puede almacenar en <em></em> caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables especificado en el <em>parámetro paramid.</em></p> | 
| <p>JET_errTooManyOpenTables</p> | <p>Error en la operación porque el motor no pudo asignar los recursos necesarios para almacenar en caché el esquema de la tabla. El número de tablas cuyo esquema se puede almacenar <em></em> en caché se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables especificado en el <em>parámetro paramid.</em></p> | 
| <p>JET_errTooManySorts</p> | <p>Error en la operación porque el motor no pudo asignar los recursos necesarios para crear una tabla temporal. Los recursos de tabla temporal se configuran <a href="gg294044(v=exchg.10).md">mediante JetSetSystemParameter</a> con JET_paramMaxTemporaryTables especificado en el <em>parámetro paramid.</em></p> | 



Si se ejecuta correctamente, se devuelve una nueva tabla temporal que contiene los marcadores de los registros que coinciden con los criterios representados por cada una de las descripciones del intervalo de índice de entrada.

En caso de error, no se creará la tabla temporal que contiene los resultados. Se puede cambiar el estado de la base de datos temporal. El estado de las bases de datos normales en uso por el motor de base de datos permanecerá sin cambios. La posición actual de los [JET_TABLEID](./jet-tableid.md)proporcionados a esta función se puede cambiar.

#### <a name="remarks"></a>Observaciones

**JetIntersectIndexes** se puede usar para filtrar eficazmente los registros de una tabla por varios criterios si esos criterios se pueden expresar en términos de índices secundarios sobre esa tabla. Por ejemplo, tenga en cuenta que tiene una tabla muy grande que contiene personas. La tabla puede tener columnas para su identificador de usuario, nombre, apellido, y así sucesivamente. Supongamos que cada una de estas columnas se indexa por separado y que el índice principal de la tabla está por encima del identificador de usuario. Si quisiera encontrar a todos aquellos cuyo nombre empiece por A y cuyo apellido comience por G, realizaría los pasos siguientes:

1.  Abra un nuevo cursor en la tabla y establezca ese cursor para que use el índice sobre la columna "nombre". A continuación, configure un intervalo de índice para todas las [](./jet-indexrange-structure.md) personas cuyo "nombre" se inició con "A" y cree una estructura JET_IndexRange que contenga este cursor.

2.  Repita el paso 1 con un nuevo cursor en el índice "apellidos" para todas las personas cuyo "apellido" se inició con "G".

3.  Pase estos criterios a **JetIntersectIndexes para** calcular el resultado en una tabla temporal.

4.  Recor la tabla temporal y recuperar cada uno de los registros que pasan los criterios por marcador.

La tabla temporal que contiene el conjunto de resultados es una tabla simple con una columna que contiene el marcador de cada registro que superó todos los criterios usados para calcular la intersección. El conjunto de resultados se ordena en el mismo orden que el índice principal y no contiene entradas duplicadas. La aplicación puede enumerar los resultados de la intersección enumerando las filas de la tabla temporal, recuperando el marcador para cada resultado mediante [JetRetrieveColumn](./jetretrievecolumn-function.md)y, a continuación, visitando el registro en la base de datos llamando a [JetGotoBookmark](./jetgotobookmark-function.md) con ese marcador en un cursor situado en el índice principal.

La tabla temporal devuelta **por JetIntersectIndexes** solo se puede examinar en una dirección hacia delante. También se debe cerrar a través [de JetCloseTable](./jetclosetable-function.md) cuando se haya completado el examen. Para obtener más información sobre las tablas temporales y cómo funcionan, vea [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes suele** ser una manera eficaz y cómoda de filtrar registros en función de varios criterios indexados. Sin embargo, hay algunas sugerencias importantes que se deben seguir para maximizar la utilidad de esta característica. Si sabe que uno de los criterios es tan restrictivo que el intervalo de índice resultante tiene muy pocos registros, probablemente sea mejor simplemente recorrer ese intervalo de índice y filtrar los registros en el nivel de aplicación. Además, si sabe que tiene criterios mucho menos restrictivos que otros criterios en la intersección, puede considerar la posibilidad de quitar esos criterios mucho menos restrictivos de la intersección. Por último, si sabe que uno de los criterios no es en absoluto restrictivo, de modo que el intervalo de índice resultante es casi tan grande como el índice principal, es poco probable que la intersección con ese intervalo de índice beneficie (reduzca el tamaño de) del conjunto de resultados. En todos los casos, debe seleccionar criterios de una manera que tome el menor número posible de entradas de índice en la entrada y genere el conjunto de marcadores más específico en la salida para obtener el máximo rendimiento.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
