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
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358305"
---
# <a name="jetcreatedatabase-function"></a>Función JetCreateDatabase


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase-function"></a>Función JetCreateDatabase

La **función JetCreateDatabase** crea y adjunta un archivo de base de datos que se usará con el motor de base de datos ESE. Llamar [a JetCreateDatabase2 con](./jetcreatedatabase2-function.md) *cpgDatabaseSizeMax* establecido en cero es idéntico a llamar a **JetCreateDatabase** con *szConnect* establecido en NULL. Actualmente, se pueden crear hasta siete bases de datos por instancia.

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
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>De forma predeterminada, si se llama a <strong>JetCreateDatabase</strong> y la base de datos ya existe, se producirá un error en la llamada API y no se sobrescribirá la base de datos original. JET_bitDbOverwriteExisting este comportamiento y la base de datos antigua se sobrescribirá con una nueva. Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff desactiva el registro. Al establecer este bit, se pierde la capacidad de reproducir los archivos de registro y recuperar la base de datos a un estado utilizable coherente después de un evento catastrófico.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>Al JET_bitDbShadowingOff se deshabilitará la duplicación de algunas estructuras de base de datos internas (sombreado). La duplicación de estas estructuras se realiza para lograr resistencia, por lo JET_bitDbShadowingOff quitará esa resistencia.</p></td>
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
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>La base de datos denominada <em>en szFilename</em> ya existe. Cuando se devuelve este error, la base de datos no se adjunta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Se puede devolver si se solicitó acceso exclusivo, pero no se pudo conceder, o si otra sesión ya ha abierto la base de datos exclusivamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Se devuelve <em>cuando cpgDatabaseSizeMax es</em> mayor que el número máximo de páginas permitidas en una base de datos. El máximo actual es 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Se ha especificado una ruta de acceso no válida <em>en szFilename.</em> <em>szFilename</em> debe ser distinto de NULL. De forma predeterminada, <em>szFilename</em> debe apuntar a un directorio que exista. La ruta de acceso se creará <em>si JET_paramCreatePathIfNotExist</em> está establecido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter).</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Indica que otra sesión ya ha abierto la base de datos exclusivamente (mediante JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>La base de datos no se ha adjuntado previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Otra sesión ya ha adjuntado el archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Se intentó crear una base de datos mientras estaba en una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Se intentó abrir un archivo que no es un archivo de base de datos válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Se intentó abrir más de una base de datos y JET_paramOneDatabasePerSession se estableció. Vea <a href="gg269337(v=exchg.10).md">Parámetros de base de datos</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Solo se puede adjuntar un número finito de base de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Una advertencia no permanente que indica que esta sesión ya ha adjuntado el archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indica que el archivo estaba adjunto de solo lectura, pero <strong>JetCreateDatabase</strong> no pasó JET_bitDbReadOnly. La base de datos todavía se abre con acceso de solo lectura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentarios

Si la base de datos especificada en *szFilename* existe y JET_bitDbOverwriteExisting no se ha pasado, se producirá un error en la llamada API. Si JET_bitDbOverwriteExisting se pasó, primero se eliminará el archivo de base de datos anterior.

Si la API crea un archivo de base de datos y, a continuación, produce otro error, limpiará y eliminará el archivo.

**JetCreateDatabase abrirá** implícitamente la base de datos. No es necesariamente llamar a [JetOpenDatabase posteriormente.](./jetopendatabase-function.md)

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
<td><p>Se implementa como <strong>JetCreateDatabaseW</strong> (Unicode) y <strong>JetCreateDatabaseA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage motor](./extensible-storage-engine-files.md)  
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
