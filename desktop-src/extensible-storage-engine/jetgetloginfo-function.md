---
description: 'Más información sobre: JetGetLogInfo (Función)'
title: JetGetLogInfo (Función)
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 889e660254610441e56204c2585049e3c7e5ad38
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465832"
---
# <a name="jetgetloginfo-function"></a>JetGetLogInfo (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetloginfo-function"></a>JetGetLogInfo (Función)

La función **JetGetLogInfo** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar en una instancia los nombres de los archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad. Estos archivos se pueden abrir posteriormente [mediante JetOpenFile](./jetopenfile-function.md) y leer [con JetReadFile](./jetreadfile-function.md).

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*Szz*

Búfer de salida que recibirá la lista de cadenas terminadas en NULL que describen el conjunto de archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.

La lista de cadenas devueltas en este búfer tiene el mismo formato que una cadena múltiple utilizada por el Registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador null final.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*actual*

Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia. <strong>JetGetLogInfo</strong> devolverá este error si hay identificadores de archivo pendientes creados <a href="gg269249(v=exchg.10).md">mediante JetOpenFile</a> para la instancia.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetGetLogInfo</strong> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (Windows modo de compatibilidad 2000), donde solo se admite una instancia cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, la información solicitada sobre el conjunto de archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida donde se proporcionan. La máquina de estado de copia de seguridad estará avanzada de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo los archivos de revisión de base de datos y los archivos de registro de transacciones pueden abrirse para la copia de seguridad más allá de este punto.

En caso de error, el estado de los búferes de salida es indefinido. El error provocará la cancelación de todo el proceso de copia de seguridad de la instancia.

#### <a name="remarks"></a>Comentarios

Es importante tener en cuenta que esta API no devuelve un error o una advertencia si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad. La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y usar esa información para determinar si la lista se ha truncado.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetLogInfoW</strong> (Unicode) y <strong>JetGetLogInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
