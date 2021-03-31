---
description: 'Más información acerca de: JetGetDatabaseInfo (función)'
title: Función JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277102"
---
# <a name="jetgetdatabaseinfo-function"></a>Función JetGetDatabaseInfo


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>Función JetGetDatabaseInfo

La función **JetGetDatabaseInfo** Recupera varios tipos de información sobre la base de datos. Se puede llamar a esta API mientras una base de datos está conectada o en línea (con **JetGetDatabaseInfo**) o mientras la base de datos o el motor de base de datos está sin conexión (con [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*DBID*

[JET_DBID](./jet-dbid.md) de la base de datos de la que se va a recuperar la información.

*pvResult*

Puntero a un búfer que recibirá la información especificada. El tamaño del búfer, en bytes, se pasa en *cbMax*.

En caso de error, el contenido de *pvResult* no está definido.

La información almacenada en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer que se pasó en *pvResult*.

*InfoLevel*

*InfoLevel* especifica qué tipo de información se debe recuperar en la base de datos especificada. Afecta al modo en que se interpreta *pvResult* . Algunos *InfoLevel* solo están disponibles en la versión sin conexión ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o en línea (**JetGetDatabaseInfo**) de la API.

Si el búfer de *pvResult* proporcionado es demasiado pequeño, se devolverá JET_errInvalidBufferSize o JET_errBufferTooSmall en función de *InfoLevel*.

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
<td><p>JET_DbInfoCollate</p></td>
<td><p>Todavía no se admiten y devuelven valores predeterminados. No debe usarse.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Estos <em>InfoLevels</em> están desusados y no se admiten actualmente. No debe usarse.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Todavía no se admiten y devuelven valores predeterminados. No debe usarse.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Todavía no se admiten y devuelven valores predeterminados. No debe usarse.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFilename</p></td>
<td><p><em>pvResult</em> se interpretará como un búfer de cadena (Char *). No obstante, se sugiere un búfer de MAX_PATH. Si el búfer no es suficientemente largo, se devolverá JET_errBufferTooSmall. La cadena se rellenará con la ruta de acceso de la base de datos para este DBID.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> se interpretará como un valor DWORD (4 bytes). Devuelve el tamaño de la base de datos en páginas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Estos <em>InfoLevels</em> están desusados y no se admiten actualmente. No debe usarse.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoLCID</p></td>
<td><p>(Windows XP y versiones posteriores) Este <em>InfoLevel</em> se especificó originalmente como: JET_DbInfoLangid (Windows 2000)</p>
<p><em>pvResult</em> se interpretará como un valor Long. Esto devuelve el identificador de configuración regional (LCID) asociado a esta base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> se interpretará como un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La estructura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> se rellenará con información relativa a la base de datos especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoOptions</p></td>
<td><p><em>pvResult</em> se interpretará como un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Esto devuelve si la base de datos se abre en modo exclusivo. Si la base de datos está en modo exclusivo JET_bitDbExclusive se establecerá en el <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> proporcionado; de lo contrario, se establecerá cero. Tenga en cuenta que no se devuelven otras opciones de <em>grbit</em> de base de datos para <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> y <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p>Solo disponible en Windows XP y versiones posteriores. <em>pvResult</em> se interpretará como una longitud sin signo. Esto devolverá el tamaño de página de la base de datos en bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> se interpretará como un valor DWORD. Esto devuelve el espacio disponible para la base de datos en páginas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> se interpretará como un valor DWORD. Esto devuelve el espacio de propiedad de la base de datos en páginas.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoTransactions</p></td>
<td><p><em>pvResult</em> se interpretará como un valor Long. Esto devolverá un valor mayor que el nivel máximo en el que se pueden anidar las transacciones. Si se llama a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (en modo de anidamiento, es decir, en la misma sesión, sin commit o rollback) tantas veces como este valor, en la última llamada JET_errTransTooDeep se devolverá desde <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>. Tenga en cuenta que el valor de Windows 2000, Windows XP y Windows Server 2003 es 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoVersion</p></td>
<td><p><em>pvResult</em> se interpretará como un valor Long. Esto devuelve la versión principal nativa del motor de base de datos. Este valor es 0x620 para Windows 2000, Windows XP y Windows Server 2003.</p></td>
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
<td><p>El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>La <em>InfoLevel</em> solicitada se JET_DbInfoIsam. Esto no se admite.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>El tamaño del búfer proporcionado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. <strong>JetGetDatabaseInfo</strong> devolverá este error cuando el <a href="gg269248(v=exchg.10).md">JET_DBID</a> proporcionado no sea una base de datos válida (adjunta). Este error lo devolverá <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> y <strong>JetGetDatabaseInfo</strong> cuando una <em>InfoLevel</em> solicitada no sea compatible con esa versión de la función.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, los datos solicitados se devolverán en el búfer de salida.

En caso de error, el búfer de salida estará en un estado indefinido.

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
<td><p>Se implementa como <strong>JetGetDatabaseInfoW</strong> (Unicode) y <strong>JetGetDatabaseInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
