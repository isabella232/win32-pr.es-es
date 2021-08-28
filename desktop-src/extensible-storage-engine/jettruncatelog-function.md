---
description: 'Más información sobre: JetTruncateLog (Función)'
title: JetTruncateLog (Función)
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa924a7061e834d4398ed68adb800912261279f7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474361"
---
# <a name="jettruncatelog-function"></a>JetTruncateLog (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jettruncatelog-function"></a>JetTruncateLog (Función)

La función **JetTruncateLog** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para eliminar los archivos de registro de transacciones que ya no se necesiten una vez que la copia de seguridad actual se complete correctamente.

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p><p><strong>Windows Server 2003:</strong>  Este valor devuelto se introduce en Windows Server 2003.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia. <strong>JetTruncateLog</strong> devolverá este error si hay identificadores de archivo pendientes que se crearon <a href="gg269249(v=exchg.10).md">mediante JetOpenFile</a> para la instancia.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado. Esto puede ocurrir para <strong>JetTruncateLog</strong> cuando el identificador de instancia especificado no es válido.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque aún no se ha inicializado la instancia asociada a la sesión.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (Windows modo de compatibilidad 2000) donde solo se admite una instancia, cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia de asociada a la sesión.</p> | 



Si esta función se realiza correctamente, se elimina el conjunto de archivos de registro de transacciones que ya no serán necesarios una vez que la copia de seguridad actual se complete correctamente. La máquina de estado de copia de seguridad estará avanzada de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo los archivos de revisión de base de datos y los archivos de registro de transacciones pueden abrirse para la copia de seguridad más allá de este punto.

Si se produce un error en esta función, la máquina de estado de copia de seguridad se puede avanzar de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Es posible que se elimine algún número de archivos de registro de transacciones que sea menor que el número deseado, pero siempre se eliminarán de más antiguos a más pequeños.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
