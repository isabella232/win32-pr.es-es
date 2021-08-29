---
description: 'Más información sobre: JetGetTableIndexInfo (Función)'
title: Función JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cde923ea822ed3bf62dcb5e7cdc65447ce60347
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477561"
---
# <a name="jetgettableindexinfo-function"></a>Función JetGetTableIndexInfo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgettableindexinfo-function"></a>Función JetGetTableIndexInfo

La **función JetGetTableIndexInfo** recupera información sobre un índice.

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*tableid*

Tabla de base de datos que contiene el índice que contiene la información necesaria.

*szIndexName*

Nombre del índice que contiene información que se recuperará.

*pvResult*

Puntero a un búfer que recibirá la información. El búfer debe estar alineado para contener el tipo necesario. El tipo del búfer depende del *parámetro InfoLevel.*

*cbResult*

Tamaño, en bytes, del búfer pasado en el *parámetro pvResult.*

*InfoLevel*

Especifica qué información se almacenará en *pvResult.* Los valores válidos son:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta correctamente, <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> se interpreta como un LCID. Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta correctamente, <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC está obsoleto.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC está obsoleto.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor está obsoleto.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid está en desuso. Use JET_IdxInfoLCID en su lugar, y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> en su lugar.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, el ULONG contiene el recuento de índices de la tabla especificada. <em>szIndexName</em> se omite. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor de <em>cbVarSegMac</em> usado cuando se creó el índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> se interpreta como un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Si se ejecuta correctamente, <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor de cbKeyMost usado cuando se creó el índice. Vea la <a href="gg269186(v=exchg.10).md">estructura JET_INDEXCREATE</a> para obtener una descripción de cbKeyMost. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex se introdujo en Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult</em> se interpreta como una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> estructura. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 se introdujo en Windows 7.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errIndexNotFound</p> | <p>No se encuentra el índice especificado en la tabla especificada.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>El búfer pasado como <em>pvResult</em> era demasiado pequeño. El contenido del búfer no está definido.</p> | 



#### <a name="remarks"></a>Comentarios

[JetGetIndexInfo](./jetgetindexinfo-function.md) y **JetGetTableIndexInfo** recuperan información idéntica sobre un índice. La diferencia radica en cómo se especifica la tabla. [JetGetIndexInfo](./jetgetindexinfo-function.md) espera una base de datos (*dbid*) y el nombre de una tabla (*szTableName*), mientras **que JetGetTableIndexInfo** espera un identificador de tabla (*tableid*).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetTableIndexInfoW</strong> (Unicode) y <strong>JetGetTableIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)
