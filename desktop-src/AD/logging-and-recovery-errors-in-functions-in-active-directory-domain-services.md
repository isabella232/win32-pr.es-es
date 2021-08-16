---
title: Errores de registro y recuperación en Functions en Active Directory Domain Services
description: En este tema se enumeran los valores devueltos de errores de registro y recuperación para las funciones Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory registro y errores de recuperación de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b267b359b5244fddc0e8a9b2ddfbfb5d6e5f9ab0a7e647683d44759f8a7261b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186597"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Errores de registro y recuperación en Functions en Active Directory Domain Services

En este tema se enumeran los valores devueltos de errores de registro y recuperación para las funciones Active Directory Domain Services.



| Valor                                | Descripción                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | El archivo de registro está dañado.                                                                                                         |
| **hrNoBackupDirectory**              | No se ha especificado ningún directorio de copia de seguridad.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | El directorio de copia de seguridad no está vacío.                                                                                               |
| **hrBackupInProgress**               | La copia de seguridad está activa.                                                                                                                |
| **hrMissingPreviousLogFile**         | Falta un archivo de registro para el punto de control.                                                                                        |
| **hrLogWriteFail**                   | No se puede escribir en el archivo de registro.                                                                                                 |
| **hrBadLogVersion**                  | La versión del archivo de registro no es compatible con la versión de la base de datos nt/Windows del servicio de directorio (NTDS) de Windows 2000. |
| **hrInvalidLogSequence**             | La marca de tiempo del siguiente registro no coincide con lo esperado.                                                                 |
| **hrLoggingDisabled**                | El registro no está activo.                                                                                                           |
| **hrLogBufferTooSmall**              | El búfer de registro es demasiado pequeño para recuperarse.                                                                                     |
| **hrLogSequenceEnd**                 | Se ha superado el número máximo de archivos de registro.                                                                               |
| **hrNoBackup**                       | No hay ninguna copia de seguridad en curso.                                                                                                  |
| **hrInvalidBackupSequence**          | La llamada de copia de seguridad está fuera de secuencia.                                                                                              |
| **hrBackupNotAllowedYet**            | No se puede realizar una copia de seguridad ahora.                                                                                                  |
| **hrDeleteBackupFileFail**           | No se puede eliminar el archivo de copia de seguridad.                                                                                                |
| **hrMakeBackupDirectoryFail**        | No se puede crear un directorio temporal de copia de seguridad.                                                                                     |
| **hrInvalidBackup**                  | No se puede realizar una copia de seguridad incremental cuando se habilita el registro circular.                                                      |
| **hrRecoveredWithErrors**            | Se encontraron errores durante el proceso de reparación.                                                                               |
| **hrMissingLogFile**                 | Falta el archivo de registro actual.                                                                                                 |
| **hrLogDiskFull**                    | El disco de registro está lleno.                                                                                                            |
| **hrBadLogSignature**                | Un archivo de registro está dañado.                                                                                                           |
| **hrBadDbSignature**                 | Un archivo de base de datos está dañado.                                                                                                      |
| **hrBadCheckpointSignature**         | Un archivo de punto de comprobación está dañado.                                                                                                    |
| **hrCheckpointCorrupt**              | No se pudo encontrar un archivo de punto de comprobación o está dañado.                                                                       |
| **hrDatabaseInconsistent**           | La base de datos está dañada.                                                                                                         |
| **hrConsistentTimeMismatch**         | Hay un error de coincidencia en la hora de la última coherencia de la base de datos.                                                                      |
| **hrPatchFileMismatch**              | El archivo de revisión no se genera a partir de esta copia de seguridad.                                                                                |
| **hrRestoreLogTooLow**               | El número de registro inicial es demasiado bajo para la restauración.                                                                              |
| **hrRestoreLogTooHigh**              | El número de registro inicial es demasiado alto para la restauración.                                                                             |
| **hrGivenLogFileHasBadSignature**    | El archivo de registro descargado de la cinta está dañado.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | No se puede encontrar un archivo de registro obligatorio después de descargar la cinta.                                                               |
| **hrMissingRestoreLogFiles**         | Los datos no se restauran completamente porque faltan algunos archivos de registro.                                                               |
| **hrExistingLogFileHasBadSignature** | El archivo de registro de la ruta de acceso del archivo de registro está dañado.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | No se puede encontrar un archivo de registro obligatorio en la ruta de acceso del archivo de registro.                                                                        |
| **hrMissingFullBackup**              | La base de datos omitía una copia de seguridad completa anterior antes de la copia de seguridad incremental.                                                        |
| **hrBadBackupDatabaseSize**          | El tamaño de la base de datos de copia de seguridad debe ser un múltiplo de 4000 (4096 bytes).                                                                |
| **hrTermInProgress**                 | La base de datos se está cerrando.                                                                                                 |
| **hrFeatureNotAvailable**            | La característica no está disponible.                                                                                                    |
| **hrInvalidName**                    | El nombre no es válido.                                                                                                             |
| **hrInvalidParameter**               | El parámetro no es válido.                                                                                                        |
| **hrColumnNull**                     | El valor de la columna es NULL.                                                                                                 |
| **hrBufferTruncated**                | El búfer es demasiado pequeño para los datos.                                                                                                |
| **hrDatabaseAttached**               | La base de datos ya está adjunta.                                                                                                |
| **hrInvalidDatabaseId**              | El identificador de la base de datos no es válido.                                                                                                      |
| **hrOutOfMemory**                    | El equipo está sin memoria.                                                                                                   |
| **hrOutOfDatabaseSpace**             | La base de datos ha alcanzado el tamaño máximo de 16 GB.                                                                              |
| **hrOutOfCursors**                   | Cursores fuera de la tabla.                                                                                                            |
| **hrOutOfBuffers**                   | Búferes de página fuera de la base de datos.                                                                                                    |
| **hrTooManyIndexes**                 | Hay demasiados índices.                                                                                                      |
| **hrTooManyKeys**                    | Hay demasiadas columnas en un índice.                                                                                          |
| **hrRecordDeleted**                  | El registro se ha eliminado.                                                                                                     |
| **hrReadVerifyFailure**              | Error de comprobación de lectura.                                                                                              |
| **hrOutOfFileHandles**               | No hay identificadores de archivo disponibles.                                                                                                             |
| **hrDiskIO**                         | Error de E/S de disco.                                                                                                       |
| **hrInvalidPath**                    | La ruta de acceso al archivo no es válida.                                                                                                 |
| **hrRecordTooBig**                   | El registro ha superado el tamaño máximo.                                                                                        |
| **hrTooManyOpenDatabases**           | Hay demasiadas bases de datos abiertas.                                                                                               |
| **hrInvalidDatabase**                | El archivo no es un archivo de base de datos.                                                                                                 |
| **hrNotInitialized**                 | Todavía no se llamó a la base de datos.                                                                                                 |
| **hrAlreadyInitialized**             | Ya se llamó a la base de datos.                                                                                                 |
| **hrFileAccessDenied**               | No se puede acceder al archivo.                                                                                                       |
| **hrBufferTooSmall**                 | El búfer es demasiado pequeño.                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE o SeekGE no pueden encontrar una coincidencia exacta.                                                                              |
| **hrTooManyColumns**                 | Hay demasiadas columnas definidas.                                                                                              |
| **hrContainerNotEmpty**              | El contenedor no está vacío.                                                                                                      |
| **hrInvalidFilename**                | El nombre de archivo no es válido.                                                                                                         |
| **hrInvalidBookmark**                | El marcador no es válido.                                                                                                         |
| **hrColumnInUse**                    | La columna se usa en un índice.                                                                                                  |
| **hrInvalidBufferSize**              | El búfer de datos no coincide con el tamaño de columna.                                                                                  |
| **hrColumnNotUpdatable**             | No se puede establecer el valor de columna.                                                                                                  |
| **hrIndexInUse**                     | El índice está en uso.                                                                                                             |
| **hrNullKeyDisallowed**              | No se permiten claves NULL en un índice.                                                                                           |
| **hrNotInTransaction**               | La operación debe estar dentro de una transacción.                                                                                      |
| **hrNoIdleActivity**                 | No se ha producido ninguna actividad inactiva.                                                                                                       |
| **hrTooManyActiveUsers**             | Hay demasiados usuarios de base de datos activos.                                                                                        |
| **hrInvalidCountry**                 | El código de país o región no se conoce o no es válido.                                                                    |
| **hrInvalidLanguageId**              | El identificador de idioma no se conoce o no es válido.                                                                               |
| **hrInvalidCodePage**                | La página de códigos no se conoce o no es válida.                                                                                 |
| **hrNoWriteLock**                    | No hay ningún bloqueo de escritura en el nivel de transacción 0.                                                                                   |
| **hrColumnSetNull**                  | El valor de columna se establece en NULL.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | lMaxVerPages superó (solo XJET).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Fuera de cursores.                                                                                                                  |
| **hrOutOfSessions**                  | Fuera de las sesiones.                                                                                                                 |
| **hrWriteConflict**                  | Error en el bloqueo de escritura debido a un bloqueo de escritura pendiente.                                                                          |
| **hrTransTooDeep**                   | Las transacciones están anidadas demasiado profundamente.                                                                                          |
| **hrInvalidSesid**                   | El identificador de sesión no es válido.                                                                                                   |
| **hrSessionWriteConflict**           | Otra sesión tiene una versión privada de la página.                                                                               |
| **hrInTransaction**                  | La operación no se permite dentro de una transacción.                                                                               |
| **hrDatabaseDuplicate**              | La base de datos ya existe.                                                                                                     |
| **hrDatabaseInUse**                  | La base de datos está en uso.                                                                                                          |
| **hrDatabaseNotFound**               | La base de datos no existe.                                                                                                     |
| **hrDatabaseInvalidName**            | El nombre de la base de datos no es válido.                                                                                                    |
| **hrDatabaseInvalidPages**           | El número de páginas no es válido.                                                                                                  |
| **hrDatabaseCorrupted**              | El archivo de base de datos está dañado o no se encuentra.                                                                          |
| **hrDatabaseLocked**                 | La base de datos está bloqueada.                                                                                                          |
| **hrTableEmpty**                     | Se ha abierto una tabla vacía.                                                                                                       |
| **hrTableLocked**                    | La tabla está bloqueada.                                                                                                             |
| **hrTableDuplicate**                 | La tabla ya existe.                                                                                                        |
| **hrTableInUse**                     | No se puede bloquear la tabla porque ya está en uso.                                                                           |
| **hrObjectNotFound**                 | La tabla u objeto no existe.                                                                                              |
| **hrCannotRename**                   | No se puede cambiar el nombre del archivo temporal.                                                                                             |
| **hrDensityInvalid**                 | La densidad de archivo/índice no es válida.                                                                                               |
| **hrTableNotEmpty**                  | No se puede definir el índice clúster.                                                                                            |
| **hrInvalidTableId**                 | El identificador de tabla no es válido.                                                                                                         |
| **hrTooManyOpenTables**              | No se pueden abrir más tablas.                                                                                                  |
| **hr HrGallgalOperation**               | La operación no se admite en las tablas.                                                                                        |
| **hrObjectDuplicate**                | Ya se está utilizando el nombre de tabla u objeto.                                                                                  |
| **hrInvalidObject**                  | El objeto no es válido para la operación.                                                                                             |
| **hrIndexCantBuild**                 | No se puede crear un índice clúster.                                                                                               |
| **hrIndexHasPrimary**                | El índice principal ya está definido.                                                                                            |
| **hrIndexDuplicate**                 | El índice ya está definido.                                                                                                    |
| **hrIndexNotFound**                  | El índice no existe.                                                                                                        |
| **hrIndexMustIndex**                  | No se puede eliminar un índice clúster.                                                                                              |
| **hrIndexInvalidDef**                | La definición de índice no es posible.                                                                                                 |
| **hrIndexHasClustered**              | El índice clúster ya está definido.                                                                                          |
| **hrCreateIndexFailed**              | No se puede crear el índice porque se produjo un error al crear una tabla.                                                     |
| **hrTooManyOpenIndexes**             | Bloques de descripción fuera del índice.                                                                                                 |
| **hrColumnLong**                     | El valor de la columna es demasiado largo.                                                                                                    |
| **hrColumnDoesNotFit**               | El campo no cabe en el registro.                                                                                            |
| **hrNullInvalid**                    | El valor no puede ser null.                                                                                                        |
| **hrColumnIndexed**                  | No se puede eliminar porque la columna está indexada.                                                                                  |
| **hrColumnTooBig**                   | La longitud del campo supera la longitud máxima de 255 bytes.                                                                 |
| **hrColumnNotFound**                 | No se encuentra la columna.                                                                                                       |
| **hrColumnDuplicate**                | El campo ya está definido.                                                                                                    |
| **hrColumn2ndSysMaint**              | Solo se permite una columna de incremento automático o de versión por tabla.                                                                  |
| **hrInvalidColumnType**              | El tipo de datos de columna no es válido.                                                                                                 |
| **hrColumnMaxTruncated**             | La columna se trunó porque superó la longitud máxima de 255 bytes.                                                    |
| **hrColumnCannotIndex**              | No se puede indexar una columna de valor largo.                                                                                             |
| **hrTaggedNotNULL**                  | Las columnas etiquetadas no pueden ser NULL.                                                                                                   |
| **hrNoCurrentIndex**                 | La entrada no es válida sin un índice actual.                                                                                    |
| **hrKeyIsMade**                      | La clave está completa.                                                                                                             |
| **hrBadColumnId**                    | El identificador de columna es incorrecto.                                                                                                      |
| **hrBadItagSequence**                | Hay un identificador de instancia no válido para una columna de varios valores.                                                                     |
| **hrCannotBeTagged**                 | AutoIncrement y Version no se pueden multivalor.                                                                                 |
| **hrRecordNotFound**                 | No se encuentra la clave.                                                                                                          |
| **hrNoCurrentRecord**                | La moneda no está en un registro.                                                                                                 |
| **hrRecordClusteredChanged**         | No se puede cambiar una clave en clúster.                                                                                               |
| **hrKeyDuplicate**                   | La clave ya existe.                                                                                                          |
| **hrAlreadyPrepared**                | La entrada actual ya se ha copiado o borrado.                                                                            |
| **hrKeyNotMade**                     | No se ha realizado ninguna clave.                                                                                                                 |
| **hrUpdateNotPrepared**              | La actualización no se preparó.                                                                                                         |
| **hrwrnDataHasChanged**              | Los datos han cambiado.                                                                                                                |
| **alterrDataHasChanged**              | La operación se abandonó porque los datos han cambiado.                                                                            |
| **hrKeyChanged**                     | Se ha movido a una nueva clave.                                                                                                              |
| **hrTooManySorts**                   | Hay demasiados procesos de ordenación.                                                                                               |
| **hrInvalidOnSort**                  | Se ha producido una operación que no es válida en la ordenación.                                                                               |
| **hrTempFileOpenError**              | No se puede abrir el archivo temporal.                                                                                               |
| **hrTooManyAttachedDatabases**       | Hay demasiadas bases de datos abiertas.                                                                                               |
| **hrDiskFull**                       | El disco está lleno.                                                                                                                |
| **hrPermissionDenied**               | Se deniega el permiso.                                                                                                            |
| **hrFileNotFound**                   | No se encuentra el archivo.                                                                                                         |
| **hrFileOpenReadOnly**               | El archivo de base de datos es de solo lectura.                                                                                                  |
| **hrAfterInitialization**            | No se puede restaurar después de la inicialización.                                                                                          |
| **hrLogCorrupted**                   | Los archivos de registro de la base de datos están dañados.                                                                                              |
| **hrInvalidOperation**               | La operación no es válida.                                                                                                        |
| **hrAccessDenied**                   | Acceso denegado.                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Success](success.md)
</dt> <dt>

[Errores de copia de seguridad en Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errores del sistema en Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Errores del Administrador de directorios](directory-manager-errors.md)
</dt> <dt>

[Valores devueltos para funciones en Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




