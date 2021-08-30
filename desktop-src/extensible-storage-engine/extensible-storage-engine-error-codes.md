---
description: 'Más información sobre: Códigos de error extensibles Storage motor de datos'
title: Códigos de error Storage motor extensibles
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
ms.openlocfilehash: cdbdff7255b621eaab59cfbf38cb577a6e8c0331
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481781"
---
# <a name="extensible-storage-engine-error-codes"></a>Códigos de error Storage motor extensibles


_**Se aplica a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-error-codes"></a>Códigos de error Storage motor extensibles

Las funciones de Extensible Storage Engine API usan los siguientes códigos de error (marcas).

Un [JET_ERR](./jet-err.md) valor cero debe interpretarse como correcto.


| <p>Correcto</p> | <p>Descripción</p> | 
|----------------|--------------------|
| <p>JET_errSuccess 0</p> | <p>La función se ha realizado correctamente.</p> | 



Un [JET_ERR](./jet-err.md) que sea mayor que cero debe interpretarse como una advertencia.


| <p>Warnings</p> | <p>Descripción</p> | 
|-----------------|--------------------|
| <p>JET_wrnRemainingVersions<br />321</p> | <p>El almacén de versiones sigue activo. El administrador de directorios devuelve este error.</p> | 
| <p>JET_wrnUniqueKey<br />345</p> | <p>Una búsqueda en un índice no único produjo una clave única. El administrador de directorios devuelve este error.</p> | 
| <p>JET_wrnSeparateLongValue<br />406</p> | <p>Una columna de base de datos es un valor long separado. El administrador de registros devuelve este error.</p> | 
| <p>JET_wrnExistingLogFileHasBadSignature<br />558</p> | <p>El archivo de registro existente tiene una firma no válida.</p> | 
| <p>JET_wrnExistingLogFileIsNotContiguous<br />559</p> | <p>El archivo de registro existente no es contiguo.</p> | 
| <p>JET_wrnSkipThisRecord<br />564</p> | <p>Este error es solo para uso interno.</p> | 
| <p>JET_wrnTargetInstanceRunning<br />578</p> | <p>Se está ejecutando la instancia de TargetInstance especificada para la restauración.</p> | 
| <p>JET_wrnDatabaseRepaired<br />595</p> | <p>Se han reparado los daños en la base de datos.</p> | 
| <p>JET_wrnColumnNull<br />1004</p> | <p>La columna tiene un <strong>valor</strong> NULL.</p> | 
| <p>JET_wrnBufferTruncated<br />1006</p> | <p>El búfer es demasiado pequeño para los datos.</p> | 
| <p>JET_wrnDatabaseAttached<br />1007</p> | <p>La base de datos ya está adjunta.</p> | 
| <p>JET_wrnSortOverflow<br />1009</p> | <p>La ordenación que se intenta no tiene suficiente memoria para completarse.</p> | 
| <p>JET_wrnSeekNotEqual<br />1039</p> | <p>No se encontró una coincidencia exacta durante una búsqueda.</p> | 
| <p>JET_wrnRecordFoundGreater<br />JET_wrnSeekNotEqual</p> | <p>No se encontró una coincidencia exacta durante una búsqueda. El administrador de registros devuelve este error.</p> | 
| <p>JET_wrnRecordFoundLess<br />JET_wrnSeekNotEqual</p> | <p>No se encontró una coincidencia exacta durante una búsqueda. El administrador de registros devuelve este error.</p> | 
| <p>JET_wrnNoErrorInfo<br />1055</p> | <p>No hay ninguna información de error extendida.</p> | 
| <p>JET_wrnNoIdleActivity<br />1058</p> | <p>No se ha producido ninguna actividad inactiva.</p> | 
| <p>JET_wrnNoWriteLock<br />1067</p> | <p>No hay ningún bloqueo de escritura en el nivel de transacción 0.</p> | 
| <p>JET_wrnColumnSetNull<br />1068</p> | <p>La columna se establece en un <strong>valor</strong> NULL.</p> | 
| <p>JET_wrnTableEmpty<br />1301</p> | <p>Se ha abierto una tabla vacía.</p> | 
| <p>JET_wrnTableInUseBySystem<br />1327</p> | <p>La limpieza del sistema tiene un cursor abierto en la tabla.</p> | 
| <p>JET_wrnCorruptIndexDeleted<br />1415</p> | <p>Se debe quitar el índice no actualizado.</p> | 
| <p>JET_wrnColumnMaxTruncated<br />1512</p> | <p>La longitud máxima es demasiado grande y se ha truncado.</p> | 
| <p>JET_wrnCopyLongValue<br />1520</p> | <p>Un valor BLOB se ha movido del registro a un almacenamiento independiente de blobs grandes.</p><p><strong>Nota</strong> Este error es solo para uso interno.</p> | 
| <p>JET_wrnColumnSkipped<br />1531</p> | <p>No se devolvieron los valores de columna porque el identificador <a href="gg294052(v=exchg.10).md"></a> de columna correspondiente o el miembro <em>itagSequence</em> de la estructura JET_ENUMCOLUMNVALUE que se solicitó para la enumeración era NULL.</p> | 
| <p>JET_wrnColumnNotLocal<br />1532</p> | <p>No se devolvieron los valores de columna porque no se pudieron reconstruir a partir de los datos existentes.</p> | 
| <p>JET_wrnColumnMoreTags<br />1533</p> | <p>Los valores de columna existentes no se solicitaron para la enumeración.</p> | 
| <p>JET_wrnColumnTruncated<br />1534</p> | <p>El valor de columna se truntó en el límite de tamaño solicitado durante la enumeración.</p> | 
| <p>JET_wrnColumnPresent<br />1535</p> | <p>Los valores de columna existen, pero la solicitud no los devolvió.</p> | 
| <p>JET_wrnColumnSingleValue<br />1536</p> | <p>El valor de columna se devolvió en JET_COLUMNENUM como resultado de la JET_bitEnumerateCompressOutput se establece.</p> | 
| <p>JET_wrnColumnDefault<br />1537</p> | <p>El valor de columna se establece en el valor predeterminado de la columna.</p> | 
| <p>JET_wrnDataHasChanged<br />1610</p> | <p>Los datos han cambiado.</p> | 
| <p>JET_wrnKeyChanged<br />1618</p> | <p>Se está utilizando una nueva clave.</p> | 
| <p>JET_wrnFileOpenReadOnly<br />1813</p> | <p>El archivo de base de datos es de solo lectura.</p> | 
| <p>JET_wrnIdleFull<br />1908</p> | <p>El registro inactivo está lleno.</p> | 
| <p>JET_wrnDefragAlreadyRunning<br />2000</p> | <p>Ya se estaba ejecutando una desfragmentación en línea en la base de datos especificada.</p> | 
| <p>JET_wrnDefragNotRunning<br />2001</p> | <p>No se está ejecutando una desfragmentación en línea en la base de datos especificada.</p> | 
| <p>JET_wrnCallbackNotRegistered<br />2100</p> | <p>Se ha anulado el registro de una función de devolución de llamada inexistente.</p> | 



