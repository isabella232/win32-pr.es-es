---
description: 'Más información sobre: JetAttachDatabase2 (Función)'
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
ms.openlocfilehash: 02f896d41c5804fd85a3cb5f31b6c509c3099357
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983528"
---
# <a name="jetattachdatabase2-function"></a>Función JetAttachDatabase2


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetattachdatabase2-function"></a>Función JetAttachDatabase2

La **función JetAttachDatabase2** adjunta un archivo de base de datos para su uso con una instancia de base de datos y especifica un tamaño máximo para esa base de datos. Para usar la base de datos, deberá abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).

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

Contexto de sesión de base de datos que se usará para la llamada API.

*szFilename*

Nombre de la base de datos que se adjuntará.

*cpgDatabaseSizeMax*

Tamaño máximo, en páginas de base de datos, para la base de datos. El tamaño de página predeterminado de la base de datos es de 4 kilobytes, que se puede cambiar mediante la [función JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de crear una base de datos.

Pasar cero significa que el motor de base de datos no exige ningún máximo.

*grbit*

Un grupo de bits que contienen las opciones que se usarán para esta llamada, que incluyen cero o más de lo siguiente:


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Si <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> se ha establecido, se eliminarán todos los índices de datos Unicode. Para obtener información más detallada, consulte la sección Comentarios.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Todos los índices sobre datos Unicode se eliminarán, independientemente de la configuración de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Para obtener información más detallada, consulte la sección Comentarios.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impide las modificaciones en la base de datos.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Reservado para uso futuro.</p> | 



### <a name="return-value"></a>Valor devuelto

La función devuelve uno de [los](./jet-err.md) JET_ERR de error. Los siguientes son los que se devuelven con más habitualmente. (Para obtener una lista completa de los errores de esta API, consulte Códigos de error Storage [motor extensible).](./extensible-storage-engine-error-codes.md)


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupInProgress</p> | <p>No se permite adjuntar una base de datos durante una copia de seguridad.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>El archivo de base de datos especificado <em>por szFilename</em> debe poder escribirse. El Read-Only no debe establecerse y el proceso en ejecución debe tener privilegios suficientes para escribir en el archivo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Otro proceso ya ha abierto el archivo de base de datos.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Se ha especificado una ruta de acceso no válida <em>en szFilename.</em> <em>szFilename</em> debe ser distinto de NULL y hacer referencia a una ruta de acceso válida.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Otra sesión ya ha adjuntado el archivo de base de datos.</p> | 
| <p>JET_errFileNotFound</p> | <p>El archivo especificado en <em>szFilename</em> no existe.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Se produce un error con el índice principal. Esto puede deberse a daños físicos (por ejemplo, daños en el disco o la memoria). También se puede devolver al adjuntar una base de datos modificada por última vez en un sistema operativo anterior y el índice principal se encuentra sobre una columna con datos Unicode. Consulte los comentarios para obtener más información sobre los índices sobre los datos Unicode.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Se produce un error con un índice secundario. Esto puede deberse a daños físicos (por ejemplo, daños en el disco o la memoria). También se puede devolver al adjuntar una base de datos modificada por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode. Consulte los comentarios para obtener más información sobre los índices sobre los datos Unicode. Los índices secundarios se recompilan completamente cuando se desfragmenta una base de datos con una utilidad sin conexión mediante el siguiente <strong>comando: esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Solo se puede adjuntar un número finito de bases de datos por instancia. Actualmente, el límite es de siete bases de datos por instancia.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Una advertencia no permanente que indica que esta sesión ya ha adjuntado el archivo de base de datos.</p> | 



#### <a name="remarks"></a>Observaciones

El archivo de base de datos se [desasocia mediante JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Consulte [JetAttachDatabase para](./jetattachdatabase-function.md) obtener comentarios.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa <strong>como JetAttachDatabase2W</strong> (Unicode) y <strong>JetAttachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
