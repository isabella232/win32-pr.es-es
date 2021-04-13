---
description: 'Más información acerca de: JetMakeKey (función)'
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
ms.openlocfilehash: e3d121ed83f096baad249aab8677bb9f5e72e301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278657"
---
# <a name="jetmakekey-function"></a>Función JetMakeKey


_**Se aplica a:** Windows | Windows Server_

## <a name="jetmakekey-function"></a>Función JetMakeKey

La función **JetMakeKey** crea claves de búsqueda que, a continuación, se pueden usar para buscar un conjunto de entradas en un índice por algunos criterios de búsqueda simples en sus valores de columna de clave. Una clave de búsqueda también es una de las propiedades intrínsecas de un cursor y la usan las operaciones [JetSeek](./jetseek-function.md) y [JetSetIndexRange](./jetsetindexrange-function.md) para buscar entradas de índice que coincidan con estos criterios de búsqueda en el índice actual del cursor. Una clave de búsqueda completa se crea en una serie de llamadas a **JetMakeKey** , donde cada llamada se usa para cargar el valor de columna para la columna de clave siguiente del índice actual de un cursor. También es posible cargar una clave de búsqueda construida previamente que se ha recuperado del cursor mediante [JetRetrieveKey](./jetretrievekey-function.md).

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

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvData*

Búfer de entrada que contiene los datos de columna de la columna de clave actual del índice actual del cursor para el que se está construyendo la tecla de búsqueda.

El tipo de datos de los datos de la columna en el búfer de entrada debe coincidir exactamente con el tipo de datos y otras propiedades de la definición de columna de la columna de clave actual. No se realiza ninguna conversión de tipos en los datos de la columna.

Si se especifica JET_bitNormalizedKey en el parámetro *grbit* , el búfer de entrada debe contener una clave de búsqueda construida previamente. Estas claves se obtienen mediante una llamada a [JetRetrieveKey](./jetretrievekey-function.md).

*cbData*

Tamaño en bytes de los datos de columna proporcionados en el búfer de entrada.

Si se especifica JET_bitNormalizedKey en el parámetro *grbit* , este es el tamaño de la clave de búsqueda proporcionada en el búfer de entrada.

