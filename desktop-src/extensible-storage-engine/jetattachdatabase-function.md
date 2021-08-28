---
description: 'Más información sobre: JetAttachDatabase (Función)'
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
ms.openlocfilehash: eb68677ad55c137ebb40ffaef1ad0fd686bb4eb7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466762"
---
# <a name="jetattachdatabase-function"></a>Función JetAttachDatabase


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetattachdatabase-function"></a>Función JetAttachDatabase

La **función JetAttachDatabase** adjunta un archivo de base de datos para su uso con una instancia de base de datos. Para usar la base de datos, tendrá que abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se adjuntará.

*grbit*

Grupo de bits que especifican cero o más de las opciones siguientes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> se ha establecido, se eliminarán todos los índices a través de datos Unicode. Para obtener información más detallada, consulte la sección Comentarios.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Se eliminarán todos los índices a través de datos Unicode, independientemente de la configuración <a href="gg269337(v=exchg.10).md">de JET_paramEnableIndexChecking</a>. Para obtener información más detallada, consulte la sección Comentarios.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Obsoleto. No debe usarse.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impide modificaciones en la base de datos.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>No se permite adjuntar una base de datos durante una copia de seguridad.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>El archivo de base de datos especificado <em>por szFilename</em> debe poder escribirse. El Read-Only no debe establecerse y el proceso en ejecución debe tener privilegios suficientes para escribir en el archivo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Otro proceso ya ha abierto el archivo de base de datos.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Se ha especificado una ruta de acceso no válida <em>en szFilename</em>. <em>szFilename debe</em> ser distinto de NULL y hacer referencia a una ruta de acceso válida.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>El archivo de base de datos ya se ha adjuntado mediante una sesión diferente.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>El motor de base de datos no puede abrir el archivo de base de datos. El archivo puede estar en uso por otro proceso o es posible que el autor de la llamada no tenga privilegios suficientes para abrir el archivo.</p> | 
| <p>JET_errFileNotFound</p> | <p>El archivo especificado en <em>szFilename</em> no existe.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Se produce un error con el índice principal. Esto puede deberse a daños físicos (por ejemplo, daños en el disco o en la memoria). También se puede devolver al adjuntar una base de datos modificada por última vez en un sistema operativo anterior y el índice principal se encuentra sobre una columna con datos Unicode. Consulte los comentarios para obtener más información sobre los índices sobre datos Unicode.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Se produce un error con un índice secundario. Esto puede deberse a daños físicos (por ejemplo, daños en el disco o en la memoria). También se puede devolver al adjuntar una base de datos modificada por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode. Consulte los comentarios para obtener más información sobre los índices sobre datos Unicode. Los índices secundarios se recompilan completamente cuando se desfragmenta una base de datos con una utilidad sin conexión mediante el siguiente <strong>comando: esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Solo se puede adjuntar un número finito de bases de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Advertencia no permanente que indica que esta sesión ya ha adjuntado el archivo de base de datos.</p> | 



#### <a name="remarks"></a>Comentarios

Llamar a **JetAttachDatabase** equivale a llamar a [JetAttachDatabase2](./jetattachdatabase2-function.md) y pasar un valor de cero, lo que significa que no hay ningún límite, para el *parámetro cpgDatabaseSizeMax.*

La asociación de una base de datos grabable (es decir, si JET_bitDbReadOnly no se especificó en el parámetro *grbit)* abrirá el archivo exclusivamente en el nivel de sistema operativo. Ningún otro proceso podrá abrir el archivo. Es posible que varios procesos adjunte una base de datos única al abrirlos en modo de solo lectura.

El archivo de base de datos se [desasocia mediante JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Parámetros de comprobación de índices

Las distintas versiones Windows normalizar texto Unicode de maneras diferentes. Esto significa que es posible que los índices creados en una Windows no funcionen en otras versiones.

Antes de Windows Server 2003, cuando cambió la versión del sistema operativo (incluida la instalación de un Service Pack), todos los índices sobre datos Unicode se encontraban en un estado potencialmente dañado.

Los índices creados en Windows Server 2003 y versiones posteriores se marcan con la versión de normalización Unicode con la que se crearon. Los índices anteriores no contienen información de versión. La mayoría de los cambios de normalización Unicode consisten en agregar nuevos caracteres, los puntos de código que antes no estaban definidos ahora se definen y se normalizan de forma diferente. Por lo tanto, si los datos binarios se almacenan en una columna Unicode, se normalizarán de forma diferente a medida que se definan nuevos puntos de código.

A partir Windows Server 2003, el motor de base de datos ese realiza un seguimiento de las entradas de índice Unicode que contienen puntos de código no definidos. Se pueden usar para corregir un índice cuando cambia el conjunto de caracteres Unicode definidos.

Estos parámetros controlan lo que sucede cuando el motor de base de datos ese se asocia a una base de datos que se usó por última vez en una compilación diferente del sistema operativo. La versión del sistema operativo se marca en el encabezado de la base de datos.

Si [JET_paramEnableIndexChecking](./database-parameters.md) se establece en **TRUE** y la base de datos contiene índices potencialmente dañados:

  - **JetAttachDatabase eliminará** los índices potencialmente dañados si *grbit* contiene JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase devolverá** un error si *grbit* no contiene JET_bitDbDeleteCorruptIndexes y hay índices que deben eliminarse.

Si [JET_paramEnableIndexChecking](./database-parameters.md) está establecido en **FALSE:**

  - **JetAttachDatabase omitirá** los índices potencialmente dañados y devolverá JET_errSuccess (suponiendo que no haya otros errores).

Windows Server 2003 y versiones posteriores: si [JET_paramEnableIndexChecking](./database-parameters.md) se ha restablecido, se usará la tabla de corrección interna para corregir las entradas de índice. Esto puede no corregir todos los daños en el índice, pero será transparente para la aplicación.

Si la base de datos se adjunta como de solo lectura, el índice no se puede solucionar ni eliminar. En este caso, la API devolverá un error, como JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetAddColumnW</strong> (Unicode) y <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
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
