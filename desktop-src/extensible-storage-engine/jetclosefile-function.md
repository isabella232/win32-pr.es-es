---
description: 'Más información sobre: JetCloseFile (Función)'
title: JetCloseFile (Función)
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e9c8bd5eaa1bc01ba77a48af9f011f366d4c855
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465092"
---
# <a name="jetclosefile-function"></a>JetCloseFile (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetclosefile-function"></a>JetCloseFile (Función)

La **función JetCloseFile** cierra un archivo que se abrió con [JetOpenFile](./jetopenfile-function.md) después de extraer los datos de ese archivo [mediante JetReadFile](./jetreadfile-function.md).

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>Parámetros

*archivo de archivos de archivos*

Identificador del archivo que se va a leer.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p>Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetCloseFile</strong> cuando:</p><ul><li><p>El identificador de instancia especificado no es válido (Windows XP y versiones posteriores),</p></li><li><p>El identificador de archivo especificado no es válido.</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, se cierra el identificador de archivo. Si se cerró un archivo de base de datos, se destruye el archivo de revisión de base de datos asociado (si existe).

En caso de error, no se produce ningún cambio.

#### <a name="remarks"></a>Comentarios

Actualmente, el motor de base de datos solo admite un archivo abierto a [través de JetOpenFile](./jetopenfile-function.md) a la vez. Si se abre un identificador de archivo [mediante JetOpenFile,](./jetopenfile-function.md) debe cerrarse mediante **JetCloseFile** antes de que se pueda abrir otro archivo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_HANDLE](./jet-handle.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopService](./jetstopservice-function.md)