Si el tamaño de los datos de la columna es cero, se omite el contenido del búfer de entrada. Si se especifica JET_bitKeyDataZeroLength en el parámetro *grbit* y la columna de clave actual del índice actual del cursor es una columna de longitud variable, se supone que los datos de la columna de entrada son un valor de longitud cero. De lo contrario, se supone que los datos de la columna de entrada son valores NULL.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitFullColumnEndLimit</p></td>
<td><p>La clave de búsqueda debe construirse de tal forma que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li>
<li><p>Los valores de columna necesarios para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe usarse al compilar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JETbitFullColumnStartLimit</p></td>
<td><p>La clave de búsqueda se debe construir de modo que las columnas de clave que se encuentran después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li>
<li><p>Los valores de columna necesarios para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe utilizarse al generar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al inicio de un índice. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice. El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitKeyDataZeroLength</p></td>
<td><p>Si el tamaño del búfer de entrada es cero y la columna de clave actual es una columna de longitud variable, esta opción indica que el búfer de entrada contiene un valor de longitud cero. De lo contrario, el tamaño del búfer de entrada cero indicaría un valor NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNewKey</p></td>
<td><p>Se debe crear una nueva clave de búsqueda. Se descarta cualquier clave de búsqueda existente previamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitNormalizedKey</p></td>
<td><p>Cuando se especifica esta opción, se omiten todas las demás opciones, se descarta cualquier clave de búsqueda existente y el contenido del búfer de entrada se carga como la nueva clave de búsqueda.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPartialColumnEndLimit</p></td>
<td><p>La clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li>
<li><p>Los valores de columna necesarios para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe usarse al compilar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Esta opción no se puede usar si la columna de clave actual no es una columna de texto o una columna binaria de variable. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p>
<p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitPartialColumnStartLimit</p></td>
<td><p>Esta opción indica que la clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que se encuentran después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li>
<li><p>Los valores de columna necesarios para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe utilizarse al generar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al inicio de un índice. El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice. El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Esta opción no se puede usar si la columna de clave actual no es una columna de texto o una columna binaria de variable. Se producirá un error en la operación con JET_errInvalidgrbit si se intenta.</p>
<p>Esta opción solo está disponible en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStrLimit</p></td>
<td><p>Esta opción indica que la clave de búsqueda debe construirse de tal forma que las columnas de clave que aparecen después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para esta columna de clave y todas las columnas de clave anteriores.</p></li>
<li><p>Los valores de columna necesarios para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe usarse al compilar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Cuando esta opción se especifica en combinación con JET_bitSubStrLimit y la columna de clave actual es una columna de texto, se omitirá esta opción. Este comportamiento está diseñado para permitir que se infiera el tipo de la columna de clave actual al compilar la clave de búsqueda.</p>
<p>Si desea compilar una clave de búsqueda similar para el inicio de un índice, se debe realizar una llamada similar a <strong>JetMakeKey</strong> para la última columna de clave que no sea un carácter comodín, pero sin opciones de comodín especificadas. La clave de búsqueda está entonces en un estado adecuado para su uso en una búsqueda de este tipo. Esto es análogo al uso de JET_bitFullColumnStartLimit, salvo que la clave de búsqueda no finaliza correctamente, ya que es después del uso de una opción de carácter comodín.</p>
<p>Esta opción está en desuso en Windows XP y versiones posteriores para abordar esta semántica complicada. En su lugar, se debe usar JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit, siempre que sea posible.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSubStrLimit</p></td>
<td><p>Esta opción indica que la clave de búsqueda debe construirse de tal forma que la columna de clave actual se considere un carácter comodín de prefijo y que las columnas de clave que se encuentran después de la columna de clave actual se consideren como caracteres comodín. Esto significa que la clave de búsqueda construida puede usarse para hacer coincidir las entradas de índice que tienen lo siguiente:</p>
<ul>
<li><p>Los valores de columna exactos proporcionados para todas las columnas de clave anteriores.</p></li>
<li><p>Los datos de la columna especificada como un prefijo de su valor de columna para la columna de clave actual.</p></li>
<li><p>Cualquier valor de columna para las columnas de clave subsiguientes.</p></li>
</ul>
<p>Esta opción debe usarse al compilar claves de búsqueda con caracteres comodín que se usarán para buscar entradas de índice más cercanas al final de un índice. El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice. El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</p>
<p>Cuando esta opción se especifica en combinación con JET_bitStrLimit y la columna de clave actual es una columna de texto, esta opción tendrá prioridad. Esta opción se omite cuando la columna de clave actual no es una columna de texto. Este comportamiento está diseñado para permitir que se infiera el tipo de la columna de clave actual al compilar la clave de búsqueda.</p>
<p>Si desea compilar una clave de búsqueda similar para el inicio de un índice, se debe realizar una llamada similar a <strong>JetMakeKey</strong> para la columna de clave que va a ser el carácter comodín de prefijo, pero con que no se ha especificado ninguna opción de comodín. La clave de búsqueda está entonces en un estado adecuado para su uso en una búsqueda de este tipo. Esto es análogo al uso de JET_bitPartialColumnStartLimit, salvo que la clave de búsqueda no finaliza correctamente, ya que es después del uso de una opción de carácter comodín.</p>
<p>Esta opción está en desuso en Windows XP y versiones posteriores para abordar esta semántica complicada. En su lugar, se debe usar JET_bitPartialColumnStartLimit y JET_bitPartialColumnEndLimit, cuando sea posible.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall</p></td>
<td><p>Los datos de columna proporcionados eran demasiado pequeños para compilar una clave válida para el índice actual porque dicho índice es un índice de tupla y el tamaño mínimo de la tupla era mayor que los datos de columna proporcionados. Vea <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obtener más información sobre los índices de tupla. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Los datos de columna proporcionados no coincidían con el tamaño requerido por la definición de columna. Esto puede ocurrir si el tipo de datos de la columna es intrínsecamente un tamaño determinado. Esto también puede ocurrir si el tipo de datos de la columna no es intrínsecamente un determinado tamaño, pero la definición de la columna declara que es de longitud fija. Una excepción a esto es que este error no se producirá cuando se proporcionen demasiados datos para una columna de texto de longitud fija, ya que los datos que faltan se rellenarán automáticamente con espacios. Una segunda excepción a esto es que este error no se producirá cuando se proporcionen demasiados datos para una columna binaria de longitud fija, ya que los datos que faltan se rellenarán automáticamente con ceros.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una de las opciones solicitadas no era válida, se usó de forma ilegal o no se implementó. Esto puede ocurrir para <strong>JetMakeKey</strong> cuando:</p>
<ul>
<li><p>Se especifican JET_bitPartialColumnStartLimit o JET_bitPartialColumnEndLimit y la columna de clave correspondiente no es una columna de texto y no es una columna binaria de longitud variable. Este caso solo se produce en Windows XP y versiones posteriores.</p></li>
<li><p>Se ha intentado utilizar más de una de las siguientes opciones juntas: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit. Este caso solo se produce en Windows XP y versiones posteriores.</p></li>
<li><p>Se realiza un intento de usar JET_bitStrLimit o JET_bitSubStrLimit cuando se usa una de las siguientes opciones: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit y JET_bitFullColumnEndLimit. Este caso solo se produce en Windows XP y versiones posteriores.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</p>
<p>Esto puede ocurrir para <strong>JetMakeKey</strong> cuando se especificó JET_bitNormalizedKey y el valor proporcionado en el búfer de entrada era demasiado grande para ser una clave de búsqueda válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade</p></td>
<td><p>Los datos de columna proporcionados a <strong>JetMakeKey</strong> se rechazaron porque ya se han proporcionado datos de columna para todas las columnas de clave del índice actual. Esto puede ocurrir de tres maneras. La primera manera es si se proporcionan datos de columna para cada columna de clave del índice actual. La segunda manera es si se han proporcionado datos de columna para al menos una columna de clave y se ha elegido una opción de carácter comodín para la última llamada. La tercera manera es si se ha proporcionado una clave de búsqueda construida previamente mediante JET_bitNormalizedKey, que cubre todas las columnas de clave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>No hay ninguna clave de búsqueda actual para el cursor. Esto ocurrirá para <strong>JetMakeKey</strong> si no se especifica JET_bitNewKey y no se ha construido una clave de búsqueda para este cursor mediante una llamada anterior a <strong>JetMakeKey</strong>. La clave de búsqueda se eliminará mediante una llamada anterior a cualquier API de navegación en el cursor que no sea <a href="gg294117(v=exchg.10).md">JetMove</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>No hay ningún índice actual para el cursor. Esto ocurrirá para <strong>JetMakeKey</strong> si el cursor está en el índice clúster de una tabla, no se ha definido un índice principal y no se ha especificado JET_bitNormalizedKey. No es posible crear una clave de búsqueda si el cursor se encuentra en un índice que no tiene ninguna columna de clave a menos que se proporcione una clave de búsqueda construida previamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se realiza correctamente, si no se especificaron JET_bitNormalizedKey y JET_bitNewKey, la clave de búsqueda se habrá creado mediante los criterios de búsqueda de una columna de clave más en el índice actual. Si no se especificó JET_bitNormalizedKey y se especificó JET_bitNewKey, se descartó cualquier clave de búsqueda existente y se habrá creado una nueva con los criterios de búsqueda de la primera columna de clave del índice actual. Si se especificó JET_bitNormalizedKey, se descartó cualquier clave de búsqueda existente y se cargó una nueva desde el búfer de entrada. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

