---
description: 'Más información sobre: JetGetTableColumnInfo (Función)'
title: JetGetTableColumnInfo (Función)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3940c07cc641d8c8d077c420f8c492ab5122b3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964235"
---
# <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo (Función)

La **función JetGetTableColumnInfo** recupera información sobre una columna de tabla.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla que contiene la columna para la que se va a capturar información.

*szColumnName*

Nombre de la columna para la que se va a capturar información.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo del búfer depende de *InfoLevel.* El autor de la llamada debe configurarse para alinear el búfer correctamente.

*cbMax*

Tamaño, en bytes, del búfer que se pasó en *pvResult*.

*InfoLevel*

Tipo de información que se recuperará para la columna especificada por *szColumnName*. El formato de los datos almacenados en *pvResult* depende de *InfoLevel*. Para obtener el esquema de la tabla temporal, [vea JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid ordenará la tabla temporal por *columnid*.

  - JET_ColInfoListCompact compactará la salida. Para obtener más información sobre la salida compacta, [vea JET_COLUMNLIST](./jet-columnlist-structure.md).

Se pueden establecer las siguientes opciones para este parámetro:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura se rellenan correctamente. JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> estructura. Esto es similar a una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Si se produce un error en esta función, la estructura contiene datos no definidos.</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">valor JET_COLUMNDEF</a>, salvo que <em>infoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal y se identifica mediante el <em>miembro tableid</em> <a href="gg269228(v=exchg.10).md">de JET_COLUMNLIST</a>. La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Si se produce un error en esta función, la estructura contiene datos no definidos.</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal y se identifica mediante el <em>miembro tableid</em> <a href="gg269228(v=exchg.10).md">de JET_COLUMNLIST</a>. La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Si se produce un error en esta función, la estructura contiene datos no definidos.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Igual que JET_ColInfoList, sin embargo, la tabla resultante se ordena por <em>columnid</em>, en lugar de por nombre de columna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor está en desuso y su uso devolverá JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Igual que JET_ColInfoBase, <em>pvResult</em> se interpreta como un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, salvo que <em>infoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> Está disponible en Windows Vista y versiones posteriores.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Solo se devuelven columnas no derivadas (si la tabla se deriva de una plantilla).</p><p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Solo devuelve el nombre de columna y el id. de columna de cada columna.</p><p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Ordenar la lista de columnas devueltas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</p><p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>infoLevel</em> base se JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La columna <em>denominada szColumnName</em> no se encontró en la tabla.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Se <em>especificó un infoLevel</em> no bueno.</p> | 
| <p>JET_errInvalidName</p> | <p>Este error se puede devolver si:</p><ul><li><p>Se ha dado un nombre no <em>bueno para szTableName.</em></p></li><li><p>Se ha dado un nombre no bueno <em>para szColumnName.</em></p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Este error se puede devolver si:</p><ul><li><p>Se <em>especificó un infoLevel</em> no bueno.</p></li><li><p>Se pasó <em>un valor NULL szTableName.</em></p></li><li><p>El búfer es demasiado pequeño.</p></li></ul> | 



#### <a name="remarks"></a>Observaciones

**Tanto JetGetTableColumnInfo** [como JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperan información sobre una columna. La diferencia entre ellos es cómo se identifica la tabla:

  - **JetGetTableColumnInfo** identifica una tabla por *tableid*.

  - [JetGetColumnInfo identifica](./jetgetcolumninfo-function.md) una tabla mediante la combinación *dbid* y *szTableName.*

Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal. La tabla temporal contiene datos y la [estructura JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para recorrer la tabla temporal. La tabla temporal debe cerrarse [con JetCloseTable.](./jetclosetable-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetTableColumnInfoW</strong> (Unicode) y <strong>JetGetTableColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Errores extensibles Storage motor de instalación](./extensible-storage-engine-errors.md)  
[Parámetros de control de errores](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
