---
description: 'Más información sobre: JetDetachDatabase (Función)'
title: Función JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a66010b5d056301e368f7221380966adc2f31180
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470470"
---
# <a name="jetdetachdatabase-function"></a>Función JetDetachDatabase


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdetachdatabase-function"></a>Función JetDetachDatabase

La **función JetDetachDatabase** libera un archivo de base de datos que se adjuntaba previamente a una sesión de base de datos.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se desasoyera. Si *szFilename es* **NULL o** una cadena vacía, se desasociarán todas las bases de datos asociadas a *sesid.*

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Se está haciendo una copia de seguridad de la base de datos y no se puede desasociar.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>JetOpenDatabase ha abierto la base <a href="gg269299(v=exchg.10).md">de datos.</a> Las bases de datos deben cerrarse antes de separarse.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de datos no estaba adjuntada previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2).</a></p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó separar una base de datos mientras estaba en una transacción.</p> | 



#### <a name="remarks"></a>Comentarios

Si se abrió una base de datos adjunta (con [JetAttachDatabase),](./jetattachdatabase-function.md)debe cerrarse [con JetCloseDatabase antes](./jetclosedatabase-function.md) de separarla.

Windows 2000: las bases de datos que no se han desasociado antes de llamar a [JetTerm](./jetterm-function.md) se volverán a adjuntar automáticamente cuando se llame a [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetDetachDatabaseW</strong> (Unicode) y <strong>JetDetachDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
