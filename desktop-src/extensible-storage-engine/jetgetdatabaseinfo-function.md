---
description: 'Más información sobre: JetGetDatabaseInfo (Función)'
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
ms.openlocfilehash: c92ed1d5d42511971c53e6116574cd8d9a882124
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982578"
---
# <a name="jetgetdatabaseinfo-function"></a>Función JetGetDatabaseInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetdatabaseinfo-function"></a>Función JetGetDatabaseInfo

La **función JetGetDatabaseInfo** recupera varios tipos de información sobre la base de datos. Se puede llamar a esta API mientras una base de datos está adjunta o en línea (con **JetGetDatabaseInfo)** o mientras la base de datos o el motor de base de datos están sin conexión (con [JetGetDatabaseFileInfo).](./jetgetdatabasefileinfo-function.md)

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

*Dbid*

La [JET_DBID](./jet-dbid.md) de la base de datos de la que se recuperará la información.

*pvResult*

Puntero a un búfer que recibirá la información especificada. El tamaño del búfer, en bytes, se pasa *en cbMax*.

En caso de error, el *contenido de pvResult* no está definido.

La información almacenada en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer que se pasó en *pvResult*.

*InfoLevel*

*InfoLevel* especifica qué tipo de información se debe recuperar sobre la base de datos especificada. Afecta a cómo *se interpreta pvResult.* Algunos *InfoLevel solo* están disponibles en la versión sin conexión ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o en línea **(JetGetDatabaseInfo)** de la API.

Si el *búfer pvResult* proporcionado es demasiado pequeño, JET_errInvalidBufferSize o JET_errBufferTooSmall se devolverán en función de *InfoLevel*.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>Aún no se admite y devuelve los valores predeterminados. No debe usarse.</p> | 
| <p>JET_DbInfoConnect</p> | <p>Estos <em>InfoLevels están</em> en desuso y no se admiten actualmente. No debe usarse.</p> | 
| <p>JET_DbInfoCountry</p> | <p>Aún no se admite y devuelve los valores predeterminados. No debe usarse.</p> | 
| <p>JET_DbInfoCp</p> | <p>Aún no se admite y devuelve los valores predeterminados. No debe usarse.</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> se interpretará como un búfer de cadena (char *). Se MAX_PATH un búfer de carga, pero no es necesario. Si el búfer no es lo suficientemente largo, JET_errBufferTooSmall se devolverá. La cadena se rellenará con la ruta de acceso de la base de datos para este DBID.</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> se interpretará como DWORD (4 bytes). Devuelve el tamaño de la base de datos en páginas.</p> | 
| <p>JET_DbInfoIsam</p> | <p>Estos <em>InfoLevels están</em> en desuso y no se admiten actualmente. No debe usarse.</p> | 
| <p>JET_DbInfoLCID</p> | <p>(Windows XP y versiones posteriores) Este <em>InfoLevel</em> se especificó originalmente como: JET_DbInfoLangid (Windows 2000)</p><p><em>pvResult</em> se interpretará como un valor long. Esto devuelve el identificador de configuración regional (LCID) asociado a esta base de datos.</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> se interpretará como un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> estructura se rellenará con información relativa a la base de datos especificada.</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> se interpretará como un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Esto devuelve si la base de datos se abre en modo exclusivo. Si la base de datos está en modo <a href="gg294066(v=exchg.10).md"></a> JET_bitDbExclusive se establecerá en el JET_GRBIT proporcionado, de lo contrario, se establece cero. Tenga en cuenta que no <em>se devuelven</em> otras opciones de bits grbit de base de datos para <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> y <a href="gg269299(v=exchg.10).md">JetOpenDatabase.</a></p> | 
| <p>JET_DbInfoPageSize</p> | <p>Solo está disponible en Windows XP y versiones posteriores. <em>pvResult</em> se interpretará como unsigned long. Esto devolverá el tamaño de página de la base de datos en bytes.</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> se interpretará como DWORD. Esto devuelve el espacio disponible para la base de datos en páginas.</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> se interpretará como DWORD. Esto devuelve el espacio de propiedad de la base de datos en páginas.</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> se interpretará como un valor long. Esto devolverá un valor mayor que el nivel máximo en el que se pueden anidar las transacciones. Si se llama a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (de forma anidada, es decir, en la misma sesión, sin confirmación o reversión) tantas veces como este valor, en la última llamada JET_errTransTooDeep se devolverá <a href="gg294083(v=exchg.10).md">desde JetBeginTransaction</a>. Tenga en cuenta que el Windows 2000, Windows XP y Windows Server 2003 es 7.</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> se interpretará como un valor long. Esto devuelve la versión principal nativa del motor de base de datos. Este valor se 0x620 para Windows 2000, Windows XP y Windows Server 2003.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>El tamaño del búfer especificado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Se <em>solicitó InfoLevel</em> JET_DbInfoIsam. Esto no se admite.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>El tamaño del búfer especificado en <em>cbMax</em> era demasiado pequeño (o no correcto) para contener la información deseada.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. <strong>JetGetDatabaseInfo</strong> devolverá este error cuando <a href="gg269248(v=exchg.10).md"></a> el JET_DBID proporcionado no sea una base de datos válida (adjunta). Este error lo <a href="gg269239(v=exchg.10).md">devolverán JetGetDatabaseFileInfo</a> y <strong>JetGetDatabaseInfo</strong> cuando una <em>clase InfoLevel</em> solicitada no sea compatible con esa versión de la función.</p> | 



Si se ejecuta correctamente, los datos solicitados se devolverán en el búfer de salida.

En caso de error, el búfer de salida estará en un estado indefinido.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetDatabaseInfoW</strong> (Unicode) y <strong>JetGetDatabaseInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
