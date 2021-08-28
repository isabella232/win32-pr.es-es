---
description: 'Más información sobre: JET_OPENTEMPORARYTABLE estructura'
title: JET_OPENTEMPORARYTABLE estructura
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
ms.openlocfilehash: 625de51bf265be02fa48beb2872797cd5bd6ba26
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986918"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE estructura

La **JET_OPENTEMPORARYTABLE** estructura contiene una colección fácilmente extensible de parámetros para **la JET_OPENTEMPORARYTABLE** función. Esta estructura es la tabla temporal equivalente a la [JET_TABLECREATE](./jet-tablecreate-structure.md) estructura.

**Windows Vista:** La **JET_OPENTEMPORARYTABLE** estructura se introduce en Windows Vista.

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

Tamaño de esta estructura en bytes (para futuras expansiones). Debe establecerse en sizeof( JET_TABLECREATE ) en bytes.

**prgcolumndef**

Definiciones de columna para las columnas creadas en la tabla temporal.

**Existen** limitaciones importantes para las opciones de definición de columna que se usan con una tabla temporal. Vea la sección Comentarios para obtener más información.

Además de las opciones de definición de columna habituales, también se pueden especificar cero o más de las siguientes opciones que solo son pertinentes en el contexto de una tabla temporal.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>El criterio de ordenación de la columna de clave de la tabla temporal debe ser descendente en lugar de ascendente. Si esta opción se especifica sin JET_bitColumnTTKey, se omite esta opción.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La columna será una columna de clave para la tabla temporal.</p><p>El orden de las definiciones de columna con esta opción especificada en la matriz de entrada determinará la prioridad de cada columna de clave para la tabla temporal. La primera definición de columna de la matriz que tiene esta opción establecida será la columna de clave más importante, y así sucesivamente. Si se solicitan más columnas de clave de las que puede ser compatibles con el motor de base de datos, esta opción se omite para las columnas de clave no admitidas.</p> | 



**ccolumn**

Vea *prgcolumndef*.

**pidxunicode**

El identificador de configuración regional y las marcas de normalización que se usarán para comparar los datos de las columnas de clave Unicode de la tabla temporal.

Cuando este parámetro no está presente y el parámetro *lcid* no está presente, se usará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal. El LCID predeterminado es la configuración regional del inglés de EE. UU.

Cuando este parámetro no está presente, se usarán las marcas de normalización predeterminadas para comparar los datos de las columnas de clave Unicode de la tabla temporal. Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.

**grbit**

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de <a href="gg294103(v=exchg.10).md">JetSeek</a> para buscar registros por clave de índice.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTUnique</p> | <p>Solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal.</p><p>Antes de Windows Server 2003, el motor de base de datos siempre supusía que esta opción estaba en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir de Windows Server 2003, ahora es posible crear una tabla temporal que no quite duplicados cuando también se especifique la opción JET_bitTTForwardOnly servidor.</p><p>No es posible saber qué duplicado se realizará correctamente y qué duplicados se descartarán, en general. Sin embargo, cuando JET_bitTTErrorOnDuplicateInsertion se solicita la opción , el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre se realizará correctamente.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros que se han insertado previamente se cambien posteriormente. Si esta funcionalidad no es necesaria, es mejor no solicitarla.</p><p>Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se digitalizarán en orden y dirección arbitrarios <a href="gg294117(v=exchg.10).md">mediante JetMove</a>.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Solicita que los <strong>valores de columna</strong> de clave NULL se ordenan más cerca del final del índice que los valores de columna de clave no NULL.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Obliga al administrador de tablas temporales a abandonar la búsqueda de la mejor estrategia para usar la administración de la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Cualquier intento de insertar un registro con la misma clave de índice que un registro insertado previamente producirá un error JET_errKeyDuplicate. Si no se solicita esta opción, se detecta inmediatamente un duplicado y se produce un error, o se quita de forma silenciosa más adelante, en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal, en función de la funcionalidad solicitada.</p><p>Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>La tabla temporal solo se crea si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impediría el uso de esta optimización, se producirá un error en la operación JET_errCannotMaterializeForwardOnlySort.</p><p>Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte JET_bitTTUnique para obtener más información.</p><p><strong>Windows Server 2003:</strong> Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</p> | 



**prgcolumnid**

Búfer de salida que recibe la matriz de id. de columna generados durante la creación de la tabla temporal.

Los id. de columna de esta matriz se corresponderán exactamente con la matriz de entrada de definiciones de columna. Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.

**cbKeyMost**

Tamaño máximo de una clave que representa una fila determinada.

El tamaño máximo de la clave se puede establecer para controlar cómo se truncan las claves. El truncamiento de claves es importante porque puede afectar cuando se considera que las filas son distintas.

Si este parámetro se establece en 0 o JET_cbKeyMostMin (255), el tamaño máximo de clave y su semántica permanecerán idénticos al tamaño máximo de clave admitido por Windows Server 2003 y versiones anteriores. Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia (JET_paramDatabasePageSize). Consulte JET_paramKeyMost para obtener más información.

**cbVarSegMac**

Cantidad máxima de datos que se usarán desde cualquier columna de longitud variable para construir una clave para una fila determinada.

Este parámetro se puede usar para controlar la cantidad de espacio de claves consumido por cualquier columna de clave determinada. Este límite está en bytes. Si este parámetro es cero o es el mismo que el *parámetro cbKeyMost,* no hay ningún límite en vigor.

**tableid**

Identificador de tabla para la tabla temporal creada como resultado de una llamada correcta a [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parámetros extensibles Storage del sistema del motor de base de datos](./extensible-storage-engine-system-parameters.md)
