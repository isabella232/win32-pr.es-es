---
description: 'Más información sobre: JetMakeKey (Función)'
title: Función JetMakeKey
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b0a7300a312bf5f34c2a60cc6ed3b3c95879dde
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983408"
---
# <a name="jetmakekey-function"></a>Función JetMakeKey


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetmakekey-function"></a>Función JetMakeKey

La **función JetMakeKey** construye claves de búsqueda que, a continuación, se pueden usar para buscar un conjunto de entradas en un índice mediante algunos criterios de búsqueda simples sobre sus valores de columna de clave. Una clave de búsqueda también es una de las propiedades intrínsecas de un cursor y la usan las operaciones [JetSeek](./jetseek-function.md) y [JetSetIndexRange](./jetsetindexrange-function.md) para buscar entradas de índice que coincidan con estos criterios de búsqueda en el índice actual de ese cursor. Una clave de búsqueda completa se basa en una serie de llamadas a **JetMakeKey** en las que cada llamada se usa para cargar el valor de columna de la siguiente columna de clave del índice actual de un cursor. También es posible cargar una clave de búsqueda construida previamente que se ha recuperado del cursor [mediante JetRetrieveKey](./jetretrievekey-function.md).

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*tableid*

Cursor que se va a usar para esta llamada.

*pvData*

Búfer de entrada que contiene los datos de columna de la columna de clave actual del índice actual del cursor para el que se está construyendo la clave de búsqueda.

El tipo de datos de los datos de columna en el búfer de entrada debe coincidir exactamente con el tipo de datos y otras propiedades de la definición de columna de la columna de clave actual. No se realiza ninguna coerción de tipo en los datos de columna.

Si JET_bitNormalizedKey especifica en el parámetro *grbit,* el búfer de entrada debe contener una clave de búsqueda construida previamente. Estas claves se obtienen mediante una llamada a [JetRetrieveKey.](./jetretrievekey-function.md)

*cbData*

Tamaño en bytes de los datos de columna proporcionados en el búfer de entrada.

Si JET_bitNormalizedKey especifica en el parámetro *grbit,* este es el tamaño de la clave de búsqueda proporcionada en el búfer de entrada.

