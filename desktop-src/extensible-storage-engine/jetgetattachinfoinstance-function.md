---
description: 'Más información sobre: JetGetAttachInfoInstance (Función)'
title: Función JetGetAttachInfoInstance
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 217015896779d592662655afd04216c1cd85d6ba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988058"
---
# <a name="jetgetattachinfoinstance-function"></a>Función JetGetAttachInfoInstance


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgetattachinfoinstance-function"></a>Función JetGetAttachInfoInstance

La función **JetGetAttachInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) para consultar una instancia de los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. Solo se tendrán en cuenta las bases de datos que están asociadas actualmente a la instancia [mediante JetAttachDatabase.](./jetattachdatabase-function.md) Estos archivos se pueden abrir posteriormente [mediante JetOpenFileInstance](./jetopenfileinstance-function.md) y leer [con JetReadFileInstance.](./jetreadfileinstance-function.md)

**Windows XP: JetGetAttachInfoInstance** se introdujo en Windows XP.

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
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

Búfer de salida que recibe la lista de cadenas terminadas en NULL que describen el conjunto de archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad. La lista de cadenas devueltas en este búfer tiene el mismo formato que una cadena múltiple utilizada por el Registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador null final.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*actual*

Puntero al búfer de salida que recibe la cantidad real de datos de cadena.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>Error en la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irreales que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>Error en la operación de copia de seguridad porque se llamó fuera de la secuencia. <strong>JetGetAttachInfoInstance</strong> devolverá este error si la copia de seguridad actual no es una copia de seguridad completa.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <strong>JetGetAttachInfoInstance</strong> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p> | 
| <p>JET_errNoBackup</p> | <p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p> | 
| <p>JET_errNotInitialized</p> | <p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando en realidad ya existen varias instancias.</p> | 
| <p>JET_errTermInProgress</p> | <p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p> | 



Si se ejecuta correctamente, la información solicitada sobre el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida donde se proporcionan.

En caso de error, el estado de los búferes de salida es indefinido. El error provocará la cancelación de todo el proceso de copia de seguridad de la instancia.

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
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetGetAttachInfoInstanceW</strong> (Unicode) y <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopBackupInstance](./jetstopbackupinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
