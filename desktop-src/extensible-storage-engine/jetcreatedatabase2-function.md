---
description: 'Más información sobre: JetCreateDatabase2 (Función)'
title: Función JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4cbc3f8def16edf7e252865c4b1abcb71db12fe
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981958"
---
# <a name="jetcreatedatabase2-function"></a>Función JetCreateDatabase2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase2-function"></a>Función JetCreateDatabase2

La **función JetCreateDatabase2** crea y adjunta un archivo de base de datos que se usará con el motor de base de datos ese con un tamaño máximo de base de datos especificado. Llamar **a JetCreateDatabase2** con *cpgDatabaseSizeMax* establecido en cero es idéntico a llamar a [JetCreateDatabase](./jetcreatedatabase-function.md) con *szConnect* establecido en NULL. Actualmente se pueden crear hasta siete bases de datos por instancia.

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se va a crear.

*cpgDatabaseSizeMax*

Tamaño máximo, en páginas de base de datos, para la base de datos. El tamaño de página predeterminado de la base de datos es de 4 kilobytes y se puede cambiar [con JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de crear una base de datos.

Pasar cero significa que no hay ningún máximo aplicado por el motor de base de datos.

*pdbid*

Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos. En caso de error, el valor es indefinido.

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>De forma predeterminada, si se llama a <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> o <strong>JetCreateDatabase2</strong> y la base de datos ya existe, se producirá un error en la llamada API y no se sobrescribirá la base de datos original. JET_bitDbOverwriteExisting este comportamiento y la base de datos antigua se sobrescribirá con una nueva. Windows XP y versiones posteriores.</p> | 
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
| <p>JET_errOneDatabasePerSession</p> | <p>Se intentó abrir más de una base de datos y JET_paramOneDatabasePerSession se estableció. Vea <a href="gg294139(v=exchg.10).md">Parámetros del sistema.</a></p> | 
| <p>JET_errOutOfMemory</p> | <p>El sistema se quedó sin recursos.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Solo se puede adjuntar un número finito de base de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Advertencia no permanente que indica que esta sesión ya ha adjuntado el archivo de base de datos.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indica que el archivo se adjuntaba de solo lectura, pero <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> no pasó JET_bitDbReadOnly. La base de datos sigue abierta con acceso de solo lectura.</p> | 



#### <a name="remarks"></a>Observaciones

Si la base de datos especificada en *szFilename* existe y JET_bitDbOverwriteExisting no se pasó, se producirá un error en la llamada API. Si JET_bitDbOverwriteExisting se ha pasado, primero se eliminará el archivo de base de datos antiguo.

Si la API crea un archivo de base de datos y, a continuación, produce otro error, limpiará y eliminará el archivo.

**JetCreateDatabase2 abrirá** implícitamente la base de datos. No es necesario llamar posteriormente a [JetOpenDatabase.](./jetopendatabase-function.md)

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetCreateDatabase2W</strong> (Unicode) y <strong>JetCreateDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
