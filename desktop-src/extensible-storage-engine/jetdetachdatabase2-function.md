---
description: 'Más información sobre: JetDetachDatabase2 (Función)'
title: Función JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984888"
---
# <a name="jetdetachdatabase2-function"></a>Función JetDetachDatabase2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetdetachdatabase2-function"></a>Función JetDetachDatabase2

La **función JetDetachDatabase2** libera un archivo de base de datos que se ha adjuntado previamente a una sesión de base de datos.

**Windows XP:****JetDetachDatabase2** se presenta en Windows XP.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se desasoyera. Si *szFilename es* **NULL o** una cadena vacía, se desasociarán todas las bases de datos asociadas a *sesid.*

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Fuerza el cierre y desasociación de la base de datos. Si JET_bitForceCloseAndDetach no se admite, JET_errForceDetachNotAllowed se devolverá.</p> | 
| <p>JET_bitForceDetach</p> | <p>Fuerza la desasociación de la base de datos. Si JET_bitForceDetach no se admite, JET_errForceDetachNotAllowed se devolverá.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Se está haciendo una copia de seguridad de la base de datos y no se puede desasociar.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>JetOpenDatabase ha abierto la base <a href="gg269299(v=exchg.10).md">de datos.</a> Las bases de datos deben cerrarse antes de separarse.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de datos no estaba adjuntada previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2).</a></p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach no se admite.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó separar una base de datos mientras se encontraba en una transacción.</p> | 



#### <a name="remarks"></a>Observaciones

Si se abrió una base de datos adjunta (con [JetAttachDatabase),](./jetattachdatabase-function.md)debe cerrarse [con JetCloseDatabase antes](./jetclosedatabase-function.md) de separarla.

Windows 2000 solo: las bases de datos que no se han desasociado antes de llamar a [JetTerm](./jetterm-function.md) se volverán a adjuntar automáticamente cuando se llame a [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetDetachDatabase2W</strong> (Unicode) y <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
