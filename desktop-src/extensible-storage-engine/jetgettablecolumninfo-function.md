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
ms.openlocfilehash: 63e913e68a3aea8f220c713b07becdeecb785a619b73a833bb6a0e9c3c1d37a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979034"
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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ColInfo</p></td>
<td><p><em>pvResult</em> se interpreta como una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura se rellenan correctamente. JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> se interpreta como una <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> estructura. Esto es similar a una <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Si se produce un error en esta función, la estructura contiene datos no definidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">valor JET_COLUMNDEF</a>, salvo que <em>infoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo y JET_ColInfoByColid recuperan la misma información.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> se interpreta como una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal y se identifica mediante el <em>miembro tableid</em> <a href="gg269228(v=exchg.10).md">de JET_COLUMNLIST</a>. La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Si se produce un error en esta función, la estructura contiene datos no definidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>pvResult</em> se interpreta como una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> estructura. Si esta función se realiza correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal y se identifica mediante el <em>miembro tableid</em> <a href="gg269228(v=exchg.10).md">de JET_COLUMNLIST</a>. La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Si se produce un error en esta función, la estructura contiene datos no definidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Igual que JET_ColInfoList, sin embargo, la tabla resultante se ordena por <em>columnid</em>, en lugar de por nombre de columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor está en desuso y su uso devolverá JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Igual que JET_ColInfoBase, <em>pvResult</em> se interpreta como un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, salvo que <em>infoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista:</strong> Está disponible en Windows Vista y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Solo se devuelven columnas no derivadas (si la tabla se deriva de una plantilla).</p>
<p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>InfoLevel</em> base se JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Solo devuelve el nombre de columna y el id. de columna de cada columna.</p>
<p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>InfoLevel</em> base se JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Ordenar la lista de columnas devueltas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</p>
<p>Este valor puede estar lógicamente o en <em>infoLevel</em>, cuando el <em>InfoLevel</em> base se JET_ColInfoList.</p>
<p><strong>Windows Vista:</strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>JET_errColumnNotFound</p></td>
<td><p>La columna <em>denominada szColumnName</em> no se encontró en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Se <em>especificó un infoLevel</em> no bueno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Este error se puede devolver si:</p>
<ul>
<li><p>Se ha dado un nombre no <em>bueno para szTableName.</em></p></li>
<li><p>Se ha dado un nombre no bueno <em>para szColumnName.</em></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Este error se puede devolver si:</p>
<ul>
<li><p>Se <em>especificó un infoLevel</em> no bueno.</p></li>
<li><p>Se pasó <em>un valor NULL szTableName.</em></p></li>
<li><p>El búfer es demasiado pequeño.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentarios

**Tanto JetGetTableColumnInfo** [como JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperan información sobre una columna. La diferencia entre ellos es cómo se identifica la tabla:

  - **JetGetTableColumnInfo** identifica una tabla por *tableid*.

  - [JetGetColumnInfo identifica](./jetgetcolumninfo-function.md) una tabla mediante la combinación *dbid* y *szTableName.*

Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal. La tabla temporal contiene datos y la [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para recorrer la tabla temporal. La tabla temporal debe cerrarse [con JetCloseTable.](./jetclosetable-function.md)

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
<td><p><strong>Servidor</strong></p></td>
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
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetTableColumnInfoW</strong> (Unicode) y <strong>JetGetTableColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
