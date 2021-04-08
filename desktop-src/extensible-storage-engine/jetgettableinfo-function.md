---
description: 'Más información acerca de: JetGetTableInfo (función)'
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
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002894"
---
# <a name="jetgettableinfo-function"></a>Función JetGetTableInfo


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>Función JetGetTableInfo

La función **JetGetTableInfo** Recupera varios fragmentos de información sobre una tabla de una base de datos.

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

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Tabla a la que se aplica la información.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo de búfer depende de *InfoLevel*. Es responsabilidad del autor de la llamada alinear el búfer adecuadamente.

*cbMax*

Tamaño, en bytes, del búfer que se pasó en *pvResult*.

*InfoLevel*

El tipo de información que se recuperará para la tabla especificada por *TABLEID*. El formato de los datos que se almacenan en *pvResult* depende de *InfoLevel*.

Se pueden establecer las siguientes opciones para este parámetro:

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
<td><p>JET_TblInfo</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Si el método se ejecuta correctamente, la estructura de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> se rellena con los datos adecuados. Si se produce un error, el contenido es indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>pvResult</em> se trata como una matriz de dos objetos <a href="gg269248(v=exchg.10).md">JET_DBID</a> . El identificador de la base de datos que posee la tabla se almacena dos veces en esta matriz.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable está en desuso. La API devolverá JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName recupera el nombre de la tabla y la almacena en <em>pvResult</em>. Si el búfer es demasiado pequeño, el comportamiento es indefinido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany recupera el nombre de la tabla y la almacena en <em>pvResult</em>. Si el búfer es demasiado pequeño, el comportamiento es indefinido.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC está en desuso. La API devolverá JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt está en desuso. La API devolverá JET_errQueryNotSupported.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC está en desuso. La API devolverá JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> se interpreta como una matriz de dos ULONGs:</p>
<ul>
<li><p>El primer <strong>ULong</strong> es el número de páginas de la tabla.</p></li>
<li><p>El segundo <strong>ULong</strong> es la densidad de destino de las páginas de la tabla.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> se interpreta como <strong>ULong</strong>. <strong>ULong</strong> es la suma del número de páginas que están disponibles en la tabla, sus índices y el árbol de valores largos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> se interpreta como <strong>ULong</strong>. <strong>ULong</strong> es la suma del número de páginas que pertenecen a la tabla (incluidos sus índices y el árbol de valores largos y las páginas disponibles).</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>El comportamiento de la API depende del tamaño del búfer que se pasa a la API. Dos valores de <em>cbMax</em> deben ser al menos (2 * SIZEOF (ulong)).</p>
<ul>
<li><p>Si <em>cbMax</em> es (2 * SIZEOF (ulong)), <em>pvResult</em> se interpreta como una matriz de dos ULONGs:</p>
<ul>
<li><p>El primer <strong>ULong</strong> es el número de extensiones de propiedad de la tabla.</p></li>
<li><p>El segundo <strong>ULong</strong> es el número de extensiones disponibles de la tabla.</p></li>
</ul></li>
<li><p><em>pvResult</em> se interpreta como una matriz de:</p>
<ul>
<li><p>El primer <strong>ULong</strong> es el número de extensiones de propiedad de la tabla.</p></li>
<li><p>El segundo <strong>ULong</strong> es el número de extensiones disponibles de la tabla.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>pvResult</em> se interpreta como un búfer de cadena. El búfer debe ser al menos JET_cbNameMost + 1, incluido el carácter <strong>nulo</strong>final. Si la tabla es una tabla derivada, el búfer se rellenará con el nombre de la tabla de la que la tabla derivada heredó su DDL. Si la tabla no es una tabla derivada, el búfer será una cadena vacía.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>El búfer era demasiado pequeño.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Se ha especificado un <em>InfoLevel</em> en desuso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>El tamaño del búfer no era el correcto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La tabla que se pasó era una tabla temporal y el <em>InfoLevel</em> solicitado no se puede recuperar para una tabla temporal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p>No se admite <em>InfoLevel</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Otra operación de base de datos está utilizando la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La tabla está bloqueada por otra operación de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>El sistema utiliza la tabla. Esta advertencia no es grave.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Algunas partes de la información no son válidas para las tablas temporales (vea [JetOpenTempTable](./jetopentemptable-function.md)).

Las estadísticas de tabla incluyen el número de registros y el número de páginas del índice clúster (es decir, el índice que contiene los datos del registro). Se tiene acceso a las estadísticas de índice por separado por nombre, mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetTableInfoW</strong> (Unicode) y <strong>JetGetTableInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
