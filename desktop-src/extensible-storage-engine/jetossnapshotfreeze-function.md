---
description: 'Más información acerca de: JetOSSnapshotFreeze (función)'
title: Función JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278041"
---
# <a name="jetossnapshotfreeze-function"></a>Función JetOSSnapshotFreeze


_**Se aplica a:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>Función JetOSSnapshotFreeze

La función **JetOSSnapshotFreeze** inicia una instantánea. Mientras la instantánea está en curso, no se puede llevar a cabo ninguna actividad de escritura en disco por parte del motor.

**Windows XP:**  **JetOSSnapshotFreeze** se presentó en Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*snapId*

Identificador de la sesión de instantánea.

*pcInstanceInfo*

El número de instancias que se están ejecutando actualmente en el motor que forman parte de la sesión de instantáneas.

*paInstanceInfo*

Matriz de estructuras, una para cada instancia en ejecución que forma parte de la sesión de instantáneas, que describe la instancia y las bases de datos que forman parte de ella.

*grbit*

Opciones de esta llamada. Este parámetro está reservado para uso futuro y el único valor válido admitido es 0.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Los punteros proporcionados para los parámetros de salida son NULL, la sesión de instantáneas no es válida o el parámetro <em>grbit</em> no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La sesión de instantáneas no está en el estado adecuado para iniciar una inmovilización (por ejemplo, una inmovilización anterior produjo un error en esta sesión antes).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>El motor no está en un estado en el que se pueda realizar una instantánea. Ya hay una o más copias de seguridad de streaming en curso, o una o varias instancias están pasando por pasos de recuperación o finalizando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>El identificador de la sesión de instantáneas no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error de la función debido a una condición de memoria insuficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>Error de la función porque no se pudo iniciar un nuevo subproceso que realiza la inmovilización.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, no habrá ningún IOs de escritura emitido para los archivos de base de datos o para los archivos de registro que forman parte de las instancias que están inmovilizadas. Además, la información de la instancia se rellena correctamente y se debe liberar más adelante llamando a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.

Si se produce un error en esta función, el motor seguirá ejecutándose de forma habitual con la e/s que se produce como de costumbre. No es necesario llamar a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) si se produce un error en la inmovilización. Además, la información de la instancia no se rellenará, por lo que no es necesario liberar este recurso.

#### <a name="remarks"></a>Observaciones

Durante el período de inmovilización, no habrá ninguna e/s de escritura emitida a las bases de datos adjuntas ni a los registros de transacciones, aunque es posible que se emitan e/s de escritura para las bases de datos temporales o los archivos de streaming.

El estado en el que las bases de datos y los archivos de registro estarán durante la inmovilización (el estado en el que los archivos se encontrarían en una imagen de instantánea de volumen) serán de tal modo que se pueda realizar una recuperación normal si esos archivos se restauran más adelante.

Dado que no hay operaciones de escritura durante el período de inmovilización, es posible que las llamadas de API normales en el motor se detengan durante ese intervalo. La aplicación cliente debe ser capaz de controlar las llamadas API que podrían tardar más tiempo si se produce una inmovilización.

Debido a los posibles efectos descritos anteriormente, hay un tiempo de espera interno después del cual la sesión de instantáneas detendrá la fase de inmovilización aunque no se llame a las API que realizan la reanudación o anulación. El valor del tiempo de espera se puede cambiar mediante el parámetro del sistema [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Tenga en cuenta que el intervalo de inmovilización típico está en el intervalo de 10 segundos con el tiempo de espera predeterminado en unos 60 segundos.

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
<td><p>Se implementa como <strong>JetOSSnapshotFreezeW</strong> (Unicode) y <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
