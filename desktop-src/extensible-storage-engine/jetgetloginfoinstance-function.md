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
ms.openlocfilehash: 85537c0264768c8e524fb25436e0c345d0485143426f0d22555e06e45af7e93a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944805"
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

Por Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, el uso de esta instancia global está implícito.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>Error en la operación porque una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>anuló la copia de seguridad externa actual. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque toda la actividad en la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>Error en la operación de copia de seguridad porque se llamó fuera de secuencia. <a href="gg294055(v=exchg.10).md">JetGetLogInfo devolverá</a> este error si hay algún identificador de archivo pendiente creado <a href="gg269249(v=exchg.10).md">mediante JetOpenFile</a> para la instancia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro. Esto puede ocurrir para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>Error en la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Error en la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad Windows 2000), donde solo se admite una instancia cuando, de hecho, ya existen varias instancias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la información solicitada sobre el conjunto de archivos de revisión de base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida donde se proporcionan. La máquina de estado de copia de seguridad estará avanzada de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo los archivos de revisión de base de datos y los archivos de registro de transacciones pueden abrirse para la copia de seguridad más allá de este punto.

En caso de error, el estado de los búferes de salida es indefinido. El error dará lugar a la cancelación de todo el proceso de copia de seguridad de la instancia.

#### <a name="remarks"></a>Comentarios

Es importante tener en cuenta que esta API no devuelve un error o una advertencia si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad. La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y usar esa información para determinar si la lista se ha truncado.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetLogInfoInstanceW</strong> (Unicode) y <strong>JetGetLogInfoInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