Si el tamaño de los datos de columna es cero, se omite el contenido del búfer de entrada. Si JET_bitKeyDataZeroLength especifica en el parámetro *grbit* y la columna de clave actual del índice actual del cursor es una columna de longitud variable, se supone que los datos de la columna de entrada son un valor de longitud cero. De lo contrario, se supone que los datos de la columna de entrada son un valor NULL.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>La clave de búsqueda debe construirse de forma que las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li><li><p>Cualquier valor de columna necesario para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>La clave de búsqueda debe construirse de forma que todas las columnas de clave que vienen después de la columna de clave actual se consideren caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li><li><p>Cualquier valor de columna necesario para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al inicio de un índice. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de ese índice. El inicio del índice no es el mismo que el extremo bajo del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>Si el tamaño del búfer de entrada es cero y la columna de clave actual es una columna de longitud variable, esta opción indica que el búfer de entrada contiene un valor de longitud cero. De lo contrario, un tamaño de búfer de entrada de cero indicaría un valor NULL.</p> | 
| <p>JET_bitNewKey</p> | <p>Se debe construir una nueva clave de búsqueda. Se descarta cualquier clave de búsqueda existente anteriormente.</p> | 
| <p>JET_bitNormalizedKey</p> | <p>Cuando se especifica esta opción, se omiten todas las demás opciones, se descarta cualquier clave de búsqueda existente anteriormente y el contenido del búfer de entrada se carga como la nueva clave de búsqueda.</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>La clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li><li><p>Cualquier valor de columna necesario para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Esta opción no se puede usar cuando la columna de clave actual no es una columna de texto o una columna binaria variable. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p><p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>Esta opción indica que la clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que todas las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li><li><p>Cualquier valor de columna necesario para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al inicio de un índice. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de ese índice. El inicio del índice no es el mismo que el extremo bajo del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Esta opción no se puede usar cuando la columna de clave actual no es una columna de texto o una columna binaria variable. Se producirá un error en la operación JET_errInvalidgrbit si se intenta.</p><p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p> | 
| <p>JET_bitStrLimit</p> | <p>Esta opción indica que la clave de búsqueda debe construirse de forma que todas las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li><li><p>Cualquier valor de columna necesario para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Cuando esta opción se especifica en combinación con JET_bitSubStrLimit columna de clave actual es una columna de texto, esta opción se omitirá. Este comportamiento está pensado para permitir que el tipo de la columna de clave actual se infera al compilar la clave de búsqueda.</p><p>Si desea crear una clave de búsqueda similar para el inicio de un índice, se debe realizar una llamada similar a <strong>JetMakeKey</strong> para la última columna de clave que no sea un carácter comodín, pero sin opciones de caracteres comodín especificadas. A continuación, la clave de búsqueda se encuentra en un estado adecuado para usarlo en este tipo de búsqueda. Esto es análogo al uso de JET_bitFullColumnStartLimit, salvo que la clave de búsqueda no está correctamente finalizada como después del uso de una opción de carácter comodín.</p><p>Esta opción ha quedado en desuso para Windows XP y versiones posteriores con el fin de abordar esta semántica complicada. JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit se deben usar siempre que sea posible.</p> | 
| <p>JET_bitSubStrLimit</p> | <p>Esta opción indica que la clave de búsqueda debe construirse de forma que la columna de clave actual se considere un carácter comodín de prefijo y que todas las columnas de clave que vienen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida se puede usar para buscar coincidencias con las entradas de índice que tienen lo siguiente:</p><ul><li><p>Los valores de columna exactos proporcionados para todas las columnas de clave anteriores.</p></li><li><p>Los datos de columna especificados como prefijo de su valor de columna para la columna de clave actual.</p></li><li><p>Cualquier valor de columna para las columnas de clave posteriores.</p></li></ul><p>Esta opción debe usarse al crear claves de búsqueda con caracteres comodín para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de ese índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p><p>Cuando esta opción se especifica en combinación con JET_bitStrLimit columna de clave actual es una columna de texto, esta opción tendrá prioridad. Esta opción se omite cuando la columna de clave actual no es una columna de texto. Este comportamiento está pensado para permitir que el tipo de la columna de clave actual se infera al compilar la clave de búsqueda.</p><p>Si desea crear una clave de búsqueda similar para el inicio de un índice, se debe realizar una llamada similar a <strong>JetMakeKey</strong> para la columna de clave que va a ser el carácter comodín de prefijo, pero sin especificar ninguna opción de carácter comodín. A continuación, la clave de búsqueda se encuentra en un estado adecuado para usarlo en este tipo de búsqueda. Esto es análogo al uso de JET_bitPartialColumnStartLimit, salvo que la clave de búsqueda no está correctamente finalizada como después del uso de una opción de carácter comodín.</p><p>Esta opción ha quedado en desuso para Windows XP y versiones posteriores con el fin de abordar esta semántica complicada. JET_bitPartialColumnStartLimit y JET_bitPartialColumnEndLimit se deben usar en su lugar, siempre que sea posible.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>Los datos de columna proporcionados son demasiado pequeños para generar una clave válida para el índice actual porque ese índice es un índice de tupla y el tamaño mínimo de la tupla era mayor que los datos de columna proporcionados. Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex para</a> obtener más información sobre los índices de tupla. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Los datos de columna proporcionados no coinciden con el tamaño requerido por la definición de columna. Esto puede ocurrir si el tipo de datos de la columna tiene intrínsecamente un tamaño determinado. Esto también puede ocurrir si el tipo de datos de la columna no tiene intrínsecamente un tamaño determinado, pero la definición de la columna declara que tiene una longitud fija. Una excepción a esto es que este error no se producirá cuando se proporcionan demasiados datos para una columna de texto de longitud fija porque los datos que faltan se agregarán automáticamente con espacios. Una segunda excepción a esto es que este error no se producirá cuando se proporcionan demasiados datos para una columna binaria de longitud fija porque los datos que faltan se agregarán automáticamente con ceros.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una de las opciones solicitadas no era válida, se usaba de forma no válida o no se implementaba. Esto puede ocurrir para <strong>JetMakeKey</strong> cuando:</p><ul><li><p>JET_bitPartialColumnStartLimit o JET_bitPartialColumnEndLimit se especifican y la columna de clave correspondiente no es una columna de texto y no es una columna binaria de longitud variable. Este caso solo se produce en Windows XP y versiones posteriores.</p></li><li><p>Se intenta usar más de una de las siguientes opciones juntas: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit. Este caso solo se produce en Windows XP y versiones posteriores.</p></li><li><p>Se intenta usar JET_bitStrLimit o JET_bitSubStrLimit cuando se usa una de las siguientes opciones: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit. Este caso solo se produce en Windows XP y versiones posteriores.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro.</p><p>Esto puede ocurrir para <strong>JetMakeKey</strong> JET_bitNormalizedKey se especificó y el valor proporcionado en el búfer de entrada era demasiado grande para ser una clave de búsqueda válida.</p> | 
| <p>JET_errKeyIsMade</p> | <p>Los datos de columna proporcionados <strong>a JetMakeKey</strong> se rechazaron porque ya se han proporcionado datos de columna para todas las columnas de clave del índice actual. Esto puede ocurrir de tres maneras. La primera es si se proporcionan datos de columna para cada columna de clave del índice actual. La segunda es si se han proporcionado datos de columna para al menos una columna de clave y se ha elegido una opción comodín para la última llamada. La tercera es si se proporcionó una clave de búsqueda construida previamente mediante JET_bitNormalizedKey, que abarca todas las columnas de clave.</p> | 
| <p>JET_errKeyNotMade</p> | <p>No hay ninguna clave de búsqueda actual para el cursor. Esto ocurrirá con <strong>JetMakeKey</strong> si JET_bitNewKey no se especifica y no se ha construido una clave de búsqueda para este cursor mediante una llamada anterior a <strong>JetMakeKey</strong>. La clave de búsqueda se eliminará mediante una llamada anterior a cualquier API de navegación en el cursor que no <a href="gg294117(v=exchg.10).md">sea JetMove</a>.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>No hay ningún índice actual para el cursor. Esto ocurrirá con <strong>JetMakeKey</strong> si el cursor está en el índice clúster de una tabla, no se ha definido un índice principal y no se JET_bitNormalizedKey especificado. No es posible construir una clave de búsqueda si el cursor está en un índice que no tiene ninguna columna de clave a menos que se proporciona una clave de búsqueda construida previamente.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, JET_bitNormalizedKey y JET_bitNewKey no se especificaron, los criterios de búsqueda habrán creado la clave de búsqueda para una columna de clave más en el índice actual. Si JET_bitNormalizedKey no se especificó y se especificó JET_bitNewKey, se descartaron las claves de búsqueda existentes anteriormente y se habrá creado una nueva por los criterios de búsqueda para la primera columna de clave del índice actual. Si JET_bitNormalizedKey especificado, se descarta cualquier clave de búsqueda existente previamente y se carga una nueva desde el búfer de entrada. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

