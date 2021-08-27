---
description: 'Más información sobre: JetGetObjectInfo (Función)'
title: Función JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e6317280c5e794e9809c15f47f01d55ffd48eeb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982428"
---
# <a name="jetgetobjectinfo-function"></a>Función JetGetObjectInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetobjectinfo-function"></a>Función JetGetObjectInfo

La **función JetGetObjectInfo** recupera información sobre los objetos de base de datos. Actualmente, solo se admiten tablas. [JetGetTableInfo](./jetgettableinfo-function.md) se puede usar para capturar más información que **JetGetObjectInfo**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará.

*Dbid*

Base de datos de la que se recupera la información.

*objtyp*

Objetos que contienen información que se va a recuperar. Actualmente, solo JET_objtypNil y JET_objtypTable, ambos se comportan de forma idéntica. Solo se recuperarán las tablas.

*szContainerName*

Este parámetro está reservado para uso futuro y pasa **NULL.** Nombre de los tipos de objetos sobre los que se va a recuperar información.

*szObjectName*

Nombre del objeto que contiene información que se debe recuperar. Cuando *InfoLevel* usa las JET_ObjInfoList o JET_ObjInfoListNoStats para recuperar una lista de todos los objetos, este valor debe ser **NULL** o una cadena vacía.

Actualmente solo se admiten nombres de tabla.

*pvResult*

Puntero a un búfer que recibe la información especificada.

El tamaño del búfer, en bytes, se pasa *en cbMax*. En caso de error, el *contenido de pvResult* no está definido.

La información almacenada en *pvResult* depende de *InfoLevel*.

*cbMax*

Tamaño, en bytes, del búfer pasado en *pvResult*.

*InfoLevel*

Especifica el tipo de información que se va a recuperar para el objeto especificado. Afecta a cómo *se interpreta pvResult.*

Las siguientes opciones están disponibles para establecer para este parámetro.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estructura.</p><p>La <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estructura se rellena con información relativa al objeto denominado <em>en szObjectName</em>.</p><p>Si el autor de la llamada no quiere saber el número de registros y páginas del objeto JET_ObjInfoNoStats, considere la posibilidad de usar un nivel de información, que podría ser más rápido, ya que no se incluyen las estadísticas.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> estructura. Se recupera información sobre todos los objetos. Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en <a href="gg269348(v=exchg.10).md">la JET_OBJECTLIST</a> datos. Para obtener más información, <a href="gg269348(v=exchg.10).md">vea JET_OBJECTLIST</a>. Si el autor de la llamada no quiere saber el número de registros y páginas del objeto, considere la posibilidad de usar JET_ObjInfoListNoStats, que podría ser más rápido.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>En desuso y no se admite actualmente.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> estructura. Se recupera información sobre todos los objetos. Se creará una tabla temporal y la información necesaria para recorrer la tabla temporal se describe en <a href="gg269348(v=exchg.10).md">la JET_OBJECTLIST</a> datos. Para obtener más información, <a href="gg269348(v=exchg.10).md">vea JET_OBJECTLIST</a>. JET_ObjInfoListNoStats es idéntico a JET_ObjInfoList, salvo que no se actualizarán las columnas que informan del número de registros (<em>columnidcRecord</em>) y páginas (<em>columnidcPage</em>).</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult</em> se interpreta como un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. El tamaño máximo del objeto está en páginas. Actualmente solo se devolverán tablas.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult</em> se interpreta como un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Solo se recuperará información sobre el objeto especificado en <em>szObjectName.</em></p><p>La <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> estructura se rellenará con información relativa al objeto denominado <em>en szObjectName</em>.</p><p>JET_ObjInfoNoStats es idéntico a JET_ObjInfo, salvo que los campos que informan del número de registros y páginas están establecidos en cero.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>En desuso y no se admite actualmente.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>En desuso y no se admite actualmente.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>En desuso y no se admite actualmente.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>El tamaño del búfer especificado en <em>cbMax</em> era demasiado pequeño para contener la información deseada.</p> | 
| <p>JET_errInvalidName</p> | <p>Se ha dado un nombre no válido <em>en szObjectName</em> o <em>szContainerName.</em></p> | 
| <p>JET_errInvalidParameter</p> | <p>Se ha dado un parámetro no válido. Es posible que se pasara un nivel no adecuado a <em>InfoLevel.</em></p> | 



#### <a name="remarks"></a>Observaciones

Si **JetGetObjectInfo** crea correctamente una tabla temporal (por ejemplo, JET_ObjInfoList o JET_ObjInfoNoStats), el autor de la llamada es responsable de cerrar la tabla temporal [con JetCloseTable](./jetclosetable-function.md).

**Actualmente, JetGetObjectInfo** solo admite la recuperación de información sobre tablas.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetObjectInfoW</strong> (Unicode) y <strong>JetGetObjectInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
