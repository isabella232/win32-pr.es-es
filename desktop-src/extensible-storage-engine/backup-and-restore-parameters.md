---
description: 'Más información sobre: Parámetros de copia de seguridad y restauración'
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
ms.openlocfilehash: e57cc3f1078d46436d56a56c48c31a3fac4956c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481411"
---
# <a name="backup-and-restore-parameters"></a>Parámetros de copia de seguridad y restauración


_**Se aplica a:** Windows | Windows Servidor_

## <a name="backup-and-restore-parameters"></a>Parámetros de copia de seguridad y restauración

Este tema contiene parámetros que se usan para la copia de seguridad y restauración.

*JET_paramAlternateDatabaseRecoveryPath*  
113  

La ruta de acceso completa a cada base de datos se conserva en los registros de transacciones en tiempo de ejecución. Normalmente, estas bases de datos deben permanecer en la ubicación original para que la reproducción de transacciones funcione correctamente. Este parámetro se puede usar para forzar la recuperación de bloqueos o una operación de restauración para buscar las bases de datos a las que se hace referencia en el registro de transacciones de la carpeta especificada.


| | | <p>Valor predeterminado:</p> | <p>""</p> | | <p>Escriba:</p> | <p>Ruta de acceso de carpeta (cadena)</p> | | <p>Intervalo válido:</p> | <p>De 0 a 246 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

Este parámetro controla el resultado de [JetInit](./jetinit-function.md) cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en el disco que tienen un tamaño diferente al configurado. Normalmente, [JetInit recuperará](./jetinit-function.md) correctamente las bases de datos, pero se producirá un error JET_errLogFileSizeMismatchDatabasesConsistent para indicar que el tamaño del archivo de registro está mal configurado. Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará silenciosamente todos los archivos de registro antiguos, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño de archivo de registro configurado y devolverá JET_errSuccess.

Este parámetro es útil cuando la aplicación desea cambiar de forma transparente su tamaño de archivo de registro de transacciones, pero sigue funcionando de forma transparente en escenarios de actualización y restauración.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

Cuando este parámetro es true, JetInit eliminará todos los archivos de registro de transacciones que se encuentran en el disco que no forman parte de la secuencia actual de archivos de [registro.](./jetinit-function.md) Esto se puede usar para limpiar automáticamente los archivos de registro extraneous después de una operación de restauración.

**Windows XP:**  Introducido en Windows XP.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>Sí</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramOSSnapshotTimeout*  
82  

Este parámetro configura la cantidad de tiempo permitido entre una llamada a [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes de que se agote el tiempo de espera. Consulte [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obtener más información. El tiempo de espera es en milisegundos.


| | | <p>Valor predeterminado:</p> | <p>20000 (Windows XP y Windows Server 2003);</p><p>70000 (Windows Server 2003 SP1)</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>Sí</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

Cuando este parámetro es true, todas las páginas de una base de datos que se someten a una copia de seguridad de streaming se borrarán de los datos eliminados. Es importante tener en cuenta que las páginas de base de datos que se están limpiando están en el disco. Se hace una copia de seguridad del conjunto de datos completo antes del proceso de limpieza.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>Sí</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