En caso de error, JET_bitNormalizedKey o JET_bitNewKey especificado, el estado de la clave de búsqueda es indefinido. Si no se JET_bitNormalizedKey ni JET_bitNewKey, no se producirá ningún cambio en el estado de la clave de búsqueda. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Las claves deben tratarse como fragmentos opacos de datos. No se debe intentar aprovechar la estructura interna de estos datos. Sin embargo, se conoce lo siguiente sobre todas las claves ESENT:

  - Las claves se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su ordenación relativa en el índice de origen sobre la tabla de las entradas del índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser mayores. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

Las claves de búsqueda pueden tener un byte más si se usó una opción de carácter comodín. En ese caso, la clave de búsqueda será de hasta JET_cbLimitKeyMost (256) bytes para las versiones anteriores a Windows Vista y JET_paramKeyMost + 1 bytes para Windows Vista y versiones posteriores.

Hay una ramificación muy importante a este tamaño máximo de clave. Siempre que haya una entrada de índice que tenga valores de columna lo suficientemente grandes como para hacer que se genere una clave para ese índice que, de lo contrario, sería mayor que este tamaño máximo, esa clave se trunca silenciosamente con ese tamaño máximo. Esto produce dos efectos:

  - En el caso de las entradas de un índice único, hará que las entradas que de otro modo serían únicas se declaren como duplicadas.

  - En el caso de las entradas de todos los índices, el truncamiento de claves hará que las entradas de índice que de lo contrario no coincidan con los criterios de búsqueda de una clave de búsqueda determinada se declaren como coincidencias.

Las aplicaciones deben prever este truncamiento y evitarlo o compensar sus efectos. En Windows Vista, se ha agregado una nueva marca de índice, JET_bitIndexDisallowTruncation, para facilitar a las aplicaciones evitar truncamientos de claves. Consulte la [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información sobre esta opción de indexación.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
