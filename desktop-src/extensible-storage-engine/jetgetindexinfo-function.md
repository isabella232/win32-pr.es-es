---
description: 'Más información acerca de: JetGetIndexInfo (función)'
title: Función JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648519"
---
# <a name="jetgetindexinfo-function"></a>Función JetGetIndexInfo


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>Función JetGetIndexInfo

La función **JetGetIndexInfo** recupera información acerca de un índice.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*DBID*

Identificador de base de datos que se va a usar para la llamada API.

*szTableName*

Nombre de la tabla que contiene el índice con la información que se va a recuperar.

*szIndexName*

Nombre del índice con la información que se va a recuperar.

*pvResult*

Puntero a un búfer que recibirá la información deseada. El búfer debe estar alineado para contener el tipo necesario. El tipo de búfer depende del parámetro *InfoLevel* .

*cbResult*

Tamaño, en bytes, del búfer pasado como *pvResult*.

*InfoLevel*

La información que se almacenará en *pvResult*. Se pueden usar las siguientes opciones para este parámetro.

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvResult</em> se interpreta como ulong. Si se ejecuta correctamente, ULONG contiene el recuento de índices de la tabla especificada. <em>szIndexName</em> se omite. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvResult</em> se interpreta como <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Si se ejecuta correctamente, la estructura de <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> recibe información sobre el índice. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid está en desuso. En su lugar, use JET_IdxInfoLCID y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvResult</em> se interpreta como un LCID. Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p>
<p><strong>Windows XP:  </strong> JET_IdxInfoLCID se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . Si se ejecuta correctamente, la estructura de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> recibe información sobre el índice. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC está obsoleto.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC está obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> se interpreta como ulong. Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor está obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvResult</em> se interpreta como un USHORT. Si se ejecuta correctamente, USHORT contiene el valor de <em>cbVarSegMac</em> que se usa cuando se creó el índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvResult</em> se interpreta como un USHORT. Si se ejecuta correctamente, USHORT contiene el valor de <em>cbKeyMost</em> que se usa cuando se creó el índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbKeyMost</em>. En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p>
<p><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost se introduce en Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex se presenta en Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . En caso de error, el contenido de <em>pvBuffer</em> no está definido.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 se presenta en Windows 7.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>No se encuentra el índice especificado en la tabla especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>El búfer pasado como <em>pvResult</em> era demasiado pequeño. El contenido del búfer no está definido.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

**JetGetIndexInfo** y [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperan la misma información sobre un índice. La diferencia radica en cómo se especifica la tabla. **JetGetIndexInfo** espera una base de datos (*DBID*) y el nombre de una tabla (*SzTableName*), mientras que [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera un identificador de tabla (*TABLEID*).

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
<td><p>Se implementa como <strong>JetGetIndexInfoW</strong> (Unicode) y <strong>JetGetIndexInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
