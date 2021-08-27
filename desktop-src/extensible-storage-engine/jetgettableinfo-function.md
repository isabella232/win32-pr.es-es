---
description: 'Más información sobre: JetGetTableInfo (Función)'
title: Función JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465802"
---
# <a name="jetgettableinfo-function"></a>Función JetGetTableInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgettableinfo-function"></a>Función JetGetTableInfo

La **función JetGetTableInfo** recupera varios fragmentos de información sobre una tabla de una base de datos.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla a la que se aplica la información.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo del búfer depende de *InfoLevel.* Es responsabilidad del autor de la llamada alinear el búfer correctamente.

*cbMax*

Tamaño, en bytes, del búfer que se pasó en *pvResult*.

*InfoLevel*

Tipo de información que se recuperará para la tabla especificada por *tableid*. El formato de los datos almacenados en *pvResult* depende de *InfoLevel*.

Se pueden establecer las siguientes opciones para este parámetro:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estructura. Si el método se realiza correctamente, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estructura se rellena con los datos adecuados. Si se produce un error, el contenido no está definido.</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>pvResult</em> se trata como una matriz de dos <a href="gg269248(v=exchg.10).md">JET_DBID</a> objetos. El identificador de base de datos de la base de datos propietaria de la tabla se almacena en esta matriz dos veces.</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable está en desuso. La API devolverá JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName recupera el nombre de la tabla y la almacena en <em>pvResult</em>. Si el búfer es demasiado pequeño, el comportamiento no está definido.</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany recupera el nombre de la tabla y la almacena en <em>pvResult</em>. Si el búfer es demasiado pequeño, el comportamiento no está definido.</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC está en desuso. La API devolverá JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt está en desuso. La API devolverá JET_errQueryNotSupported.</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC está en desuso. La API devolverá JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>pvResult</em> se interpreta como una matriz de dos ULONG:</p><ul><li><p>El primer <strong>ULONG</strong> es el número de páginas de la tabla.</p></li><li><p>El segundo <strong>ULONG</strong> es la densidad de destino de las páginas de la tabla.</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>pvResult</em> se interpreta como <strong>ULONG.</strong> <strong>ULONG</strong> es la suma del número de páginas que están disponibles en la tabla, sus índices y el árbol de valores largos.</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>pvResult</em> se interpreta como <strong>ULONG.</strong> <strong>ULONG es</strong> la suma del número de páginas que pertenecen a la tabla (incluidos sus índices, y el árbol de valores largos y las páginas disponibles en ellas).</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>El comportamiento de la API depende del tamaño del búfer que se pasa a la API. Dos <em>valores cbMax</em> deben ser al menos ( 2 * sizeof( ULONG ) ).</p><ul><li><p>Si <em>cbMax</em> es ( 2 * sizeof( ULONG ) ), <em>pvResult</em> se interpreta como una matriz de dos ULONG:</p><ul><li><p>El primer <strong>ULONG</strong> es el número de extensiones de propiedad de la tabla.</p></li><li><p>El segundo <strong>ULONG</strong> es el número de extensiones disponibles de la tabla.</p></li></ul></li><li><p><em>pvResult</em> se interpreta como una matriz de:</p><ul><li><p>El primer <strong>ULONG</strong> es el número de extensiones de propiedad de la tabla.</p></li><li><p>El segundo <strong>ULONG</strong> es el número de extensiones disponibles de la tabla.</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>pvResult</em> se interpreta como un búfer de cadena. El búfer debe ser al menos JET_cbNameMost + 1, incluido el valor <strong>NULL final.</strong> Si la tabla es una tabla derivada, el búfer se rellenará con el nombre de la tabla de la que la tabla derivada heredó su DDL. Si la tabla no es una tabla derivada, el búfer tendrá una cadena vacía.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>El búfer era demasiado pequeño.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Se especificó <em>un InfoLevel</em> en desuso.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>El búfer no tenía el tamaño correcto.</p> | 
| <p>JET_errInvalidOperation</p> | <p>La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</p> | 
| <p>JET_errQueryNotSupported</p> | <p>No <em>se admite InfoLevel.</em></p> | 
| <p>JET_errTableInUse</p> | <p>Otra operación de base de datos está utilizando la tabla.</p> | 
| <p>JET_errTableLocked</p> | <p>Otra operación de base de datos bloquea la tabla.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>El sistema está utilizando la tabla. Esta advertencia no es importante.</p> | 



#### <a name="remarks"></a>Comentarios

Algunos fragmentos de información no son válidos para las tablas temporales (vea [JetOpenTempTable).](./jetopentemptable-function.md)

Las estadísticas de tabla incluyen el número de registros y el número de páginas del índice clúster (es decir, el índice que contiene los datos de registro). Se accede a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetTableInfoW</strong> (Unicode) y <strong>JetGetTableInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
