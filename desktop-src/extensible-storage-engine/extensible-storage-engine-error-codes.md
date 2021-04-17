---
description: 'Más información sobre: códigos de error del motor de almacenamiento extensible'
title: Códigos de error del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716833"
---
# <a name="extensible-storage-engine-error-codes"></a>Códigos de error del motor de almacenamiento extensible


_**Se aplica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>Códigos de error del motor de almacenamiento extensible

Las funciones de la API del motor de almacenamiento extensible usan los siguientes códigos de error (marcas).

Un valor [JET_ERR](./jet-err.md) de cero debe interpretarse como correcto.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Correcto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>La función se ha realizado correctamente.</p></td>
</tr>
</tbody>
</table>


Un valor [JET_ERR](./jet-err.md) mayor que cero debe interpretarse como una advertencia.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Advertencias</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>El almacén de versiones todavía está activo. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Una búsqueda en un índice no único produjo una clave única. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Una columna de base de datos es un valor largo separado. Este error lo devuelve el administrador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>El archivo de registro existente tiene una firma incorrecta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>El archivo de registro existente no es contiguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Este error solo es para uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>Se está ejecutando el TargetInstance especificado para la restauración.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>Se han reparado los daños en la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>La columna tiene un valor <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>El búfer es demasiado pequeño para los datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>La base de datos ya está adjunta.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>La ordenación que se está intentando no tiene suficiente memoria para completarse.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>No se encontró una coincidencia exacta durante una búsqueda.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>No se encontró una coincidencia exacta durante una búsqueda. Este error lo devuelve el administrador de registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>No se encontró una coincidencia exacta durante una búsqueda. Este error lo devuelve el administrador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>No hay información de error extendida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>No se ha producido ninguna actividad inactiva.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>No hay ningún bloqueo de escritura en el nivel de transacción 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>La columna se establece en un valor <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>Se abrió una tabla vacía.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>La limpieza del sistema tiene un cursor abierto en la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>Se debe quitar el índice no actualizado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>La longitud máxima es demasiado grande y se ha truncado.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Un valor de BLOB se ha pasado del registro a un almacenamiento independiente de blobs grandes.</p>
<p><strong>Nota:</strong> Este error solo es para uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>No se devolvieron los valores de columna porque el ID. de columna correspondiente o el miembro <em>itagSequence</em> de la estructura <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> que se solicitó para la enumeración era null.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>No se devolvieron los valores de columna porque no se pudieron reconstruir a partir de los datos existentes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>No se solicitaron los valores de columna existentes para la enumeración.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>El valor de la columna se truncó en el límite de tamaño solicitado durante la enumeración.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>Los valores de columna existen pero no fueron devueltos por la solicitud.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>El valor de la columna se devolvió en JET_COLUMNENUM como resultado de la JET_bitEnumerateCompressOutput que se establece.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>El valor de la columna se establece en el valor predeterminado de la columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>Los datos han cambiado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Se está usando una nueva clave.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>El archivo de base de datos es de solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>El registro inactivo está lleno.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>Había una desfragmentación con conexión que ya se estaba ejecutando en la base de datos especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>No se está ejecutando una desfragmentación con conexión en la base de datos especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2100</p></td>
<td><p>Se anuló el registro de una función de devolución de llamada que no existe.</p></td>
</tr>
</tbody>
</table>


