---
description: 'Más información acerca de: estructura de JET_OPENTEMPORARYTABLE'
title: Estructura de JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360770"
---
# <a name="jet_opentemporarytable-structure"></a>Estructura de JET_OPENTEMPORARYTABLE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>Estructura de JET_OPENTEMPORARYTABLE

La estructura **JET_OPENTEMPORARYTABLE** contiene una colección fácilmente extensible de parámetros para la función **JET_OPENTEMPORARYTABLE** . Esta estructura es la tabla temporal equivalente a la estructura [JET_TABLECREATE](./jet-tablecreate-structure.md) .

**Windows Vista:** La estructura de **JET_OPENTEMPORARYTABLE** se introduce en Windows Vista.

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de esta estructura en bytes (para una futura ampliación). Debe establecerse en sizeof (JET_TABLECREATE) en bytes.

**prgcolumndef**

Definiciones de columna para las columnas creadas en la tabla temporal.

Existen limitaciones **importantes** para las opciones de definición de columna que se utilizan con una tabla temporal. Vea la sección Comentarios para obtener más información.

Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las opciones siguientes que solo son relevantes en el contexto de una tabla temporal.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>El criterio de ordenación de la columna de clave para la tabla temporal debe ser descendente en lugar de ascendente. Si se especifica esta opción sin JET_bitColumnTTKey, se omite esta opción.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>La columna será una columna de clave para la tabla temporal.</p>
<p>El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más significativa, etc. Si se solicitan más columnas de clave de las que puede admitir el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</p></td>
</tr>
</tbody>
</table>


**ccolumn**

Vea *prgcolumndef*.

**pidxunicode**

El identificador de configuración regional y las marcas de normalización que se van a usar para comparar los datos de columna de clave Unicode en la tabla temporal.

Cuando este parámetro no está presente y cuando el parámetro *LCID* no está presente, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional en Inglés de EE. UU.

Cuando este parámetro no está presente, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal. Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.

**grbit**

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
<td><p>JET_bitTTIndexed</p></td>
<td><p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</p>
<p>Si esta funcionalidad no es necesaria, es mejor no solicitarlo. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUnique</p></td>
<td><p>Solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</p>
<p>Antes de Windows Server 2003, el motor de base de datos siempre asumió que esta opción está en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quita los duplicados cuando también se especifica la opción de JET_bitTTForwardOnly.</p>
<p>No es posible saber qué duplicado se realizará correctamente y qué duplicados se descartarán, en general. Sin embargo, cuando se solicita la opción de JET_bitTTErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre se realizará correctamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que se modifiquen posteriormente los registros que se han insertado previamente. Si esta funcionalidad no es necesaria, es mejor no solicitarlo.</p>
<p>Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se examinen en orden y dirección arbitrarios mediante <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Si no se necesita esta funcionalidad, es mejor no solicitarla. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Solicita que los valores de columna de clave <strong>null</strong> se ordenen más cerca del final del índice que los valores de columna de clave no NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Obliga al administrador de tablas temporal a abandonar la búsqueda de la mejor estrategia para usar la administración de la tabla temporal, lo que dará lugar a un rendimiento mejorado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Cualquier intento de insertar un registro con la misma clave de índice que un registro insertado anteriormente producirá un error inmediatamente con JET_errKeyDuplicate. Si no se solicita esta opción, se detectará un duplicado inmediatamente y se producirá un error, o se quitará de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal, en función de la funcionalidad solicitada.</p>
<p>Si esta funcionalidad no es necesaria, es mejor no solicitarlo. Si no se solicita esta funcionalidad, el administrador de tablas temporales puede elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>La tabla temporal solo se crea si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte JET_bitTTUnique para obtener más información.</p>
<p><strong>Windows Server 2003:  </strong> Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p></td>
</tr>
</tbody>
</table>


**prgcolumnid**

Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.

Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

**cbKeyMost**

Tamaño máximo de una clave que representa una fila determinada.

Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves. El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas.

Si este parámetro se establece en 0 o JET_cbKeyMostMin (255), el tamaño de clave máximo y su semántica serán idénticos al tamaño de clave máximo admitido por Windows Server 2003 y versiones anteriores. Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia (JET_paramDatabasePageSize). Consulte JET_paramKeyMost para obtener más información.

**cbVarSegMac**

La cantidad máxima de datos que se usarán de cualquier columna de longitud variable para construir una clave para una fila determinada.

Este parámetro se puede utilizar para controlar la cantidad de espacio de clave consumida por una columna de clave determinada. Este límite se encuentra en bytes. Si este parámetro es cero o es igual que el parámetro *cbKeyMost* , no se aplica ningún límite.

**TABLEID**

El identificador de la tabla temporal creada como resultado de una llamada correcta a [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md)
