---
description: 'Más información sobre: JetGetLogInfoInstance (Función)'
title: JetGetLogInfoInstance (Función)
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21f931f390f7f4bf4daf8b50a2968d2dd6e193da
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982558"
---
# <a name="jetgetloginfoinstance-function"></a>JetGetLogInfoInstance (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetloginfoinstance-function"></a>JetGetLogInfoInstance (Función)

La función **JetGetLogInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup para](./jetbeginexternalbackup-function.md) consultar una instancia de los nombres de los archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad. Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y [leerse mediante JetReadFile.](./jetreadfile-function.md)

**Windows XP: JetGetLogInfoInstance** se presenta en Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de que se va a usar para esta llamada.

Para Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

Para Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación JET_errRunningInMultiInstanceMode.

*Szz*

Búfer de salida que recibirá la lista de cadenas terminadas en NULL que describen el conjunto de archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.

La lista de cadenas devueltas en este búfer tiene el mismo formato que una cadena múltiple usada por el Registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador null final.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*actual*

Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>anuló la copia de seguridad externa actual. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de secuencia. <a href="gg294055(v=exchg.10).md">JetGetLogInfo devolverá</a> este error si hay algún identificador de archivo pendiente creado <a href="gg269249(v=exchg.10).md">mediante JetOpenFile</a> para la instancia.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando, de hecho, ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, la información solicitada sobre el conjunto de archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida donde se proporcionan. La máquina de estado de copia de seguridad estará avanzada de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo los archivos de revisión de base de datos y los archivos de registro de transacciones pueden abrirse para la copia de seguridad más allá de este punto.

En caso de error, el estado de los búferes de salida es indefinido. El error dará lugar a la cancelación de todo el proceso de copia de seguridad de la instancia.

#### <a name="remarks"></a>Observaciones

Es importante tener en cuenta que esta API no devuelve un error o una advertencia si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad. La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y usar esa información para determinar si la lista se ha truncado.

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetLogInfoInstanceW</strong> (Unicode) y <strong>JetGetLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
