---
description: 'Más información acerca de: JetAttachDatabase2 (función)'
title: Función JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716969"
---
# <a name="jetattachdatabase2-function"></a>Función JetAttachDatabase2


_**Se aplica a:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>Función JetAttachDatabase2

La función **JetAttachDatabase2** adjunta un archivo de base de datos para su uso con una instancia de base de datos y especifica un tamaño máximo para la base de datos. Para poder usar la base de datos, deberá abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada de API.

*szFilename*

Nombre de la base de datos que se va a adjuntar.

*cpgDatabaseSizeMax*

Tamaño máximo, en páginas de base de datos, para la base de datos. El tamaño de página predeterminado de la base de datos es de 4 kilobytes, que se puede cambiar mediante la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de crear una base de datos.

Pasar cero significa que no hay ningún máximo aplicado por el motor de base de datos.

*grbit*

Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Si se ha establecido <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> , se eliminarán todos los índices sobre los datos Unicode. Para obtener información más detallada, consulte la sección Comentarios.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Se eliminarán todos los índices sobre datos Unicode, independientemente del valor de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Para obtener información más detallada, consulte la sección Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Impide las modificaciones en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Reservado para uso futuro.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

La función devuelve uno de los códigos de error de [JET_ERR](./jet-err.md) . A continuación se muestran los elementos que se devuelven con más frecuencia. (Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)).

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>No se permite adjuntar una base de datos durante una copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>El archivo de base de datos especificado por <em>szFilename</em> debe ser grabable. No se debe establecer el atributo Read-Only y el proceso en ejecución debe tener privilegios suficientes para escribir en el archivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Otro proceso está abriendo el archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Se proporcionó una ruta de acceso no válida en <em>szFilename</em>. <em>szFilename</em> debe ser distinto de NULL y hacer referencia a una ruta de acceso válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Una sesión diferente ya ha adjuntado el archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>El archivo proporcionado en <em>szFilename</em> no existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Hay un error con el índice principal. Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria). También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y el índice principal está sobre una columna con datos Unicode. Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Hay un error con un índice secundario. Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria). También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode. Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode. Los índices secundarios se recompilan completamente cuando una base de datos se desfragmenta con una utilidad sin conexión mediante el siguiente comando: <strong>esentutl-d</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Solo se puede asociar un número finito de bases de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

El archivo de base de datos se separa mediante [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para obtener comentarios.

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
<td><p>Se implementa como <strong>JetAttachDatabase2W</strong> (Unicode) y <strong>JetAttachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
