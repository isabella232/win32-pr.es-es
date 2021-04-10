---
description: 'Más información acerca de: JetAttachDatabase (función)'
title: Función JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275191"
---
# <a name="jetattachdatabase-function"></a>Función JetAttachDatabase


_**Se aplica a:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>Función JetAttachDatabase

La función **JetAttachDatabase** adjunta un archivo de base de datos para su uso con una instancia de base de datos. Para poder usar la base de datos, deberá abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*szFilename*

Nombre de la base de datos que se va a adjuntar.

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Si se ha establecido <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> , se eliminarán todos los índices sobre los datos Unicode. Para obtener información más detallada, consulte la sección Comentarios.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Se eliminarán todos los índices sobre datos Unicode, independientemente del valor de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Para obtener información más detallada, consulte la sección Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Obsoleto. No debe usarse.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Impide las modificaciones en la base de datos.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
<td><p>JET_errFileAccessDenied</p></td>
<td><p>El motor de base de datos no puede abrir el archivo de base de datos. Es posible que el archivo esté en uso por otro proceso o que el autor de la llamada no tenga privilegios suficientes para abrir el archivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>El archivo proporcionado en <em>szFilename</em> no existe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Hay un error con el índice principal. Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria). También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y el índice principal está sobre una columna con datos Unicode. Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Hay un error con un índice secundario. Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria). También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode. Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode. Los índices secundarios se recompilan completamente cuando una base de datos se desfragmenta con una utilidad sin conexión mediante el siguiente comando: <strong>esentutl-d</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Solo se puede asociar un número finito de bases de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Llamar a **JetAttachDatabase** es equivalente a llamar a [JetAttachDatabase2](./jetattachdatabase2-function.md) y pasar un valor de cero, lo que significa que no hay límite para el parámetro *cpgDatabaseSizeMax* .

Si se adjunta una base de datos de escritura (es decir, si no se especificó JET_bitDbReadOnly en el parámetro *grbit* ), el archivo se abrirá exclusivamente en el nivel de sistema operativo. Ningún otro proceso podrá abrir el archivo. Es posible que varios procesos adjunten una sola base de datos abriéndola en modo de solo lectura.

El archivo de base de datos se separa mediante [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Parámetros de comprobación de índices

Las distintas versiones de Windows normalizan el texto Unicode de maneras diferentes. Esto significa que los índices compilados con una versión de Windows pueden no funcionar en otras versiones.

Antes de Windows Server 2003, cuando la versión del sistema operativo cambió (incluida la instalación de un Service Pack), cada índice sobre datos Unicode estaba en un estado potencialmente dañado.

Los índices creados en Windows Server 2003 y versiones posteriores se marcan con la versión de normalización Unicode con la que se compilaron. Los índices más antiguos no contienen información de versión. La mayoría de los cambios de normalización Unicode consisten en agregar nuevos caracteres, los puntos de código que anteriormente no estaban definidos ahora se definen y normalizan de manera diferente. Por lo tanto, si los datos binarios se almacenan en una columna Unicode, se normalizarán de manera diferente a medida que se definen nuevos puntos de código.

A partir de Windows Server 2003, el motor de base de datos de ESE realiza un seguimiento de las entradas de índice Unicode que contienen puntos de código sin definir. Se pueden usar para corregir un índice cuando cambia el conjunto de caracteres Unicode definidos.

Estos parámetros controlan lo que sucede cuando el motor de base de datos de ESE se adjunta a una base de datos que se usó por última vez en una compilación diferente del sistema operativo. La versión del sistema operativo se marca en el encabezado de la base de datos.

Si [JET_paramEnableIndexChecking](./database-parameters.md) está establecido en **true** y la base de datos contiene índices potencialmente dañados:

  - **JetAttachDatabase** eliminará los índices potencialmente dañados si *grbit* contiene JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** devolverá un error si *grbit* no contiene JET_bitDbDeleteCorruptIndexes y hay índices que deben eliminarse.

Si [JET_paramEnableIndexChecking](./database-parameters.md) está establecido en **false**:

  - **JetAttachDatabase** omitirá los índices potencialmente dañados y devolverá JET_errSuccess (suponiendo que no haya otros errores).

Windows Server 2003 y versiones posteriores: Si no se ha restablecido [JET_paramEnableIndexChecking](./database-parameters.md) , se usará la tabla de correcciones internas para corregir las entradas de índice. Es posible que esto no corrija todos los daños en el índice, pero que sea transparente para la aplicación.

Si la base de datos se adjuntó como de solo lectura, el índice no se puede corregir ni eliminar. En este caso, la API devolverá en su lugar un error, como JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.

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
<td><p>Se implementa como <strong>JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
