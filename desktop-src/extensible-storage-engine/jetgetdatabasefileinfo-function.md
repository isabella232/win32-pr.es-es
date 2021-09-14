---
description: 'Más información sobre: JetGetDatabaseFileInfo (Función)'
title: JetGetDatabaseFileInfo (Función)
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
ms.openlocfilehash: b19d783480a8d82485bce32689b8d49e046b0285
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887292"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo (Función)

La **función JetGetDatabaseFileInfo** recupera varios tipos de información sobre la base de datos. Se puede llamar a esta API mientras una base de datos está adjunta o en línea (con [JetGetDatabaseInfo)](./jetgetdatabaseinfo-function.md)o mientras la base de datos o el motor de base de datos están sin conexión (con **JetGetDatabaseFileInfo).**

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

Puntero a un búfer que recibirá la información especificada. El tamaño del búfer, en bytes, se pasa *en cbMax*.

Si se produce un error en esta función, el contenido de *pvResult* no está definido.

La información almacenada en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

*InfoLevel* especifica qué tipo de información se debe recuperar sobre la base de datos especificada. Afecta a cómo *se interpreta pvResult.* Algunos *objetos InfoLevel* solo están disponibles en la versión sin conexión (**JetGetDatabaseFileInfo**) o en línea ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) de la API.

Si el *búfer pvResult* proporcionado es demasiado pequeño, JET_errInvalidBufferSize o JET_errBufferTooSmall se devolverán, dependiendo de *InfoLevel*.

<table>
<colgroup>
<col  />
<col  />
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
<td><p><em>pvResult</em> se interpretará como QWORD (8 bytes). Devuelve el tamaño de la base de datos en bytes.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> se interpretará como una <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. La <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> estructura se rellenará con información relativa a la base de datos especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> se interpretará como una <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> estructura se rellenará con información relativa a la base de datos especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> se interpretará como bool (4 bytes). Esto devolverá si el motor de base de datos tiene actualmente bases de datos abiertas o asociadas.</p>
<p><strong>Windows XP:</strong> Este valor se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> se interpretará como unsigned long. Esto devolverá el tamaño de página de la base de datos en bytes.</p>
<p><strong>Windows XP:</strong> Este valor se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Estos <em>InfoLevels aún</em> no se admiten y devuelven valores predeterminados. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Estos <em>InfoLevels aún</em> no se admiten y devuelven valores predeterminados. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Igual que JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Estos <em>InfoLevels están</em> en desuso y no se admiten actualmente. No use estos <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Igual que JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:</strong> Este <em>valor InfoLevel</em> se introduce en Windows Vista.</p>
<p><em>pvResult</em> se tratará como un puntero a un DWORD. Devuelve un valor de enumeración, que indica el tipo de archivo que el motor considera que es. Los tipos de archivo se enumeran en la tabla siguiente. Para obtener más información sobre estos tipos de archivos y su uso en el motor, vea <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</p>
<div class="tableSection">
<table>
<colgroup>
<col  />
<col  />
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

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores ese, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col  />
<col  />
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
<td><p>Se <em>solicitó InfoLevel</em> JET_DbInfoIsam. Esto no se admite.</p></td>
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
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado. <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> devolverá este error cuando el DBID proporcionado no sea una base de datos válida (adjunta). Este error lo <strong>devolverán JetGetDatabaseFileInfo</strong> y <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> cuando una <em>clase InfoLevel</em> solicitada no sea compatible con esa versión de la función.</p></td>
</tr>
</tbody>
</table>


Si esta función se realiza correctamente, los datos solicitados se devolverán en el búfer de salida.

Si se produce un error en esta función, el búfer de salida estará en un estado indefinido.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col  />
<col  />
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
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Archivo DLL</strong></p></td>
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
