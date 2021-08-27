---
description: 'Más información sobre: JetGetColumnInfo (Función)'
title: Función JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97b6dfc76de520249880314ecd32769951c7b927
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479111"
---
# <a name="jetgetcolumninfo-function"></a>Función JetGetColumnInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetcolumninfo-function"></a>Función JetGetColumnInfo

La **función JetGetColumnInfo** recupera información sobre una columna.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Identifica, junto con *szTableName*, la tabla que contiene la columna de la que se recupera la información.

*szTableName*

Identifica, junto con *dbid*, la tabla que contiene la columna de la que se recupera la información.

*szColumnName*

Nombre de la columna para la que se captura la información.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo del búfer depende de *InfoLevel.* El autor de la llamada debe configurarse para alinear el búfer correctamente.

*cbMax*

Tamaño, en bytes, del búfer que se pasa en *pvResult*.

*InfoLevel*

Tipo de información que se va a recuperar para la columna especificada por *szColumnName*. El formato de los datos almacenados en *pvResult* depende de este parámetro. Para obtener el esquema de la tabla temporal, [vea JET_COLUMNLIST](./jet-columnlist-structure.md).

Estos *InfoLevels* se diferencian por:

  - JET_ColInfoListSortColumnid ordenará la tabla temporal por *columnid*.

  - JET_ColInfoListCompact compactará la salida. Para obtener más información sobre la salida compacta, [vea JET_COLUMNLIST](./jet-columnlist-structure.md).

Las siguientes opciones están disponibles para su uso con este parámetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo y JET_ColInfoByColid recuperan la misma información. <em>pvResult</em> se interpreta como una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura se rellenan correctamente.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> estructura. Esto es similar a una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Si se produce un error en esta función, la estructura contiene datos no definidos.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Al JET_ColInfo, <em>pvResult</em> se interpreta como <a href="gg294130(v=exchg.10).md">un JET_COLUMNDEF</a>, salvo que <em>infoLevel</em> indica que la columna solicitada<em>(szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal y se identifica mediante el <strong>miembro tableid</strong> de la <a href="gg269228(v=exchg.10).md">estructura JET_COLUMNLIST</a> datos. La tabla debe cerrarse <a href="gg294087(v=exchg.10).md">con JetCloseTable.</a> Si se produce un error en esta función, la estructura contiene datos no definidos.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>Igual que JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Igual que JET_ColInfoList; sin embargo, la tabla resultante se ordena por columnid, en lugar de por el nombre de columna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor está en desuso y su uso devolverá JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Al JET_ColInfoBase, <em>pvResult</em> se interpreta como <a href="gg269194(v=exchg.10).md">un JET_COLUMNBASE</a>, salvo que <em>infoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a <a href="gg294104(v=exchg.10).md">un JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Solo se devuelven columnas no derivadas (si la tabla se deriva de una plantilla).</p><p>Este valor puede estar lógicamente o en <em>InfoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Solo devuelve el nombre de columna y el id. de columna de cada columna.</p><p>Este valor puede estar lógicamente o en <em>InfoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Ordenar la lista de columnas devueltas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</p><p>Este valor puede estar lógicamente o en <em>InfoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna <em>denominada szColumnName</em> no se encontró en la tabla.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Se <em>especificó un infoLevel</em> no bueno.</p> | 
| <p>JET_errInvalidName</p> | <p>Este error se puede devolver si:</p><ul><li><p>Se ha dado un nombre no <em>bueno para szTableName.</em></p></li><li><p>Se ha dado un nombre no bueno <em>para szColumnName.</em></p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Este error se puede devolver si:</p><ul><li><p>Se <em>especificó un infoLevel</em> no bueno.</p></li><li><p>Se pasó <em>un valor NULL szTableName.</em></p></li><li><p>El búfer es demasiado pequeño.</p></li></ul> | 



#### <a name="remarks"></a>Comentarios

[Tanto JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) **como JetGetColumnInfo** recuperan información sobre una columna. La diferencia entre ellos es cómo se identifica la tabla:

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica una tabla por *tableid*.

  - **JetGetColumnInfo identifica** una tabla mediante la combinación *dbid* y *szTableName.*

Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal. La tabla temporal contiene datos y la [estructura JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para recorrer la tabla temporal. La tabla temporal debe cerrarse [con JetCloseTable.](./jetclosetable-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetColumnInfoW</strong> (Unicode) y <strong>JetGetColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
