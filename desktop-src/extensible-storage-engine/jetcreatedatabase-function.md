---
description: 'Más información sobre: JetCreateDatabase (Función)'
title: Función JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 572684785139bd8cdcd0da391199bdf6b5cb0bd9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985078"
---
# <a name="jetcreatedatabase-function"></a>Función JetCreateDatabase


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase-function"></a>Función JetCreateDatabase

La **función JetCreateDatabase** crea y adjunta un archivo de base de datos que se usará con el motor de base de datos ese. Llamar [a JetCreateDatabase2](./jetcreatedatabase2-function.md) con *cpgDatabaseSizeMax* establecido en cero es idéntico a llamar a **JetCreateDatabase** con *szConnect* establecido en NULL. Actualmente, se pueden crear hasta siete bases de datos por instancia.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se va a crear.

*szConnect*

Reservado para uso futuro. Definición en NULL

*pdbid*

Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos. En caso de error, el valor es indefinido.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>De forma predeterminada, si se llama a <strong>JetCreateDatabase</strong> y la base de datos ya existe, se producirá un error en la llamada API y no se sobrescribirá la base de datos original. JET_bitDbOverwriteExisting este comportamiento y la base de datos antigua se sobrescribirá con una nueva. Windows XP y versiones posteriores.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff desactiva el registro. Al establecer este bit, se pierde la capacidad de reproducir archivos de registro y recuperar la base de datos a un estado utilizable coherente después de un evento catastrófico.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>Al JET_bitDbShadowingOff se deshabilitará la duplicación de algunas estructuras de base de datos internas (sombreado). La duplicación de estas estructuras se realiza para lograr resistencia, por lo JET_bitDbShadowingOff quitará esa resistencia.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>La base de datos denominada <em>en szFilename</em> ya existe. Cuando se devuelve este error, la base de datos no se adjunta.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Se puede devolver si se solicitó acceso exclusivo, pero no se pudo conceder, o si otra sesión ya ha abierto la base de datos exclusivamente.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Se devuelve <em>cuando cpgDatabaseSizeMax</em> es mayor que el número máximo de páginas permitido en una base de datos. El máximo actual es 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Se ha especificado una ruta de acceso no válida <em>en szFilename</em>. <em>szFilename</em> debe ser distinto de NULL. De forma predeterminada, <em>szFilename</em> debe apuntar a un directorio que exista. La ruta de acceso se creará <em>si JET_paramCreatePathIfNotExist</em> está establecido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Indica que otra sesión ya ha abierto la base de datos exclusivamente (mediante JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>La base de datos no se ha adjuntado previamente <a href="gg294074(v=exchg.10).md">(consulte JetAttachDatabase</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>El archivo de base de datos ya se ha adjuntado mediante una sesión diferente.</p> | 
| <p>JET_errInTransaction</p> | <p>Se intentó crear una base de datos mientras se encontraba en una transacción.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Se intentó abrir un archivo que no es un archivo de base de datos válido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Se intentó abrir más de una base de datos y JET_paramOneDatabasePerSession se estableció. Vea <a href="gg269337(v=exchg.10).md">Parámetros de base de datos</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Error en la operación porque no se pudo asignar memoria.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Solo se puede adjuntar un número finito de base de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Advertencia no permanente que indica que esta sesión ya ha adjuntado el archivo de base de datos.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indica que el archivo se adjuntaba de solo lectura, pero <strong>JetCreateDatabase</strong> no pasó JET_bitDbReadOnly. La base de datos sigue abierta con acceso de solo lectura.</p> | 



#### <a name="remarks"></a>Observaciones

Si la base de datos especificada en *szFilename* existe y JET_bitDbOverwriteExisting no se pasó, se producirá un error en la llamada API. Si JET_bitDbOverwriteExisting se ha pasado, primero se eliminará el archivo de base de datos antiguo.

Si la API crea un archivo de base de datos y, a continuación, produce otro error, limpiará y eliminará el archivo.

**JetCreateDatabase abrirá** implícitamente la base de datos. No es necesariamente llamar a [JetOpenDatabase posteriormente.](./jetopendatabase-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateDatabaseW</strong> (Unicode) y <strong>JetCreateDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