Un [JET_ERR](./jet-err.md) que sea menor que cero debe interpretarse como un error.


| <p>Errors</p> | <p>Descripción</p> | 
|---------------|--------------------|
| <p>JET_wrnNyi<br />-1</p> | <p>La función aún no se ha implementado.</p> | 
| <p>JET_errRfsFailure<br />-100</p> | <p>Error en el simulador de errores de recursos.</p> | 
| <p>JET_errRfsNotArmed<br />-101</p> | <p>No se ha inicializado el simulador de errores de recursos.</p> | 
| <p>JET_errFileClose<br />-102</p> | <p>No se pudo cerrar el archivo.</p> | 
| <p>JET_errOutOfThreads<br />-103</p> | <p>No se pudo iniciar el subproceso.</p> | 
| <p>JET_errTooManyIO<br />-105</p> | <p>El sistema está ocupado debido a demasiadas E/S.</p> | 
| <p>JET_errTaskDropped<br />-106</p> | <p>No se pudo ejecutar la tarea asincrónica solicitada.</p> | 
| <p>JET_errInternalError<br />-107</p> | <p>Se produjo un error interno grave.</p> | 
| <p>JET_errDatabaseBufferDependenciesCorrupted<br />-255</p> | <p>Las dependencias del búfer se han establecido incorrectamente y se ha produce un error de recuperación.</p> | 
| <p>JET_errPreviousVersion<br />-322</p> | <p>La versión ya existía y se ha producido un error de recuperación. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errPageBoundary<br />-323</p> | <p>Se ha alcanzado el límite de página. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errKeyBoundary<br />-324</p> | <p>Se ha alcanzado el límite de clave. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errBadPageLink<br />-327</p> | <p>La base de datos está dañada. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errBadBookmark<br />-328</p> | <p>El marcador no tiene ninguna dirección correspondiente en la base de datos. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errNTSystemCallFailed<br />-334</p> | <p>Error en la llamada al sistema operativo. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errBadParentPageLink<br />-338</p> | <p>Una base de datos primaria está dañada. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errSPAvailExtCacheOutOfSync<br />-340</p> | <p>La caché AvailExt no coincide con el árbol B+. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errSPAvailExtCorrupted<br />-341</p> | <p>El árbol de espacio AllAvailExt está dañado. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errSPAvailExtCacheOutOfMemory<br />-342</p> | <p>Se produjo un error de memoria fuera de memoria al asignar un nodo de caché AvailExt. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errSPOwnExtCorrupted<br />-343</p> | <p>El árbol de espacio OwnExt está dañado. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errDbTimeCorrupted<br />-344</p> | <p>Dbtime en la página actual es mayor que el valor de dbtime de la base de datos global. El administrador de directorios devuelve este error.</p> | 
| <p>JET_errKeyTruncated<br />-346</p> | <p>Error al intentar crear una clave para una entrada de índice porque la clave se habría truncado y la definición de índice no permite el truncamiento de la clave.</p> | 
| <p>JET_errKeyTooBig<br />-408</p> | <p>La clave es demasiado grande. El administrador de registros devuelve este error.</p> | 
| <p>JET_errInvalidLoggedOperation<br />-500</p> | <p>La operación registrada no se puede volver a crear.</p> | 
| <p>JET_errLogFileCorrupt<br />-501</p> | <p>El archivo de registro está dañado.</p> | 
| <p>JET_errNoBackupDirectory<br />-503</p> | <p>No se ha especificado un directorio de copia de seguridad.</p> | 
| <p>JET_errBackupDirectoryNotEmpty<br />-504</p> | <p>El directorio de copia de seguridad no está vacío.</p> | 
| <p>JET_errBackupInProgress<br />-505</p> | <p>La copia de seguridad ya está activa.</p> | 
| <p>JET_errRestoreInProgress<br />-506</p> | <p>Hay una restauración en curso.</p> | 
| <p>JET_errMissingPreviousLogFile<br />-509</p> | <p>Falta el archivo de registro para el punto de comprobación.</p> | 
| <p>JET_errLogWriteFail<br />-510</p> | <p>Error al escribir en el archivo de registro.</p> | 
| <p>JET_errLogDisabledDueToRecoveryFailure<br />-511</p> | <p>Error al intentar escribir en el registro después de la recuperación.</p> | 
| <p>JET_errCannotLogDuringRecoveryRedo<br />-512</p> | <p>Error al intentar escribir en el registro durante la fase de rehacer la recuperación.</p> | 
| <p>JET_errLogGenerationMismatch<br />-513</p> | <p>El nombre del archivo de registro no coincide con el número de generación interno.</p> | 
| <p>JET_errBadLogVersion<br />-514</p> | <p>La versión del archivo de registro no es compatible con la versión ese.</p> | 
| <p>JET_errInvalidLogSequence<br />-515</p> | <p>La marca de tiempo del siguiente registro no coincide con la marca de tiempo esperada.</p> | 
| <p>JET_errLoggingDisabled<br />-516</p> | <p>El registro no está activo.</p> | 
| <p>JET_errLogBufferTooSmall<br />-517</p> | <p>El búfer de registro es demasiado pequeño para la recuperación.</p> | 
| <p>JET_errLogSequenceEnd<br />-519</p> | <p>Se ha superado el número máximo de archivos de registro.</p> | 
| <p>JET_errNoBackup<br />-520</p> | <p>No hay ninguna copia de seguridad en curso.</p> | 
| <p>JET_errInvalidBackupSequence<br />-521</p> | <p>La llamada de copia de seguridad está fuera de secuencia.</p> | 
| <p>JET_errBackupNotAllowedYet<br />-523</p> | <p>No se puede realizar una copia de seguridad en este momento.</p> | 
| <p>JET_errDeleteBackupFileFail<br />-524</p> | <p>No se pudo eliminar un archivo de copia de seguridad.</p> | 
| <p>JET_errMakeBackupDirectoryFail<br />-525</p> | <p>No se pudo crear el directorio temporal de copia de seguridad.</p> | 
| <p>JET_errInvalidBackup<br />-526</p> | <p>El registro circular está habilitado; No se puede realizar una copia de seguridad incremental.</p> | 
| <p>JET_errRecoveredWithErrors<br />-527</p> | <p>Los datos se restauraron con errores.</p> | 
| <p>JET_errMissingLogFile<br />-528</p> | <p>Falta el archivo de registro actual.</p> | 
| <p>JET_errLogDiskFull<br />-529</p> | <p>El disco de registro está lleno.</p> | 
| <p>JET_errBadLogSignature<br />-530</p> | <p>Hay una firma no válida para un archivo de registro.</p> | 
| <p>JET_errBadDbSignature<br />-531</p> | <p>Hay una firma no válida para un archivo de base de datos.</p> | 
| <p>JET_errBadCheckpointSignature<br />-532</p> | <p>Hay una firma no válida para un archivo de punto de comprobación.</p> | 
| <p>JET_errCheckpointCorrupt<br />-533</p> | <p>El archivo de punto de comprobación no se encontró o estaba dañado.</p> | 
| <p>JET_errMissingPatchPage<br />-534</p> | <p>No se encontró la página del archivo de revisión de base de datos durante la recuperación.</p> | 
| <p>JET_errBadPatchPage<br />-535</p> | <p>La página del archivo de revisión de base de datos no es válida.</p> | 
| <p>JET_errRedoAbruptEnded<br />-536</p> | <p>La rehacer finalizó repentinamente debido a un error repentino al leer los registros del archivo de registro.</p> | 
| <p>JET_errBadSLVSignature<br />-537</p> | <p>Esta marca está reservada.</p> | 
| <p>JET_errPatchFileMissing<br />-538</p> | <p>La restauración en disco detectó que falta un archivo de revisión de base de datos del conjunto de copia de seguridad.</p> | 
| <p>JET_errDatabaseLogSetMismatch<br />-539</p> | <p>La base de datos no pertenece al conjunto actual de archivos de registro.</p> | 
| <p>JET_errDatabaseStreamingFileMismatch<br />-540</p> | <p>Esta marca está reservada.</p> | 
| <p>JET_errLogFileSizeMismatch<br />-541</p> | <p>El tamaño real del archivo de registro no coincide <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p> | 
| <p>JET_errCheckpointFileNotFound<br />-542</p> | <p>No se pudo encontrar el archivo de punto de comprobación.</p> | 
| <p>JET_errRequiredLogFilesMissing<br />-543</p> | <p>Faltan los archivos de registro necesarios para la recuperación.</p> | 
| <p>JET_errSoftRecoveryOnBackupDatabase<br />-544</p> | <p>Una recuperación flexible está a punto de usarse en una base de datos de copia de seguridad cuando se debe usar una restauración en su lugar.</p> | 
| <p>JET_errLogFileSizeMismatchDatabasesConsistent<br />-545</p> | <p>Las bases de datos se han recuperado, pero el tamaño del archivo de registro utilizado durante la recuperación no coincide <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p> | 
| <p>JET_errLogSectorSizeMismatch<br />-546</p> | <p>El tamaño del sector del archivo de registro no coincide con el tamaño del sector del volumen actual.</p> | 
| <p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />-547</p> | <p>Las bases de datos se han recuperado, pero el tamaño del sector del archivo de registro (que se usa durante la recuperación) no coincide con el tamaño del sector del volumen actual.</p> | 
| <p>JET_errLogSequenceEndDatabasesConsistent<br />-548</p> | <p>Se han recuperado las bases de datos, pero se han usado todas las generaciones de registros posibles de la secuencia actual. Todos los archivos de registro y el archivo de punto de comprobación deben eliminarse y se debe realizar una copia de seguridad de las bases de datos antes de continuar.</p> | 
| <p>JET_errStreamingDataNotLogged<br />-549</p> | <p>Se ha intentado reproducir una operación de archivo de streaming en la que no se registraron los datos. Esto probablemente se debe a un intento de revertir con el registro circular habilitado.</p> | 
| <p>JET_errDatabaseDirtyShutdown<br />-550</p> | <p>La base de datos no se ha apagado correctamente. Primero se debe ejecutar una recuperación para completar correctamente las operaciones de base de datos del cierre anterior.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>Este error está obsoleto y se ha reemplazado por JET_errDatabaseDirtyShutdown.</p> | 
| <p>JET_errConsistentTimeMismatch<br />-551</p> | <p>No se ha coincidente la última hora coherente para la base de datos.</p> | 
| <p>JET_errDatabasePatchFileMismatch<br />-552</p> | <p>El archivo de revisión de base de datos no se genera a partir de esta copia de seguridad.</p> | 
| <p>JET_errEndingRestoreLogTooLow<br />-553</p> | <p>El número de registro inicial es demasiado bajo para la restauración.</p> | 
| <p>JET_errStartingRestoreLogTooHigh<br />-554</p> | <p>El número de registro inicial es demasiado alto para la restauración.</p> | 
| <p>JET_errGivenLogFileHasBadSignature<br />-555</p> | <p>El archivo de registro de restauración tiene una firma no válida.</p> | 
| <p>JET_errGivenLogFileIsNotContiguous<br />-556</p> | <p>El archivo de registro de restauración no es contiguo.</p> | 
| <p>JET_errMissingRestoreLogFiles<br />-557</p> | <p>Faltan algunos archivos de registro de restauración.</p> | 
| <p>JET_errMissingFullBackup<br />-560</p> | <p>La base de datos omitía una copia de seguridad completa anterior antes de intentar realizar una copia de seguridad incremental.</p> | 
| <p>JET_errBadBackupDatabaseSize<br />-561</p> | <p>El tamaño de la base de datos de copia de seguridad no es un múltiplo del tamaño de página de la base de datos.</p> | 
| <p>JET_errDatabaseAlreadyUpgraded<br />-562</p> | <p>El intento actual de actualizar una base de datos se ha detenido porque la base de datos ya está actualizada.</p> | 
| <p>JET_errDatabaseIncompleteUpgrade<br />-563</p> | <p>La base de datos solo se ha convertido parcialmente al formato actual. La base de datos debe restaurarse a partir de la copia de seguridad.</p> | 
| <p>JET_errMissingCurrentLogFiles<br />-565</p> | <p>Faltan algunos archivos de registro actuales para la restauración continua.</p> | 
| <p>JET_errDbTimeTooOld<br />-566</p> | <p>El valor dbtime de una página es menor que dbtimeBefore que se encuentra en el registro.</p> | 
| <p>JET_errDbTimeTooNew<br />-567</p> | <p>El dbtime de una página es anterior al dbtimeBefore que se encuentra en el registro.</p> | 
| <p>JET_errMissingFileToBackup<br />-569</p> | <p>Faltan algunos archivos de revisión de base de datos o registro durante la copia de seguridad.</p> | 
| <p>JET_errLogTornWriteDuringHardRestore<br />-570</p> | <p>Se detectó una escritura rasgada en una copia de seguridad que se estableció durante una restauración fuerte.</p> | 
| <p>JET_errLogTornWriteDuringHardRecovery<br />-571</p> | <p>Se detectó una escritura rasgada durante una recuperación fuerte (el registro no formaba parte de un conjunto de copia de seguridad).</p> | 
| <p>JET_errLogCorruptDuringHardRestore<br />-573</p> | <p>Se detectaron daños en un conjunto de copia de seguridad durante una restauración fuerte.</p> | 
| <p>JET_errLogCorruptDuringHardRecovery<br />-574</p> | <p>Se detectaron daños durante la recuperación dura (el registro no formaba parte de un conjunto de copia de seguridad).</p> | 
| <p>JET_errMustDisableLoggingForDbUpgrade<br />-575</p> | <p>No se puede habilitar el registro al intentar actualizar una base de datos.</p> | 
| <p>JET_errBadRestoreTargetInstance<br />-577</p> | <p>No se ha encontrado el elemento TargetInstance especificado para la restauración o los archivos de registro no coinciden.</p> | 
| <p>JET_errRecoveredWithoutUndo<br />-579</p> | <p>El motor de base de datos reprobaba correctamente todas las operaciones del registro de transacciones para realizar una recuperación de bloqueos, pero el autor de la llamada eligió detener la recuperación sin revertir las actualizaciones no confirmadas.</p> | 
| <p>JET_errDatabasesNotFromSameSnapshot<br />-580</p> | <p>Las bases de datos que se van a restaurar no son de la misma copia de seguridad de instantáneas.</p> | 
| <p>JET_errSoftRecoveryOnSnapshot<br />-581</p> | <p>Hay una recuperación de software en una base de datos a partir de un conjunto de copia de seguridad de instantáneas.</p> | 
| <p>JET_errUnicodeTranslationBufferTooSmall<br />-601</p> | <p>El búfer de traducción Unicode es demasiado pequeño.</p> | 
| <p>JET_errUnicodeTranslationFail<br />-602</p> | <p>Error de normalización Unicode.</p> | 
| <p>JET_errUnicodeNormalizationNotSupported<br />-603</p> | <p>El sistema operativo no proporciona compatibilidad con la normalización Unicode y no se especificó una devolución de llamada de normalización.</p> | 
| <p>JET_errExistingLogFileHasBadSignature<br />-610</p> | <p>El archivo de registro existente tiene una firma no válida.</p> | 
| <p>JET_errExistingLogFileIsNotContiguous<br />-611</p> | <p>Un archivo de registro existente no es contiguo.</p> | 
| <p>JET_errLogReadVerifyFailure<br />-612</p> | <p>Se encontró un error de suma de comprobación en el archivo de registro durante la copia de seguridad.</p> | 
| <p>JET_errSLVReadVerifyFailure<br />-613</p> | <p>Esta marca está reservada.</p> | 
| <p>JET_errCheckpointDepthTooDeep<br />-614</p> | <p>Hay demasiadas generaciones pendientes entre el punto de control y la generación actual.</p> | 
| <p>JET_errRestoreOfNonBackupDatabase<br />-615</p> | <p>Se intentó realizar una recuperación en una base de datos que no era una base de datos de copia de seguridad.</p> | 
| <p>JET_errInvalidGrbit<br />-900</p> | <p>Hay un parámetro grbit no válido.</p> | 
| <p>JET_errTermInProgress<br />-1000</p> | <p>La terminación está en curso.</p> | 
| <p>JET_errFeatureNotAvailable<br />-1001</p> | <p>No se admite este elemento de API.</p> | 
| <p>JET_errInvalidName<br />-1002</p> | <p>Se usa un nombre no válido.</p> | 
| <p>JET_errInvalidParameter<br />-1003</p> | <p>Se usa un parámetro de API no válido.</p> | 
| <p>JET_errDatabaseFileReadOnly<br />-1008</p> | <p>Se intentó adjuntar a un archivo de base de datos de solo lectura para operaciones de lectura y escritura.</p> | 
| <p>JET_errInvalidDatabaseId<br />-1010</p> | <p>Hay un identificador de base de datos no válido.</p> | 
| <p>JET_errOutOfMemory<br />-1011</p> | <p>El sistema está sin memoria.</p> | 
| <p>JET_errOutOfDatabaseSpace<br />-1012</p> | <p>Se ha alcanzado el tamaño máximo de la base de datos.</p> | 
| <p>JET_errOutOfCursors<br />-1013</p> | <p>La tabla está fuera de cursores.</p> | 
| <p>JET_errOutOfBuffers<br />-1014</p> | <p>La base de datos está fuera de los búferes de página.</p> | 
| <p>JET_errTooManyIndexes<br />-1015</p> | <p>Hay demasiados índices.</p> | 
| <p>JET_errTooManyKeys<br />-1016</p> | <p>Hay demasiadas columnas en un índice.</p> | 
| <p>JET_errRecordDeleted<br />-1017</p> | <p>El registro se ha eliminado.</p> | 
| <p>JET_errReadVerifyFailure<br />-1018</p> | <p>Hay un error de suma de comprobación en una página de base de datos.</p> | 
| <p>JET_errPageNotInitialized<br />-1019</p> | <p>Hay una página de base de datos en blanco.</p> | 
| <p>JET_errOutOfFileHandles<br />-1020</p> | <p>No hay identificadores de archivo.</p> | 
| <p>JET_errDiskIO<br />-1022</p> | <p>Hay un error de E/S de disco.</p> | 
| <p>JET_errInvalidPath<br />-1023</p> | <p>Hay una ruta de acceso de archivo no válida.</p> | 
| <p>JET_errInvalidSystemPath<br />-1024</p> | <p>Hay una ruta de acceso del sistema no válida.</p> | 
| <p>JET_errInvalidLogDirectory<br />-1025</p> | <p>Hay un directorio de registro no válido.</p> | 
| <p>JET_errRecordTooBig<br />-1026</p> | <p>El registro es mayor que el tamaño máximo.</p> | 
| <p>JET_errTooManyOpenDatabases<br />-1027</p> | <p>Hay demasiadas bases de datos abiertas.</p> | 
| <p>JET_errInvalidDatabase<br />-1028</p> | <p>No se trata de un archivo de base de datos.</p> | 
| <p>JET_errNotInitialized<br />-1029</p> | <p>El motor de base de datos no se ha inicializado.</p> | 
| <p>JET_errAlreadyInitialized<br />-1030</p> | <p>El motor de base de datos ya está inicializado.</p> | 
| <p>JET_errInitInProgress<br />-1031</p> | <p>Se está inicializando el motor de base de datos.</p> | 
| <p>JET_errFileAccessDenied<br />-1032</p> | <p>No se puede acceder al archivo porque está bloqueado o en uso.</p> | 
| <p>JET_errBufferTooSmall<br />-1038</p> | <p>El búfer es demasiado pequeño.</p> | 
| <p>JET_errTooManyColumns<br />-1040</p> | <p>Se definen demasiadas columnas.</p> | 
| <p>JET_errContainerNotEmpty<br />-1043</p> | <p>El contenedor no está vacío.</p> | 
| <p>JET_errInvalidFilename<br />-1044</p> | <p>El nombre de archivo no es válido.</p> | 
| <p>JET_errInvalidBookmark<br />-1045</p> | <p>Hay un marcador no válido.</p> | 
| <p>JET_errColumnInUse<br />-1046</p> | <p>La columna utilizada está en un índice.</p> | 
| <p>JET_errInvalidBufferSize<br />-1047</p> | <p>El búfer de datos no coincide con el tamaño de columna.</p> | 
| <p>JET_errColumnNotUpdatable<br />-1048</p> | <p>No se puede establecer el valor de columna.</p> | 
| <p>JET_errIndexInUse<br />-1051</p> | <p>El índice está en uso.</p> | 
| <p>JET_errLinkNotSupported<br />-1052</p> | <p>La compatibilidad con vínculos no está disponible.</p> | 
| <p>JET_errNullKeyDisallowed<br />-1053</p> | <p>No se permiten claves NULL en un índice.</p> | 
| <p>JET_errNotInTransaction<br />-1054</p> | <p>La operación debe producirse dentro de una transacción.</p> | 
| <p>JET_errTooManyActiveUsers<br />-1059</p> | <p>Hay demasiados usuarios activos de base de datos</p> | 
| <p>JET_errInvalidCountry<br />-1061</p> | <p>Hay un código de país no válido o desconocido.</p> | 
| <p>JET_errInvalidLanguageId<br />-1062</p> | <p>Hay un identificador de idioma no válido o desconocido.</p> | 
| <p>JET_errInvalidCodePage<br />-1063</p> | <p>Hay una página de códigos no válida o desconocida.</p> | 
| <p>JET_errInvalidLCMapStringFlags<br />-1064</p> | <p>Se usan marcas no válidas para <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString.</a></p> | 
| <p>JET_errVersionStoreEntryTooBig<br />-1065</p> | <p>Se intentó crear una entrada de almacén de versiones (RCE) mayor que un cubo de versión.</p> | 
| <p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />-1066</p> | <p>El almacén de versiones está sin memoria y no se pudo completar el intento de limpieza.</p> | 
| <p>JET_errVersionStoreOutOfMemory<br />-1069</p> | <p>El almacén de versiones está sin memoria y ya se ha intentado realizar una limpieza).</p> | 
| <p>JET_errCannotIndex<br />-1071</p> | <p>Las columnas escrow y SLV no se pueden indexar.</p> | 
| <p>JET_errRecordNotDeleted<br />-1072</p> | <p>El registro no se ha eliminado.</p> | 
| <p>JET_errTooManyMempoolEntries<br />-1073</p> | <p>Se han solicitado demasiadas entradas mempool.</p> | 
| <p>JET_errOutOfObjectIDs<br />-1074</p> | <p>La base de datos está fuera de los ObjectID del árbol B+, por lo que se debe realizar una desfragmentación sin conexión para reclamar objectIds libres o no usados.</p> | 
| <p>JET_errOutOfLongValueIDs<br />-1075</p> | <p>El contador id. de valor largo ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para reclamar valores LongValueID gratuitos o no usados.</p> | 
| <p>JET_errOutOfAutoincrementValues<br />-1076</p> | <p>El contador de incremento automático ha alcanzado el valor máximo. Una desfragmentación sin conexión no podrá reclamar valores de incremento automático libres o no usados).</p> | 
| <p>JET_errOutOfDbtimeValues<br />-1077</p> | <p>El contador Dbtime ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para reclamar valores Dbtime libres o no usados.</p> | 
| <p>JET_errOutOfSequentialIndexValues<br />-1078</p> | <p>Un contador de índice secuencial ha alcanzado el valor máximo. Se debe realizar una desfragmentación sin conexión para reclamar valores SequentialIndex libres o no usados.</p> | 
| <p>JET_errRunningInOneInstanceMode<br />-1080</p> | <p>Esta llamada a varias instancias tiene habilitado el modo de instancia única.</p> | 
| <p>JET_errRunningInMultiInstanceMode<br />-1081</p> | <p>Esta llamada de instancia única tiene habilitado el modo de instancias múltiples.</p> | 
| <p>JET_errSystemParamsAlreadySet<br />-1082</p> | <p>Ya se han establecido los parámetros globales del sistema.</p> | 
| <p>JET_errSystemPathInUse<br />-1083</p> | <p>Otra instancia de base de datos ya está utilizando la ruta de acceso del sistema.</p> | 
| <p>JET_errLogFilePathInUse<br />-1084</p> | <p>Otra instancia de base de datos ya está utilizando la ruta de acceso del archivo de registro.</p> | 
| <p>JET_errTempPathInUse<br />-1085</p> | <p>Otra instancia de base de datos ya está utilizando la ruta de acceso a la base de datos temporal.</p> | 
| <p>JET_errInstanceNameInUse<br />-1086</p> | <p>El nombre de instancia ya está en uso.</p> | 
| <p>JET_errInstanceUnavailable<br />-1090</p> | <p>Esta instancia no se puede usar porque encontró un error irresal.</p> | 
| <p>JET_errDatabaseUnavailable<br />-1091</p> | <p>Esta base de datos no se puede usar porque encontró un error irresal.</p> | 
| <p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />-1092</p> | <p>Esta instancia no se puede usar porque encontró un error de disco de registro completo al realizar una operación (por ejemplo, una reversión de transacciones) que no pudo tolerar errores.</p> | 
| <p>JET_errOutOfSessions<br />-1101</p> | <p>La base de datos está fuera de las sesiones.</p> | 
| <p>JET_errWriteConflict<br />-1102</p> | <p>Error en el bloqueo de escritura debido a la existencia de un bloqueo de escritura pendiente.</p> | 
| <p>JET_errTransTooDeep<br />-1103</p> | <p>Las transacciones están anidadas demasiado profundamente.</p> | 
| <p>JET_errInvalidSesid<br />-1104</p> | <p>Hay un identificador de sesión no válido.</p> | 
| <p>JET_errWriteConflictPrimaryIndex<br />-1105</p> | <p>Se intentó realizar una actualización en un índice principal no confirmado.</p> | 
| <p>JET_errInTransaction<br />-1108</p> | <p>La operación no se permite dentro de una transacción.</p> | 
| <p>JET_errRollbackRequired<br />-1109</p> | <p>La transacción actual debe revertirse. No se puede confirmado y no se puede iniciar uno nuevo.</p> | 
| <p>JET_errTransReadOnly<br />-1110</p> | <p>Una transacción de solo lectura intentó modificar la base de datos.</p> | 
| <p>JET_errSessionWriteConflict<br />-1111</p> | <p>Se intentó reemplazar el mismo registro por dos cursores diferentes en la misma sesión.</p> | 
| <p>JET_errRecordTooBigForBackwardCompatibility<br />-1112</p> | <p>El registro sería demasiado grande si se representa en un formato de base de datos de una versión anterior de Jet.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort<br />-1113</p> | <p>No se pudo crear la tabla temporal debido a parámetros que entren en conflicto con JET_bitTTForwardOnly.</p> | 
| <p>JET_errSesidTableIdMismatch<br />-1114</p> | <p>El identificador de sesión no se puede usar con el identificador de tabla porque no se usó para crearlo.</p> | 
| <p>JET_errInvalidInstance<br />-1115</p> | <p>El identificador de instancia no es válido o hace referencia a una instancia que se ha cerrado.</p> | 
| <p>JET_errReadLostFlushVerifyFailure<br />-1119</p> | <p>La página de base de datos leía desde el disco tenía una escritura anterior no representada en la página. Disponible en Windows 8 y versiones posteriores para el cliente, y Windows Server 2012 y versiones posteriores para el servidor.</p> | 
| <p>JET_errDatabaseDuplicate<br />-1201</p> | <p>La base de datos ya existe.</p> | 
| <p>JET_errDatabaseInUse<br />-1202</p> | <p>Base de datos en uso.</p> | 
| <p>JET_errDatabaseNotFound<br />-1203</p> | <p>No hay ninguna base de datos de este tipo.</p> | 
| <p>JET_errDatabaseInvalidName<br />-1204</p> | <p>El nombre de la base de datos no es válido.</p> | 
| <p>JET_errDatabaseInvalidPages<br />-1205</p> | <p>Hay un número de páginas no válido.</p> | 
| <p>JET_errDatabaseCorrupted<br />-1206</p> | <p>Hay un archivo que no es de base de datos o una base de datos dañada.</p> | 
| <p>JET_errDatabaseLocked<br />-1207</p> | <p>La base de datos está bloqueada exclusivamente.</p> | 
| <p>JET_errCannotDisableVersioning<br />-1208</p> | <p>No se puede deshabilitar el control de versiones de esta base de datos.</p> | 
| <p>JET_errInvalidDatabaseVersion<br />-1209</p> | <p>El motor de base de datos no es compatible con la base de datos.</p> | 
| <p>JET_errDatabase200Format<br />-1210</p> | <p>La base de datos está en un formato anterior (200). JetInit devuelve <a href="gg294068(v=exchg.10).md"></a> este error <a href="gg269337(v=exchg.10).md">si JET_paramCheckFormatWhenOpenFail</a> está establecido. Windows Solo cliente NT.</p> | 
| <p>JET_errDatabase400Format<br />-1211</p> | <p>La base de datos está en un formato anterior (400). JetInit devuelve <a href="gg294068(v=exchg.10).md"></a> este error <a href="gg269337(v=exchg.10).md">si JET_paramCheckFormatWhenOpenFail</a> está establecido. Windows Solo cliente NT.</p> | 
| <p>JET_errDatabase500Format<br />-1212</p> | <p>La base de datos tiene un formato anterior (500). JetInit devuelve <a href="gg294068(v=exchg.10).md"></a> este error <a href="gg269337(v=exchg.10).md">si JET_paramCheckFormatWhenOpenFail</a> está establecido. Windows Solo cliente NT.</p> | 
| <p>JET_errPageSizeMismatch<br />-1213</p> | <p>El tamaño de página de la base de datos no coincide con el motor.</p> | 
| <p>JET_errTooManyInstances<br />-1214</p> | <p>No se pueden iniciar más instancias de base de datos.</p> | 
| <p>JET_errDatabaseSharingViolation<br />-1215</p> | <p>Una instancia de base de datos diferente usa esta base de datos.</p> | 
| <p>JET_errAttachedDatabaseMismatch<br />-1216</p> | <p>Se ha detectado un dato adjunto pendiente de la base de datos al principio o al final de la recuperación, pero falta la base de datos o no coincide con la información de los datos adjuntos.</p> | 
| <p>JET_errDatabaseInvalidPath<br />-1217</p> | <p>La ruta de acceso especificada al archivo de base de datos no es válida.</p> | 
| <p>JET_errDatabaseIdInUse<br />-1218</p> | <p>A una base de datos se le asigna un identificador que ya está en uso.</p> | 
| <p>JET_errForceDetachNotAllowed<br />-1219</p> | <p>La desasoción por fuerza solo se permite después de que se detuvo la desasoción normal debido a un error.</p> | 
| <p>JET_errCatalogCorrupted<br />-1220</p> | <p>Se detectaron daños en el catálogo.</p> | 
| <p>JET_errPartiallyAttachedDB<br />-1221</p> | <p>La base de datos solo está parcialmente adjuntada y no se puede completar la operación de asociación.</p> | 
| <p>JET_errDatabaseSignInUse<br />-1222</p> | <p>La base de datos con la misma firma ya está en uso.</p> | 
| <p>JET_errDatabaseCorruptedNoRepair<br />-1224</p> | <p>La base de datos está dañada, pero no se permite una reparación.</p> | 
| <p>JET_errInvalidCreateDbVersion<br />-1225</p> | <p>El motor de base de datos intentó reproducir una operación Crear base de datos del registro de transacciones, pero no se pudo realizar debido a una versión incompatible de esa operación.</p> | 
| <p>JET_errTableLocked<br />-1302</p> | <p>La tabla está bloqueada exclusivamente.</p> | 
| <p>JET_errTableDuplicate<br />-1303</p> | <p>La tabla ya existe.</p> | 
| <p>JET_errTableInUse<br />-1304</p> | <p>La tabla está en uso y no se puede bloquear.</p> | 
| <p>JET_errObjectNotFound<br />-1305</p> | <p>No hay ninguna tabla u objeto de este tipo.</p> | 
| <p>JET_errDensityInvalid<br />-1307</p> | <p>Hay una densidad de índice o archivo no es buena.</p> | 
| <p>JET_errTableNotEmpty<br />-1308</p> | <p>La tabla no está vacía.</p> | 
| <p>JET_errInvalidTableId<br />-1310</p> | <p>El identificador de tabla no es válido.</p> | 
| <p>JET_errTooManyOpenTables<br />-1311</p> | <p>No se pueden abrir más tablas, incluso después de que se haya ejecutado la tarea de limpieza interna.</p> | 
| <p>JET_errIllegalOperation<br />-1312</p> | <p>La operación no se admite en la tabla.</p> | 
| <p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />-1313</p> | <p>No se pueden abrir más tablas porque no se pudo completar el intento de limpieza.</p> | 
| <p>JET_errObjectDuplicate<br />-1314</p> | <p>El nombre de la tabla o del objeto está en uso.</p> | 
| <p>JET_errInvalidObject<br />-1316</p> | <p>El objeto no es válido para la operación.</p> | 
| <p>JET_errCannotDeleteTempTable<br />-1317</p> | <p><a href="gg294087(v=exchg.10).md">JetCloseTable debe</a> usarse en lugar de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> para eliminar una tabla temporal.</p> | 
| <p>JET_errCannotDeleteSystemTable<br />-1318</p> | <p>Hubo un intento no ilegal de eliminar una tabla del sistema.</p> | 
| <p>JET_errCannotDeleteTemplateTable<br />-1319</p> | <p>Se ha intentado eliminar una tabla de plantillas de forma no ilegal.</p> | 
| <p>JET_errExclusiveTableLockRequired<br />-1322</p> | <p>Debe haber un bloqueo exclusivo en la tabla.</p> | 
| <p>JET_errFixedDDL<br />-1323</p> | <p>Las operaciones DDL están prohibidas en esta tabla.</p> | 
| <p>JET_errFixedInheritedDDL<br />-1324</p> | <p>En una tabla derivada, las operaciones DDL están prohibidas en la parte heredada del DDL.</p> | 
| <p>JET_errCannotNestDDL<br />-1325</p> | <p>Actualmente no se admite el anidamiento del DDL jerárquico.</p> | 
| <p>JET_errDDLNotInheritable<br />-1326</p> | <p>Se intentó heredar un DDL de una tabla que no está marcada como una tabla de plantilla.</p> | 
| <p>JET_errInvalidSettings<br />-1328</p> | <p>Los parámetros del sistema se han establecido incorrectamente.</p> | 
| <p>JET_errClientRequestToStopJetService<br />-1329</p> | <p>El cliente ha solicitado que se detenga el servicio.</p> | 
| <p>JET_errCannotAddFixedVarColumnToDerivedTable<br />-1330</p> | <p>La tabla Template se creó con la marca NoFixedVarColumnsInDerivedTables establecida.</p> | 
| <p>JET_errIndexCantBuild<br />-1401</p> | <p>Error en la compilación del índice.</p> | 
| <p>JET_errIndexHasPrimary<br />-1402</p> | <p>El índice principal ya está definido.</p> | 
| <p>JET_errIndexDuplicate<br />-1403</p> | <p>El índice ya está definido.</p> | 
| <p>JET_errIndexNotFound<br />-1404</p> | <p>No hay ningún índice de este tipo.</p> | 
| <p>JET_errIndexMustStay<br />-1405</p> | <p>No se puede eliminar el índice clúster.</p> | 
| <p>JET_errIndexInvalidDef<br />-1406</p> | <p>La definición del índice no es válida.</p> | 
| <p>JET_errInvalidCreateIndex<br />-1409</p> | <p>La creación de la descripción del índice no era válida.</p> | 
| <p>JET_errTooManyOpenIndexes<br />-1410</p> | <p>La base de datos está fuera de los bloques de descripción del índice.</p> | 
| <p>JET_errMultiValuedIndexViolation<br />-1411</p> | <p>Se han generado claves de índice entre registros no únicas para un índice con varios valores.</p> | 
| <p>JET_errIndexBuildCorrupted<br />-1412</p> | <p>Índice secundario que refleja correctamente que el índice principal no se pudo compilar.</p> | 
| <p>JET_errPrimaryIndexCorrupted<br />-1413</p> | <p>El índice principal está dañado y la base de datos se debe desfragmentar.</p> | 
| <p>JET_errSecondaryIndexCorrupted<br />-1414</p> | <p>El índice secundario está dañado y la base de datos se debe desfragmentar.</p> | 
| <p>JET_errInvalidIndexId<br />-1416</p> | <p>El identificador de índice no es válido.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly<br />-1430</p> | <p>El índice de tupla solo se puede establecer en un índice secundario.</p> | 
| <p>JET_errIndexTuplesTooManyColumns<br />-1431</p> | <p>La definición de índice para el índice de tupla contiene más columnas de clave que el motor de base de datos puede admitir.</p><p><strong>Nota  </strong> El JET_errIndexTuplesOneColumnOnly error está obsoleto y se ha reemplazado por JET_errIndexTuplesTooManyColumns.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly<br />-1432</p> | <p>El índice de tupla debe ser un índice no único.</p> | 
| <p>JET_errIndexTuplesTextBinaryColumnsOnly<br />-1433</p> | <p>Una definición de índice de tupla solo puede contener columnas de clave que tengan tipos de columna binarios o de texto.</p><p><strong>Nota  </strong> El JET_errIndexTuplesTextColumnsOnly error está obsoleto y se ha reemplazado por JET_errIndexTuplesTextBinaryColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed<br />-1434</p> | <p>El índice de tupla no permite establecer cbVarSegMac.</p> | 
| <p>JET_errIndexTuplesInvalidLimits<br />-1435</p> | <p>La longitud mínima o máxima de la tupla o el número máximo de caracteres especificados para un índice no son válidos.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex<br />-1436</p> | <p>No se puede llamar a <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> con la JET_bitRetrieveFromIndex establecida al recuperar una columna en un índice de tupla.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall<br />-1437</p> | <p>La clave especificada no cumple la longitud mínima de tupla.</p> | 
| <p>JET_errColumnLong<br />-1501</p> | <p>El valor de la columna es long.</p> | 
| <p>JET_errColumnNoChunk<br />-1502</p> | <p>No hay ningún fragmento de este tipo en un valor largo.</p> | 
| <p>JET_errColumnDoesNotFit<br />-1503</p> | <p>El campo no cabe en el registro.</p> | 
| <p>JET_errNullInvalid<br />-1504</p> | <p>Null no es válido.</p> | 
| <p>JET_errColumnIllegalNull<br />JET_errNullInvalid</p> | <p>Null no es válido. El administrador de registros devuelve este error.</p> | 
| <p>JET_errColumnIndexed -1505</p> | <p>La columna está indexada y no se puede eliminar.</p> | 
| <p>JET_errColumnTooBig -1506</p> | <p>La longitud del campo es mayor que la longitud máxima permitida.</p> | 
| <p>JET_errColumnNotFound -1507</p> | <p>No hay ninguna columna de este tipo.</p> | 
| <p>JET_errColumnDuplicate -1508</p> | <p>Este campo ya está definido.</p> | 
| <p>JET_errMultiValuedColumnMustBeTagged -1509</p> | <p>Se intentó crear una columna de varios valores, pero la columna no se etiquetó.</p> | 
| <p>JET_errColumnRedundant -1510</p> | <p>Hubo una segunda columna de incremento automático o versión.</p> | 
| <p>JET_errInvalidColumnType -1511</p> | <p>El tipo de datos de columna no es válido.</p> | 
| <p>JET_errTaggedNotNULL -1514</p> | <p>No hay columnas etiquetadas que no sean NULL.</p> | 
| <p>JET_errNoCurrentIndex -1515</p> | <p>La base de datos no es válida porque no contiene un índice actual.</p> | 
| <p>JET_errKeyIsMade -1516</p> | <p>La clave está completamente realizada.</p> | 
| <p>JET_errBadColumnId -1517</p> | <p>El identificador de columna es incorrecto.</p> | 
| <p>JET_errBadItagSequence -1518</p> | <p>Hay una itagSequence mal para la columna etiquetada.</p> | 
| <p>JET_errColumnInRelationship -1519</p> | <p>No se puede eliminar una columna porque forma parte de una relación.</p> | 
| <p>JET_errCannotBeTagged -1521</p> | <p>El incremento automático y la versión no se pueden etiquetar.</p> | 
| <p>JET_errDefaultValueTooBig -1524</p> | <p>El valor predeterminado supera el tamaño máximo.</p> | 
| <p>JET_errMultiValuedDuplicate -1525</p> | <p>Se detectó un valor duplicado en una columna única de varios valores.</p> | 
| <p>JET_errLVCorrupted -1526</p> | <p>Se encontraron daños en un árbol de valores largos.</p> | 
| <p>JET_errMultiValuedDuplicateAfterTruncation -1528</p> | <p>Se detectó un valor duplicado en una columna única de varios valores después de normalizar los datos y se están normalizando truncando los datos antes de la comparación.</p> | 
| <p>JET_errDerivedColumnCorruption -1529</p> | <p>Hay una columna no válida en la tabla derivada.</p> | 
| <p>JET_errInvalidPlaceholderColumn -1530</p> | <p>Se intentó convertir una columna en un marcador de posición de índice principal, pero la columna no cumple los criterios necesarios.</p> | 
| <p>JET_errRecordNotFound -1601</p> | <p>No se encontró la clave.</p> | 
| <p>JET_errRecordNoCopy -1602</p> | <p>No hay ningún búfer de trabajo.</p> | 
| <p>JET_errNoCurrentRecord -1603</p> | <p>No hay ningún registro actual.</p> | 
| <p>JET_errRecordPrimaryChanged -1604</p> | <p>Es posible que la clave principal no cambie.</p> | 
| <p>JET_errKeyDuplicate -1605</p> | <p>Hay una clave duplicada no ilegal.</p> | 
| <p>JET_errAlreadyPrepared -1607</p> | <p>Se intentó actualizar un registro mientras ya había una actualización de registros en curso.</p> | 
| <p>JET_errKeyNotMade -1608</p> | <p>No se realizó una llamada <a href="gg269329(v=exchg.10).md">a JetMakeKey.</a></p> | 
| <p>JET_errUpdateNotPrepared -1609</p> | <p>No se realizó una llamada <a href="gg269339(v=exchg.10).md">a JetPrepareUpdate</a>.</p> | 
| <p>JET_errDataHasChanged -1611</p> | <p>Los datos han cambiado y se anuló la operación.</p> | 
| <p>JET_errLanguageNotSupported -1619</p> | <p>Esta Windows instalación no admite el idioma seleccionado.</p> | 
| <p>JET_errTooManySorts -1701</p> | <p>Hay demasiados procesos de ordenación.</p> | 
| <p>JET_errInvalidOnSort -1702</p> | <p>Se produjo una operación no válida durante una ordenación.</p> | 
| <p>JET_errTempFileOpenError -1803</p> | <p>No se pudo abrir el archivo temporal.</p> | 
| <p>JET_errTooManyAttachedDatabases -1805</p> | <p>Hay demasiadas bases de datos abiertas.</p> | 
| <p>JET_errDiskFull -1808</p> | <p>No queda espacio en el disco.</p> | 
| <p>JET_errPermissionDenied -1809</p> | <p>Se deniega el permiso.</p> | 
| <p>JET_errFileNotFound -1811</p> | <p>No se encontró el archivo.</p> | 
| <p>JET_errFileInvalidType -1812</p> | <p>El tipo de archivo no es válido.</p> | 
| <p>JET_errAfterInitialization -1850</p> | <p>No se puede iniciar una restauración después de la inicialización.</p> | 
| <p>JET_errLogCorrupted -1852</p> | <p>No se pudieron interpretar los registros.</p> | 
| <p>JET_errInvalidOperation -1906</p> | <p>La operación no es válida.</p> | 
| <p>JET_errAccessDenied -1907</p> | <p>Acceso denegado.</p> | 
| <p>JET_errTooManySplits -1909</p> | <p>División infinita.</p> | 
| <p>JET_errSessionSharingViolation -1910</p> | <p>Varios subprocesos usan la misma sesión.</p> | 
| <p>JET_errEntryPointNotFound -1911</p> | <p>No se encontró un punto de entrada en un archivo DLL necesario.</p> | 
| <p>JET_errSessionContextAlreadySet -1912</p> | <p>La sesión especificada ya tiene un conjunto de contextos de sesión.</p> | 
| <p>JET_errSessionContextNotSetByThisThread -1913</p> | <p>Se intentó restablecer el contexto de sesión, pero el subproceso actual no fue el original que estableció el contexto de sesión.</p> | 
| <p>JET_errSessionInUse -1914</p> | <p>Se intentó finalizar la sesión actualmente en uso.</p> | 
| <p>JET_errRecordFormatConversionFailed -1915</p> | <p>Error interno durante una conversión de formato de registro dinámico.</p> | 
| <p>JET_errOneDatabasePerSession -1916</p> | <p>Solo se permite una base de datos de usuario abierta por sesión (como se indica estableciendo la <a href="gg269337(v=exchg.10).md">marca JET_paramOneDatabasePerSession</a> durante la creación de la base de datos).</p> | 
| <p>JET_errRollbackError -1917</p> | <p>Se produjo un error durante la reversión.</p> | 
| <p>JET_errCallbackFailed -2101</p> | <p>Error en una llamada de función de devolución de llamada.</p> | 
| <p>JET_errCallbackNotResolved -2102</p> | <p>No se encontró una función de devolución de llamada.</p> | 
| <p>JET_errOSSnapshotInvalidSequence -2401</p> | <p>La API de instantáneas del sistema operativo se usó en una secuencia no válida.</p> | 
| <p>JET_errOSSnapshotTimeOut -2402</p> | <p>La instantánea del sistema operativo finalizó con un tiempo de espera.</p> | 
| <p>JET_errOSSnapshotNotAllowed -2403</p> | <p>No se permite la instantánea del sistema operativo porque hay una copia de seguridad o recuperación en en curso.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId -2404</p> | <p>Error en la operación porque el identificador de instantáneas del sistema operativo especificado no era válido.</p> | 
| <p>JET_errLSCallbackNotSpecified -3000</p> | <p>Se intentó usar el almacenamiento local sin especificar una función de devolución de llamada.</p> | 
| <p>JET_errLSAlreadySet -3001</p> | <p>Se intentó establecer el almacenamiento local para un objeto que ya lo tenía establecido.</p> | 
| <p>JET_errLSNotSet -3002</p> | <p>Se intentó recuperar el almacenamiento local de un objeto que no tenía establecido.</p> | 
| <p>JET_errFileIOSparse -4000</p> | <p>Error en una operación de E/S porque se intentó en una región sin asignar de un archivo.</p> | 
| <p>JET_errFileIOBeyondEOF -4001</p> | <p>Se emitió una lectura en una ubicación más allá del EOF (las escrituras expandirán el archivo).</p> | 
| <p>JET_errFileIOAbort -4002</p> | <p>Esta marca indica al autor JET_ABORTRETRYFAILCALLBACK que anule la E/S especificada.</p> | 
| <p>JET_errFileIORetry -4003</p> | <p>Esta marca indica al autor JET_ABORTRETRYFAILCALLBACK que vuelva a intentar la E/S especificada.</p> | 
| <p>JET_errFileIOFail -4004</p> | <p>Esta marca indica al autor JET_ABORTRETRYFAILCALLBACK que no se haya producido un error en la E/S especificada.</p> | 
| <p>JET_errFileCompressed -4005</p> | <p>El acceso de lectura y escritura no se admite en archivos comprimidos.</p> | 



### <a name="remarks"></a>Comentarios

En general, un valor mayor que cero debe interpretarse como una advertencia, un valor de cero debe interpretarse como correcto y un valor menor que cero debe interpretarse como un error. Una aplicación no debe confiar en ningún otro patrón de estos valores, como los intervalos de valores.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores extensibles Storage motor de ejecución](./extensible-storage-engine-errors.md)  
[Archivos extensibles Storage engine](./extensible-storage-engine-files.md)
