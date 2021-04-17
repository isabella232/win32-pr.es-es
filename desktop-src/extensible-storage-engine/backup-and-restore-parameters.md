---
description: Más información acerca de los parámetros de copia de seguridad y restauración
title: Parámetros de copia de seguridad y restauración
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546846"
---
# <a name="backup-and-restore-parameters"></a>Parámetros de copia de seguridad y restauración


_**Se aplica a:** Windows | Windows Server_

## <a name="backup-and-restore-parameters"></a>Parámetros de copia de seguridad y restauración

Este tema contiene los parámetros que se usan para la copia de seguridad y la restauración.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

La ruta de acceso completa a cada base de datos se conserva en los registros de transacciones en tiempo de ejecución. Normalmente, estas bases de datos deben permanecer en la ubicación original para que la reproducción de transacciones funcione correctamente. Este parámetro se puede usar para forzar la recuperación tras bloqueo o una operación de restauración para buscar las bases de datos a las que se hace referencia en el registro de transacciones en la carpeta especificada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Ruta de acceso de la carpeta (cadena)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 246 caracteres</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramCleanupMismatchedLogFiles*  
77  

Este parámetro controla el resultado de [JetInit](./jetinit-function.md) cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado. Normalmente, [JetInit](./jetinit-function.md) recuperará correctamente las bases de datos, pero producirá un error con JET_errLogFileSizeMismatchDatabasesConsistent para indicar que el tamaño del archivo de registro está mal configurado. Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará los archivos de registro antiguos de forma silenciosa, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño de archivo de registro configurado y devolverá JET_errSuccess.

Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>All</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOutOfRangeLogs*  
52  

Cuando este parámetro es true, los archivos de registro de transacciones que se encuentran en el disco y que no forman parte de la secuencia actual de archivos de registro se eliminarán mediante [JetInit](./jetinit-function.md). Se puede usar para limpiar automáticamente los archivos de registro superfluos después de una operación de restauración.

**Windows XP:**  Introducido en Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramOSSnapshotTimeout*  
82  

Este parámetro configura la cantidad de tiempo que se permite entre una llamada a [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes de que se agote el tiempo de espera. Consulte [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obtener más información. El tiempo de espera es en milisegundos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>20000 (Windows XP y Windows Server 2003);</p>
<p>70000 (Windows Server 2003 SP1)</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Entero</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>de 0 a 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramZeroDatabaseDuringBackup*  
71  

Cuando este parámetro es true, todas las páginas de una base de datos que se está sometiendo a una copia de seguridad de streaming se borrarán de los datos eliminados. Es importante tener en cuenta que las páginas de la base de datos que se van a limpiar están en el disco. Se realiza una copia de seguridad del conjunto de datos completo antes del proceso de limpieza.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor predeterminado:</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Escriba:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Ámbito:</p></td>
<td><p>Instancia</p></td>
</tr>
<tr class="odd">
<td><p>Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al diseño físico:</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>Afecta a la confiabilidad:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Afecta al rendimiento:</p></td>
<td><p>Sí</p></td>
</tr>
<tr class="even">
<td><p>Afecta a los recursos:</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidad:</p></td>
<td><p>Windows XP y versiones posteriores</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
