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
ms.openlocfilehash: 2066e3d20ef98d71c4c891d941d322e993b309e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965539"
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

Puntero a un búfer que recibirá la información. El búfer debe alinearse para contener el tipo requerido. El tipo del búfer depende del *parámetro InfoLevel.*

*cbResult*

Tamaño, en bytes, del búfer pasado en el *parámetro pvResult.*

*InfoLevel*

Especifica qué información se almacenará en *pvResult*. Los valores válidos son:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta <a href="gg269185(v=exchg.10).md">correctamente, JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> se interpreta como un LCID. Si se ejecuta correctamente, el LCID contiene el identificador de configuración regional del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> estructura. Si se ejecuta <a href="gg269185(v=exchg.10).md">correctamente, JET_INDEXLIST</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC está obsoleto.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC está obsoleto.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, ULONG contiene el uso de espacio del índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor está obsoleto.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid está en desuso. Use JET_IdxInfoLCID en su lugar y la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> en su lugar.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> se interpreta como ULONG. Si se ejecuta correctamente, el ULONG contiene el recuento de índices en la tabla especificada. <em>szIndexName</em> se omite. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor <em>de cbVarSegMac</em> usado cuando se creó el índice. Consulte <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> para obtener una descripción de <em>cbVarSegMac</em>. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> se interpreta como una <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. Si se ejecuta <a href="gg269327(v=exchg.10).md">correctamente, JET_INDEXID</a> estructura recibe información sobre el índice. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> se interpreta como USHORT. Si se ejecuta correctamente, USHORT contiene el valor de cbKeyMost usado cuando se creó el índice. Consulte la <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> estructura para obtener una descripción de cbKeyMost. En caso de error, el contenido <em>de pvBuffer</em> no está definido.</p> | 
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

[JetGetIndexInfo](./jetgetindexinfo-function.md) y **JetGetTableIndexInfo recuperan** información idéntica sobre un índice. La diferencia radica en cómo se especifica la tabla. [JetGetIndexInfo espera](./jetgetindexinfo-function.md) una base de datos (*dbid*) y el nombre de una tabla (*szTableName*), mientras **que JetGetTableIndexInfo** espera un identificador de tabla (*tableid*).

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetGetTableIndexInfoW</strong> (Unicode) y <strong>JetGetTableIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)