Un valor de [JET_ERR](./jet-err.md) que sea menor que cero debe interpretarse como un error.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>La función aún no está implementada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>Error del simulador de errores de recursos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>No se ha inicializado el simulador de errores de recursos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>No se pudo cerrar el archivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>No se pudo iniciar el subproceso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>El sistema está ocupado debido a que hay demasiadas e/s.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>No se pudo ejecutar la tarea asincrónica solicitada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Se produjo un error interno grave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>Las dependencias del búfer se establecieron incorrectamente y se produjo un error de recuperación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>La versión ya existía y se produjo un error de recuperación. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>Se ha alcanzado el límite de la página. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>Se ha alcanzado el límite de la clave. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>La base de datos está dañada. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>El marcador no tiene ninguna dirección correspondiente en la base de datos. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>Error en la llamada al sistema operativo. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>Una base de datos primaria está dañada. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>La memoria caché de AvailExt no coincide con el árbol B +. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>El árbol de espacio AllAvailExt está dañado. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>Se produjo un error de memoria insuficiente al asignar un nodo de caché de AvailExt. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>El árbol de espacio OwnExt está dañado. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>El dbTime de la página actual es mayor que el de la base de datos global dbTime. Este error lo devuelve el administrador de directorios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>Error al tratar de crear una clave para una entrada de índice porque la clave se habría truncado y la definición del índice no permite el truncamiento de claves.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>La clave es demasiado grande. Este error lo devuelve el administrador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>No se puede rehacer la operación registrada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>El archivo de registro está dañado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>No se proporcionó un directorio de copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>El directorio de copia de seguridad no está vacío.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>La copia de seguridad ya está activa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>Una restauración está en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>Falta el archivo de registro para el punto de comprobación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>Error al escribir en el archivo de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>Error al intentar escribir en el registro después de la recuperación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>Error al intentar escribir en el registro durante la repuesta de recuperación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>El nombre del archivo de registro no coincide con el número de generación interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>La versión del archivo de registro no es compatible con la versión de ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>La marca de tiempo del Registro siguiente no coincide con la marca de tiempo esperada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>El registro no está activo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>El búfer de registro es demasiado pequeño para la recuperación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>Se ha superado el número máximo de archivos de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>No hay ninguna copia de seguridad en curso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>La llamada de copia de seguridad está fuera de secuencia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>No se puede realizar una copia de seguridad en este momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>No se pudo eliminar un archivo de copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>No se pudo crear el directorio temporal de copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>El registro circular está habilitado; no se puede realizar una copia de seguridad incremental.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>Los datos se restauraron con errores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>Falta el archivo de registro actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>El disco de registro está lleno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>Hay una firma incorrecta para un archivo de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>Hay una firma incorrecta para un archivo de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>Hay una firma incorrecta para un archivo de punto de comprobación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>No se encontró el archivo de punto de comprobación o estaba dañado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>No se encontró la página del archivo de revisión de la base de datos durante la recuperación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>La página del archivo de revisión de la base de datos no es válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>La repuesta finalizó repentinamente debido a un error repentino al leer los registros del archivo de registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>Esta marca está reservada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>La restauración de hardware detectó que falta un archivo de revisión de base de datos en el conjunto de copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>La base de datos no pertenece al conjunto actual de archivos de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>Esta marca está reservada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>El tamaño real del archivo de registro no coincide con <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>No se pudo encontrar el archivo de punto de comprobación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>Faltan los archivos de registro necesarios para la recuperación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>Una recuperación de software está a punto de usarse en una base de datos de copia de seguridad cuando se debe utilizar en su lugar una restauración.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>Se han recuperado las bases de datos, pero el tamaño del archivo de registro usado durante la recuperación no coincide con <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>El tamaño del sector del archivo de registro no coincide con el tamaño del sector del volumen actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>Se han recuperado las bases de datos, pero el tamaño del sector del archivo de registro (usado durante la recuperación) no coincide con el tamaño del sector del volumen actual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>Se han recuperado las bases de datos, pero se han utilizado todas las generaciones de registro posibles en la secuencia actual. Deben eliminarse todos los archivos de registro y el archivo de punto de comprobación y se deben realizar copias de seguridad de las bases de datos antes de continuar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>Se produjo un intento no válido de reproducir una operación de transmisión de archivos en la que los datos no se registraron. Esto probablemente se debe a un intento de puesta al día con el registro circular habilitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>La base de datos no se ha cerrado correctamente. Primero se debe ejecutar una recuperación para completar correctamente las operaciones de base de datos para el cierre anterior.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Este error está obsoleto y se ha reemplazado por JET_errDatabaseDirtyShutdown.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>No se ha encontrado la última hora coherente para la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>El archivo de revisión de la base de datos no se genera a partir de esta copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>El número de registro de inicio es demasiado bajo para la restauración.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>El número de registro de inicio es demasiado alto para la restauración.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>El archivo de registro de restauración tiene una firma incorrecta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>El archivo de registro de restauración no es contiguo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>Faltan algunos archivos de registro de restauración.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>La base de datos perdió una copia de seguridad completa anterior antes de intentar realizar una copia de seguridad incremental.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>El tamaño de la base de datos de copia de seguridad no es múltiplo del tamaño de página de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>Se ha detenido el intento actual de actualizar una base de datos porque la base de datos ya está actualizada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>La base de datos se convirtió solo parcialmente en el formato actual. La base de datos debe restaurarse a partir de una copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>Faltan algunos archivos de registro actuales para la restauración continua.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>El dbTime de una página es menor que el dbtimeBefore que se encuentra en el registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>El dbTime de una página es anterior al dbtimeBefore que se encuentra en el registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>Faltan algunos archivos de revisión de registro o de base de datos durante la copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>Se detectó una escritura rasgada en una copia de seguridad que se estableció durante una restauración de hardware.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>Se detectó una escritura incompleta durante una recuperación de hardware (el registro no formaba parte de un conjunto de copia de seguridad).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>Se detectaron daños en un conjunto de copia de seguridad durante una restauración de hardware.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>Se detectaron daños durante la recuperación de hardware (el registro no formaba parte de un conjunto de copia de seguridad).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>No se puede habilitar el registro al intentar actualizar una base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>No se ha encontrado el TargetInstance que se especificó para la restauración o los archivos de registro no coinciden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>El motor de base de datos ha reproducido correctamente todas las operaciones en el registro de transacciones para realizar una recuperación tras bloqueo, pero el autor de la llamada decidió detener la recuperación sin revertir las actualizaciones no confirmadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>Las bases de datos que se van a restaurar no son de la misma copia de seguridad de instantánea.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>Hay una recuperación de software en una base de datos de un conjunto de copia de seguridad de instantáneas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>El búfer de conversión Unicode es demasiado pequeño.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>Error de normalización Unicode.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>El sistema operativo no proporciona compatibilidad con la normalización Unicode y no se especificó una devolución de llamada de normalización.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>El archivo de registro existente tiene una firma incorrecta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>Un archivo de registro existente no es contiguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>Se encontró un error de suma de comprobación en el archivo de registro durante la copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>Esta marca está reservada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>Hay demasiadas generaciones pendientes entre el punto de control y la generación actual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>Se intentó realizar una recuperación de hardware en una base de datos que no era una base de datos de copia de seguridad.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>Hay un parámetro grbit no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1000</p></td>
<td><p>La terminación está en curso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>Este elemento de API no se admite.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>Se está utilizando un nombre no válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>Se está utilizando un parámetro de API no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>Se intentó asociar a un archivo de base de datos de solo lectura para las operaciones de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>Hay un identificador de base de datos no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>El sistema no tiene memoria suficiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>Se ha alcanzado el tamaño máximo de la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>La tabla está fuera de cursores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>La base de datos no tiene búferes de página.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>Hay demasiados índices.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>Hay demasiadas columnas en un índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>El registro se ha eliminado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>Hay un error de suma de comprobación en una página de base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>Hay una página de base de datos en blanco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>No hay identificadores de archivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>Hay un error de e/s de disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>Hay una ruta de acceso de archivo no válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>Hay una ruta de acceso del sistema no válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>Hay un directorio de registro no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>El registro es mayor que el tamaño máximo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>Hay demasiadas bases de datos abiertas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>No es un archivo de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>El motor de base de datos no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>El motor de base de datos ya está inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>El motor de base de datos se está inicializando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>No se puede tener acceso al archivo porque el archivo está bloqueado o en uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>El búfer es demasiado pequeño.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>Hay demasiadas columnas definidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>El contenedor no está vacío.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>El nombre de archivo no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>Hay un marcador no válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>La columna utilizada se encuentra en un índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>El búfer de datos no coincide con el tamaño de la columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>No se puede establecer el valor de la columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>El índice está en uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>La compatibilidad con vínculos no está disponible.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>No se permiten claves null en un índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>La operación debe realizarse dentro de una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>Hay demasiados usuarios de base de datos activos</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>Hay un código de país no válido o desconocido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>Hay un ID. de idioma no válido o desconocido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>Hay una página de códigos no válida o desconocida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p>Hay marcas no válidas que se usan para <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>Se produjo un intento de crear una entrada de almacén de versiones (RCE) más grande que un depósito de versión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>El almacén de versiones no tiene memoria y no se pudo completar el intento de limpieza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>El almacén de versiones no tiene memoria y ya se intentó realizar una limpieza).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>Las columnas custodia y SLV no se pueden indizar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>El registro no se ha eliminado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>Se han solicitado demasiadas entradas de mempool.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>La base de datos está fuera del árbol de objectId B +, por lo que se debe realizar una desfragmentación sin conexión para reclamar el objectId liberado o no utilizado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>El contador de identificador de valor largo ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para reclamar LongValueIDs libres o sin usar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>El contador de incremento automático ha alcanzado el valor máximo. Una desfragmentación sin conexión no podrá recuperar valores de incremento automático gratuitos o no usados).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>El contador dbTime ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para recuperar los valores de dbTime libres o no usados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>Un contador de índice secuencial ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para recuperar los valores de SequentialIndex libres o no usados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>Esta llamada de varias instancias tiene habilitado el modo de instancia única.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>Esta llamada de instancia única tiene el modo de varias instancias habilitado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>Ya se han establecido los parámetros globales del sistema.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>La ruta de acceso del sistema ya está siendo utilizada por otra instancia de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>Otra instancia de base de datos ya está usando la ruta de acceso al archivo de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>La ruta de acceso a la base de datos temporal ya está siendo utilizada por otra instancia de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>El nombre de instancia ya está en uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>Esta instancia no se puede usar porque encontró un error irrecuperable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>No se puede usar esta base de datos porque se ha producido un error irrecuperable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>Esta instancia no se puede usar porque encontró un error de registro de disco completo al realizar una operación (por ejemplo, una reversión de la transacción) que no pudo tolerar el error.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>La base de datos no tiene sesiones.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>Error en el bloqueo de escritura debido a la existencia de un bloqueo de escritura pendiente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>Las transacciones están demasiado anidadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>Hay un identificador de sesión no válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>Se intentó realizar una actualización en un índice principal no confirmado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>No se permite la operación dentro de una transacción.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>Se debe revertir la transacción actual. No se puede confirmar y no se puede iniciar una nueva.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>Una transacción de solo lectura intentó modificar la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>Se intentó reemplazar el mismo registro por dos cursores diferentes en la misma sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>El registro sería demasiado grande si se representa en un formato de base de datos de una versión anterior de jet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>No se pudo crear la tabla temporal debido a los parámetros que entran en conflicto con JET_bitTTForwardOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>No se puede usar el identificador de sesión con el ID. de tabla porque no se usó para crearlo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>El identificador de instancia no es válido o hace referencia a una instancia de que se ha cerrado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>La página de la base de datos leída del disco tenía una escritura anterior no representada en la página. Disponible en Windows 8 y versiones posteriores para el cliente de, y Windows Server 2012 y versiones posteriores para el servidor de.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>La base de datos ya existe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>La base de datos en uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>No existe dicha base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>El nombre de la base de datos no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>Hay un número no válido de páginas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>Hay un archivo que no es de base de datos o una base de datos dañada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>La base de datos está bloqueada de forma exclusiva.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>No se puede deshabilitar el control de versiones de esta base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>El motor de base de datos no es compatible con la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>La base de datos tiene un formato anterior (200). <a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo cliente de Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>La base de datos tiene un formato anterior (400). <a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo cliente de Windows NT.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>La base de datos tiene un formato anterior (500). <a href="gg294068(v=exchg.10).md">JetInit</a> devuelve este error si se establece <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> . Solo cliente de Windows NT.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>El tamaño de página de la base de datos no coincide con el motor.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>No se pueden iniciar más instancias de base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>Una instancia de base de datos diferente utiliza esta base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>Se detectaron datos adjuntos de base de datos pendientes al principio o al final de la recuperación, pero falta la base de datos o no coincide con la información de datos adjuntos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>La ruta de acceso especificada al archivo de base de datos no es válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>A una base de datos se le asigna un identificador que ya está en uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>Se permite la desasociación forzada solo después de que se detuviera la desasociación normal debido a un error.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>Se detectaron daños en el catálogo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>La base de datos solo está parcialmente adjunta y no se puede completar la operación de adjuntar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>La base de datos con la misma firma ya está en uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>La base de datos está dañada, pero no se permite una reparación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>El motor de base de datos intentó reproducir una operación de creación de base de datos desde el registro de transacciones, pero se produjo un error debido a una versión incompatible de esa operación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>La tabla está bloqueada de forma exclusiva.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>La tabla ya existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>La tabla está en uso y no se puede bloquear.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>No hay ninguna tabla u objeto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>Hay una densidad de índice o archivo incorrecta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>La tabla no está vacía.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>El ID. de tabla no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>No se pueden abrir más tablas, incluso después de que se ejecute la tarea de limpieza interna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>La operación no se admite en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>No se pueden abrir más tablas porque no se pudo completar el intento de limpieza.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>El nombre de la tabla o del objeto está en uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>El objeto no es válido para la operación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p>Se debe utilizar <a href="gg294087(v=exchg.10).md">JetCloseTable</a> en lugar de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> para eliminar una tabla temporal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>Se produjo un intento no válido de eliminar una tabla del sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>Se produjo un intento no válido de eliminar una tabla de plantilla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>Debe haber un bloqueo exclusivo en la tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>Las operaciones DDL están prohibidas en esta tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>En una tabla derivada, las operaciones DDL están prohibidas en la parte heredada del DDL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>Actualmente no se admite el anidamiento de la DDL jerárquica.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>Se produjo un intento de heredar un DDL de una tabla que no está marcada como tabla de plantillas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>Los parámetros del sistema se establecieron incorrectamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>El cliente ha solicitado que se detenga el servicio.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>La tabla de plantilla se creó con la marca NoFixedVarColumnsInDerivedTables establecida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>No se pudo generar el índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>El índice principal ya está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>El índice ya está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>No existe este tipo de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>No se puede eliminar el índice clúster.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>La definición del índice no es válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>La creación de la descripción del índice no era válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>La base de datos está fuera de los bloques de Descripción del índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>Se han generado claves de índice entre registros no únicas para un índice con varios valores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>Un índice secundario que refleja correctamente el índice principal no se pudo compilar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>El índice principal está dañado y se debe desfragmentar la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>El índice secundario está dañado y se debe desfragmentar la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>El ID. de índice no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>El índice de tupla solo se puede establecer en un índice secundario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>La definición de índice para el índice de tupla contiene más columnas de clave que el motor de base de datos puede admitir.</p>
<p><strong>Nota:  </strong> El error de JET_errIndexTuplesOneColumnOnly está obsoleto y se ha reemplazado por JET_errIndexTuplesTooManyColumns.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>El índice de tupla debe ser un índice no único.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>Una definición de índice de tupla solo puede contener columnas de clave que tengan tipos de columna de texto o binarios.</p>
<p><strong>Nota:  </strong> El error de JET_errIndexTuplesTextColumnsOnly está obsoleto y se ha reemplazado por JET_errIndexTuplesTextBinaryColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>El índice de tupla no permite establecer cbVarSegMac.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>La longitud de tupla mínima/máxima o el número máximo de caracteres que se especifican para un índice no son válidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p>No se puede llamar a <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> con la marca JET_bitRetrieveFromIndex establecida al recuperar una columna en un índice de tupla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>La clave especificada no cumple la longitud mínima de la tupla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>El valor de la columna es Long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>No existe este fragmento en un valor largo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>El campo no cabe en el registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>NULL no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>NULL no es válido. Este error lo devuelve el administrador de registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>La columna está indizada y no se puede eliminar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>La longitud del campo es mayor que la longitud máxima permitida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>No existe esa columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Este campo ya está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>Se intentó crear una columna con varios valores, pero no se etiquetó la columna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>Se produjo una segunda columna de incremento automático o de versión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>El tipo de datos de la columna no es válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>No hay ninguna columna etiquetada que no sea NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>La base de datos no es válida porque no contiene un índice actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>La clave se realiza por completo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>El ID. de columna no es correcto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>Hay un itagSequence incorrecto para la columna etiquetada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>No se puede eliminar una columna porque forma parte de una relación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>El incremento automático y la versión no se pueden etiquetar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>El valor predeterminado es mayor que el tamaño máximo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>Se detectó un valor duplicado en una columna con varios valores única.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>Se encontraron daños en un árbol de valores largos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>Se detectó un valor duplicado en una columna con varios valores única después de que se normalizaran los datos y se normalizó el truncamiento de los datos antes de la comparación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>Hay una columna no válida en la tabla derivada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>Se intentó convertir una columna en un marcador de posición de índice principal, pero la columna no cumple los criterios necesarios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>No se encontró la clave.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>No hay ningún búfer de trabajo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>No hay ningún registro actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>Es posible que la clave principal no cambie.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Hay una clave duplicada no válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>Se intentó actualizar un registro mientras una actualización de registro ya estaba en curso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>No se realizó una llamada a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>No se realizó una llamada a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>Los datos han cambiado y se anuló la operación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>Esta instalación de Windows no admite el idioma seleccionado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Hay demasiados procesos de ordenación.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Se produjo una operación no válida durante una ordenación.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>No se pudo abrir el archivo temporal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Hay demasiadas bases de datos abiertas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>No queda espacio en el disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Se denegó el permiso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>No se encontró el archivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>El tipo de archivo no es válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>No se puede iniciar una restauración después de la inicialización.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>No se pudieron interpretar los registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>La operación no es válida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>Acceso denegado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>División infinita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Varios subprocesos están usando la misma sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>No se pudo encontrar un punto de entrada en un archivo DLL necesario.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>La sesión especificada ya tiene un conjunto de contextos de sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>Se intentó restablecer el contexto de la sesión, pero el subproceso actual no era el original que estableció el contexto de la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>Se ha intentado finalizar la sesión actualmente en uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Se produjo un error interno durante la conversión del formato de registro dinámico.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>Solo se permite una base de datos de usuario abierta por sesión (como se indica al establecer la marca de <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante la creación de la base de datos).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Error durante la reversión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Error en una llamada de función de devolución de llamada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>No se pudo encontrar una función de devolución de llamada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>La API de instantáneas de sistema operativo se usó en una secuencia no válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>La instantánea del sistema operativo finalizó con un tiempo de espera.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>La instantánea del sistema operativo no está permitida porque una copia de seguridad o una recuperación en está en curso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>No se pudo realizar la operación porque el controlador de instantáneas del sistema operativo especificado no era válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>Se intentó usar el almacenamiento local sin especificar una función de devolución de llamada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>Se intentó establecer el almacenamiento local de un objeto que ya lo tenía establecido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>Se intentó recuperar el almacenamiento local de un objeto que no lo tenía establecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>No se pudo realizar una operación de e/s porque se intentó en una región sin asignar de un archivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Se emitió una lectura a una ubicación más allá de EOF (las escrituras expandirán el archivo).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Esta marca indica al JET_ABORTRETRYFAILCALLBACK que llama para anular la e/s especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Esta marca indica al llamador JET_ABORTRETRYFAILCALLBACK que vuelva a intentar la e/s especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Esta marca indica al JET_ABORTRETRYFAILCALLBACK llamador que produzca un error en la e/s especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>No se admite el acceso de lectura y escritura en archivos comprimidos.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Observaciones

En general, un valor mayor que cero debe interpretarse como una advertencia, el valor cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error. Ningún otro patrón de estos valores, como los intervalos de valores, debe basarse en una aplicación.

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

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[Archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md)
