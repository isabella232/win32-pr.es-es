---
description: 'Más información sobre: JetGetIndexInfo (Función)'
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
ms.openlocfilehash: e4d7c835d5077d2bfee87025b202480a888de981
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988588"
---
# <a name="jetgetindexinfo-function"></a>Función JetGetIndexInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetindexinfo-function"></a>Función JetGetIndexInfo

La **función JetGetIndexInfo** recupera información sobre un índice.

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

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Identificador de base de datos que se usará para la llamada API.

*szTableName*

Nombre de la tabla que contiene el índice con la información que se debe recuperar.

*szIndexName*

Nombre del índice con la información que se recuperará.

*pvResult*

Puntero a un búfer que recibirá la información deseada. El búfer debe estar alineado para contener el tipo necesario. El tipo del búfer depende del *parámetro InfoLevel.*

*cbResult*

Tamaño, en bytes, del búfer pasado como *pvResult*.

*InfoLevel*

Información que se almacenará en *pvResult.* Se pueden usar las siguientes opciones para este parámetro.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta correctamente, <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, ULONG contiene el recuento de índices de la tabla especificada. <em>szIndexName</em> se omite. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> se interpreta como un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Si se ejecuta correctamente, <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid está en desuso. Use JET_IdxInfoLCID y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> en su lugar.</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> se interpreta como un LCID. Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows XP:</strong> JET_IdxInfoLCID se introduce en Windows XP.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta correctamente, <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC está obsoleto.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC está obsoleto.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor está obsoleto.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor de <em>cbVarSegMac</em> usado cuando se creó el índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor de <em>cbKeyMost</em> usado cuando se creó el índice. Vea <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbKeyMost</em>. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows Vista:</strong> JET_IdxInfoKeyMost se introdujo en Windows Vista.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex se introdujo en Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult</em> se interpreta como una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errIndexNotFound</p> | <p>No se encuentra el índice especificado en la tabla especificada.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>El búfer pasado como <em>pvResult</em> era demasiado pequeño. El contenido del búfer no está definido.</p> | 



#### <a name="remarks"></a>Observaciones

**JetGetIndexInfo** y [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperan información idéntica sobre un índice. La diferencia radica en cómo se especifica la tabla. **JetGetIndexInfo** espera una base de datos (*dbid*) y el nombre de una tabla (*szTableName*), mientras [que JetGetTableIndexInfo](./jetgettableindexinfo-function.md) espera un identificador de tabla (*tableid*).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetIndexInfoW</strong> (Unicode) y <strong>JetGetIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
