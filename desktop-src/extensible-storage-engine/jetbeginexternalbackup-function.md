---
description: 'Más información acerca de: JetBeginExternalBackup (función)'
title: JetBeginExternalBackup función)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669713"
---
# <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetbeginexternalbackup-function"></a>JetBeginExternalBackup función)

La función **JetBeginExternalBackup** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos. **JetBeginExternalBackup** es el primero de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.

Se puede utilizar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.

La copia de seguridad será aproximada, en la que la copia de seguridad será coherente con un único punto en el tiempo en el historial de transacciones, pero no es posible controlar el punto exacto en el tiempo.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parámetros

*grbit*

Grupo de bits que especifica cero o más de las opciones siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Esta marca está en desuso. El uso de este bit producirá JET_errInvalidgrbit devuelto.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crea una copia de seguridad incremental en lugar de una copia de seguridad completa. Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro. Definido para Windows XP.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Si ya está en curso una copia de seguridad externa o de instantáneas, se devolverá este error hasta que se llame a <strong>JetBeginExternalBackup</strong> (o a una de las variantes de este). ESE solo permite una copia de seguridad en línea a la vez.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>La instancia o el motor de base de datos está en recuperación o en una fase de cierre o finalización.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt</p></td>
<td><p>En una copia de seguridad completa, no se pudo leer el archivo de punto de comprobación o no se pudo comprobar el archivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound</p></td>
<td><p>En una copia de seguridad completa, no se encontró el archivo de punto de comprobación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>El registro circular está habilitado y el tipo de copia de seguridad especificado es JET_bitBackupIncremental. Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> en los <strong>errores del registro de transacciones</strong> para obtener información sobre cómo controlar el registro circular o no circular.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uno o varios de los miembros de <em>grbit</em> no eran válidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>La recuperación o el registro están deshabilitados. No se puede realizar una copia de seguridad en línea si el registro está deshabilitado. Para obtener más información sobre el registro y la recuperación, vea <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail</p></td>
<td><p>El motor ha dejado de escribir en la unidad de registro debido a que el registro está lleno o errores de e/s de disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup</p></td>
<td><p>Se especificó la copia de seguridad incremental (con JET_bitBackupIncremental) y nunca se realizó una copia de seguridad completa para una de las bases de datos adjuntas del conjunto de registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si la función se ejecuta correctamente, se inicia una copia de seguridad externa y se inicializa el motor de estado de copia de seguridad. Ahora se puede llamar a las API subsiguientes para completar la secuencia de copia de seguridad externa y la secuencia o leer el archivo de base de datos, el archivo de revisión de la base de datos (si se admite) y el archivo de registro. Se puede registrar un evento de que se ha iniciado una copia de seguridad externa.

Si se produce un error en la función, no se iniciará la sesión de copia de seguridad. Si hay otra sesión de copia de seguridad en curso, no se cancelará.

#### <a name="remarks"></a>Observaciones

El proceso de copia de seguridad externo (tal y como lo inició **JetBeginExternalBackup**) está diseñado para permitir una copia de seguridad en línea de transacción aproximada de toda la instancia en un dispositivo de destino como un flujo. La copia de seguridad contendrá todos los archivos de base de datos que están asociados a la instancia de mediante [JetAttachDatabase](./jetattachdatabase-function.md) (para una copia de seguridad completa), seguidos de los archivos de revisión de la base de datos asociados (si se admiten) y, por último, los archivos de registro de transacciones que se generaron durante el proceso de copia de seguridad. El resultado final será un conjunto de archivos que se pueden restaurar a partir de la secuencia, posiblemente combinados con los archivos de registro y de base de datos existentes, y, por último, recuperarse a un estado coherente.

El orden general de las operaciones de una copia de seguridad completa consta de las siguientes llamadas. En primer lugar, se llama a **JetBeginExternalBackup** para iniciar el proceso de copia de seguridad. A continuación, se llama a [JetGetAttachInfo](./jetgetattachinfo-function.md) para obtener la lista de bases de datos que se adjuntan a la instancia de de la que es necesario hacer una copia de seguridad. Para cada una de estas bases de datos, se llama a [JetOpenFile](./jetopenfile-function.md) , seguido de una serie de llamadas a [JetReadFile](./jetreadfile-function.md) y, a continuación, mediante una llamada a [JetCloseFile](./jetclosefile-function.md). A continuación, se llama a [JetGetLogInfo](./jetgetloginfo-function.md) para obtener una lista de los archivos de registro y revisión de la base de datos de los que se va a hacer una copia de seguridad. Para cada uno de estos archivos, se realiza otra secuencia de llamadas a [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)y [JetCloseFile](./jetclosefile-function.md) . A continuación, se eliminan los archivos de registro de transacciones no deseados con [JetTruncateLog](./jettruncatelog-function.md). Por último, la copia de seguridad finaliza mediante una llamada a [JetEndExternalBackup](./jetendexternalbackup-function.md).

También es posible modificar este conjunto de pasos para realizar una copia de seguridad incremental de la instancia. Una copia de seguridad incremental enumera y realiza copias de seguridad de los archivos de registro. Las copias de seguridad incrementales solo son posibles si el registro circular no está habilitado.

También es posible modificar este conjunto de pasos para permitir que se realicen copias de seguridad diferenciales posteriores de la instancia. Para realizar una copia de seguridad diferencial, no llame a [JetTruncateLog](./jettruncatelog-function.md) en la copia de seguridad completa o incremental anterior. Al no llamar a [JetTruncateLog](./jettruncatelog-function.md), las copias de seguridad posteriores se habilitan para que sean diferenciales con respecto a la última copia de seguridad completa o incremental. Las copias de seguridad diferenciales solo son posibles si el registro circular no está habilitado.

El archivo de revisión de la base de datos es un archivo auxiliar especial que se usa para almacenar imágenes de páginas de base de datos en determinadas circunstancias durante la copia de seguridad. Este archivo debe estar presente en la misma ubicación que su base de datos asociada durante una operación de restauración. Este archivo solo se utiliza en Windows 2000. Como resultado, todas las aplicaciones escritas para funcionar en Windows 2000 y otras versiones deben admitir archivos de revisión de base de datos, si están presentes, pero tampoco deben generar errores si no están presentes.

#### <a name="requirements"></a>Requisitos

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
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
