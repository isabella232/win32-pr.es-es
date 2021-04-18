---
description: 'Más información acerca de: JetGetDatabaseFileInfo (función)'
title: JetGetDatabaseFileInfo función)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659991"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo función)

La función **JetGetDatabaseFileInfo** Recupera varios tipos de información sobre la base de datos. Se puede llamar a esta API mientras una base de datos está conectada o en línea (con [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) o mientras la base de datos o el motor de base de datos está sin conexión (con **JetGetDatabaseFileInfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*szDatabaseName*

Ruta de acceso de la base de datos de la que se va a recuperar la información.

*pvResult*

Puntero a un búfer que recibirá la información especificada. El tamaño del búfer, en bytes, se pasa en *cbMax*.

Si se produce un error en esta función, el contenido de *pvResult* no está definido.

La información almacenada en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

*InfoLevel* especifica qué tipo de información se debe recuperar en la base de datos especificada. Afecta al modo en que se interpreta *pvResult* . Algunos objetos *InfoLevel* solo están disponibles en la versión sin conexión (**JetGetDatabaseFileInfo**) o en línea ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) de la API.

Si el búfer de *pvResult* proporcionado es demasiado pequeño, se devolverá JET_errInvalidBufferSize o JET_errBufferTooSmall, en función de *InfoLevel*.

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
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> se interpretará como QWord (8 bytes). Devuelve el tamaño de la base de datos en bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> se interpretará como un <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. La estructura de <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> se rellenará con información relativa a la base de datos especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> se interpretará como un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La estructura de <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> se rellenará con información relativa a la base de datos especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> se interpretará como un booleano (4 bytes). Esto devolverá si el motor de base de datos tiene actualmente cualquier base de datos abierta o adjunta.</p>
<p><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> se interpretará como una longitud sin signo. Esto devolverá el tamaño de página de la base de datos en bytes.</p>
<p><strong>Windows XP:  </strong> Este valor se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Estos <em>InfoLevels</em> aún no se admiten y devuelven valores predeterminados. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Estos <em>InfoLevels</em> aún no se admiten y devuelven valores predeterminados. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Igual que JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Estos <em>InfoLevels</em> están desusados y no se admiten actualmente. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Igual que JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:  </strong> Este valor de <em>InfoLevel</em> se introduce en Windows Vista.</p>
<p><em>pvResult</em> se tratará como un puntero a un valor DWORD. Devuelve un valor de enumeración, que indica el tipo de archivo que el motor considera que es. Los tipos de archivo se muestran en la tabla siguiente. Para obtener más información sobre estos tipos de archivos y su uso en el motor de, consulte <a href="gg294069(v=exchg.10).md">archivos del motor de almacenamiento extensible</a>.</p>
<div class="tableSection">
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
<td><p>JET_filetypeUnknown</p></td>
<td><p>El tipo de archivo es desconocido o no es un tipo de archivo ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>El archivo es un archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>El archivo es un archivo de registro de transacciones.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>El archivo es un archivo de punto de comprobación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>El archivo es un archivo de base de datos temporal.</p></td>
</tr>
</tbody>
</table>

</div></td>
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>La <em>InfoLevel</em> solicitada se JET_DbInfoIsam. Esto no se admite.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>El búfer que se proporciona en <em>cbMax</em> es demasiado pequeño para la información deseada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>El búfer que se proporciona en <em>cbMax</em> no es el tamaño correcto para la información deseada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado. <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> devolverá este error cuando el DBID proporcionado no sea una base de datos válida (adjunta). Este error lo devolverá <strong>JetGetDatabaseFileInfo</strong> y <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> cuando una <em>InfoLevel</em> solicitada no sea compatible con esa versión de la función.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, los datos solicitados se devolverán en el búfer de salida.

Si se produce un error en esta función, el búfer de salida estará en un estado indefinido.

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
<td><p>Se implementa como <strong>JetGetDatabaseFileInfoW</strong> (Unicode) y <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