En caso de error, si se especificó JET_bitNormalizedKey o JET_bitNewKey, el estado de la clave de búsqueda es indefinido. Si no se especificaron JET_bitNormalizedKey ni JET_bitNewKey, no se producirá ningún cambio en el estado de la clave de búsqueda. En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Las claves se deben tratar como fragmentos opacos de datos. No se realiza ningún intento de aprovechar la estructura interna de estos datos. Sin embargo, lo siguiente se conoce en todas las claves de ESENT:

  - Las claves se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice de origen en la tabla de las entradas del índice de origen.

  - No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.

  - Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista. En Windows Vista y versiones posteriores, las claves pueden ser más grandes. El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.

Las claves de búsqueda pueden tener un byte más largo si se utiliza una opción de carácter comodín. En ese caso, la clave de búsqueda será de hasta JET_cbLimitKeyMost (256) bytes para las versiones anteriores a Windows Vista y JET_paramKeyMost + 1 bytes para Windows Vista y versiones posteriores.

Hay una ramificación muy importante de este tamaño máximo de clave. Siempre que haya una entrada de índice que tenga valores de columna lo suficientemente grandes como para que se genere una clave para ese índice que, de otro modo, será mayor que este tamaño máximo, esa clave se truncará silenciosamente en ese tamaño máximo. Esto produce dos efectos:

  - En el caso de las entradas de un índice único, provocará que las entradas que de otro modo sean únicas se declaren como duplicados.

  - En el caso de las entradas de todos los índices, el truncamiento de claves hará que las entradas de índice que, de otro modo, no coincidan con los criterios de búsqueda de una clave de búsqueda determinada se declaren como coincidencias.

Las aplicaciones deben anticipar este truncamiento y evitarlo o compensar sus efectos. En Windows Vista, se ha agregado una nueva marca de índice, JET_bitIndexDisallowTruncation, para facilitar a las aplicaciones la prevención de truncamientos de claves. Consulte la estructura de [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información sobre esta opción de indización.

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
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
