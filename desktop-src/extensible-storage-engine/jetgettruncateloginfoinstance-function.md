---
description: 'Más información sobre: JetGetTruncateLogInfoInstance (Función)'
title: JetGetTruncateLogInfoInstance (Función)
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36583267277f7c5254adc85047ce99631f6c03ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479081"
---
# <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgettruncateloginfoinstance-function"></a>JetGetTruncateLogInfoInstance (Función)

La función **JetGetTruncateLogInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar una instancia de los nombres de los archivos de registro de transacciones que se pueden eliminar de forma segura una vez completada correctamente la copia de seguridad.

**Windows XP:****JetGetTruncateLogInfoInstance** se introdujo en Windows XP.  

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

*Szz*

Búfer de salida que recibe la lista de cadenas terminadas en NULL que describen el conjunto de archivos de registro de transacciones que se pueden eliminar de forma segura una vez completada correctamente la copia de seguridad.

La lista de cadenas que se devuelven en este búfer tiene el mismo formato que una cadena múltiple que usa el Registro. Cada cadena terminada en NULL se devuelve en secuencia y va seguida de un terminador null final.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*actual*

Puntero al búfer de salida que recibe la cantidad real de datos de cadena.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro dio lugar a un resultado inesperado.</p><p><strong>Windows XP y versiones posteriores:</strong>  Esto puede ocurrir para <strong>JetGetTruncateLogInfoInstance</strong> cuando el identificador de instancia especificado no es válido.</p> | 
| <p>JET_errNotInitialized</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>La operación no se puede completar porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>La operación no se puede completar porque la instancia de asociada a la sesión encontró un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introdujo en Windows XP.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p><p><strong>Windows XP:</strong>  Este valor devuelto se introdujo en Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia.</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>La operación no se puede completar porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errTermInProgress</p> | <p>La operación no se puede completar porque se está cerrando la instancia de asociada a la sesión.</p> | 
| <p><strong>JetGetTruncateLogInfoInstance</strong></p> | <p>Hay identificadores de archivo pendientes que se crearon <a href="gg269249(v=exchg.10).md">mediante JetOpenFile</a> para la instancia.</p> | 



Si esta función se realiza correctamente, la información solicitada sobre el conjunto de archivos de registro de transacciones que se pueden eliminar de forma segura una vez completada correctamente la copia de seguridad se colocará en los búferes de salida donde se proporcionan. La máquina de estado de copia de seguridad estará avanzada de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo se pueden abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.

Si se produce un error en esta función, el estado de los búferes de salida es indefinido. El error provocará la cancelación de todo el proceso de copia de seguridad de la instancia.

#### <a name="remarks"></a>Comentarios

Esta API no devuelve un error o una advertencia si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad. La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y usar esa información para determinar si la lista se ha truncado.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) y <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
