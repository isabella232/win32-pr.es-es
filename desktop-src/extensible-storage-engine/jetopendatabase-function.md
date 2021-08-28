---
description: 'Más información sobre: JetOpenDatabase (Función)'
title: Función JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fc7f484921dab0967ea991ac4060e5af7d78ec0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988507"
---
# <a name="jetopendatabase-function"></a>Función JetOpenDatabase


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetopendatabase-function"></a>Función JetOpenDatabase

La **función JetOpenDatabase** abre una base de datos adjuntada previamente, mediante las funciones [JetAttachDatabase](./jetattachdatabase-function.md) o [JetAttachDatabase2,](./jetattachdatabase2-function.md) para su uso con una sesión de base de datos. Se puede llamar a esta función varias veces para la misma base de datos.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se abrirá.

*szConnect*

Reservado. Definición en NULL

*pdbid*

Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos. Si se produce un error en la llamada, el valor es indefinido.

*grbit*

Grupo de bits que especifican cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbExclusive</p> | <p>Permite que solo una sola sesión adjunte una base de datos. Normalmente, varias sesiones pueden abrir una base de datos.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impide modificaciones en la base de datos.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Se solicitó acceso exclusivo, pero no se pudo conceder.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Se ha especificado una ruta de acceso no válida <em>en szFilename</em>. <em>szFilename</em> debe ser distinto de NULL y hacer referencia a un archivo válido.</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Otra sesión ya ha abierto la base de datos exclusivamente (mediante JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de datos no se ha adjuntado previamente <a href="gg294074(v=exchg.10).md">(consulte JetAttachDatabase</a>).</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Se intentó abrir un archivo que no es un archivo de base de datos válido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Se intentó abrir más de una base de datos y JET_paramOneDatabasePerSession <a href="gg269337(v=exchg.10).md">se</a> estableció. Para obtener más información, vea <a href="gg294139(v=exchg.10).md">Parámetros del sistema</a>.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>El archivo se adjuntaba como de solo lectura, pero <strong>JetOpenDatabase</strong> no pasó JET_bitDbReadOnly. La base de datos sigue abierta con acceso de solo lectura.</p> | 



#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetOpenDatabaseW</strong> (Unicode) y <strong>JetOpenDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
