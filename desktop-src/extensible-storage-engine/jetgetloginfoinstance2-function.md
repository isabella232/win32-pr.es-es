---
description: 'Más información acerca de: JetGetLogInfoInstance2 (función)'
title: JetGetLogInfoInstance2 función)
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697242"
---
# <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 función)

La función **JetGetLogInfoInstance2** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar en una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad. Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y leer con [JetReadFile](./jetreadfile-function.md).

**Windows XP: JetGetLogInfoInstance2** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Parámetros

*repetición*

Instancia de que se va a usar para esta llamada.

En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia. En este caso, se implica el uso de esta instancia global.

En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia. De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.

*szz*

Búfer de salida que recibirá la lista de cadenas terminadas en null que describen el conjunto de archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.

La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro. Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.

*cbMax*

Tamaño máximo en bytes del búfer de salida.

*pcbActual*

Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.

*pLogInfo*

Recibe información estructurada sobre los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad.

Cuando este parámetro no está presente, se supone que su valor es NULL.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos. Este error solo se devolverá en Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia. <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro. Esto puede ocurrir para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de revisión de la base de datos y en los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida cuando se proporcionen. El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos. Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.

En caso de error, el estado de los búferes de salida es indefinido. El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.

#### <a name="remarks"></a>Observaciones

Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad. La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.

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
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 o Windows Server 2003.</p></td>
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
<td><p>Se implementa como <strong>JetGetLogInfoInstance2W</strong> (Unicode) y <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p></td>
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
