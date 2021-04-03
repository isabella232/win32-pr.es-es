---
description: Describe los códigos de error 6000-8199 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Códigos de error del sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907354"
---
# <a name="system-error-codes-6000-8199"></a>Códigos de error del sistema (6000-8199)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 6000 a 8199). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR de \_ cifrado de errores \_**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



No se pudo cifrar el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**error en el \_ DEScifrado de errores \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



No se pudo descifrar el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**archivo de ERROR \_ \_ cifrado**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



El archivo especificado está cifrado y el usuario no tiene la capacidad de descifrarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR: \_ no hay \_ Directiva de recuperación \_**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



No hay ninguna directiva de recuperación de cifrado válida configurada para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR \_ no \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



No se ha cargado el controlador de cifrado necesario para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR \_ de \_ EFS incorrecto**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



El archivo se cifró con un controlador de cifrado diferente del que está cargado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR: \_ no hay \_ claves de usuario \_**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



No hay claves de EFS definidas para el usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**archivo de ERROR \_ \_ no \_ cifrado**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



El archivo especificado no está cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**no se pudo \_ \_ exportar el \_ formato**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



El archivo especificado no está en el formato de exportación de EFS definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**archivo de ERROR de \_ \_ \_ solo lectura**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



El archivo especificado es de solo lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR en el \_ directorio \_ EFS no \_ permitido**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



El directorio se ha deshabilitado para el cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR \_ el \_ servidor EFS no es de \_ \_ confianza**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



No se confía en el servidor para la operación de cifrado remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR \_ de \_ Directiva de recuperación incorrecta \_**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



La Directiva de recuperación configurada para este sistema contiene un certificado de recuperación no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR \_ de \_ BLOB de EFS alg \_ \_ demasiado \_ grande**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



El algoritmo de cifrado usado en el archivo de origen necesita un búfer de clave mayor que el del archivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**el \_ volumen de error \_ no es \_ compatible con \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



La partición de disco no admite el cifrado de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR de \_ EFS \_ deshabilitado**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Esta máquina está deshabilitada para el cifrado de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR: la \_ versión de EFS \_ no es \_ \_ compatible**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Se requiere un sistema más reciente para descifrar este archivo cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR \_ de \_ cifrado de CS \_ respuesta de servidor no válida \_ \_**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



El servidor remoto ha enviado una respuesta no válida para un archivo que se está abriendo con el cifrado del lado cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR en el \_ \_ servidor de cifrado CS \_ no compatible \_**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



El servidor remoto no admite el cifrado del lado cliente, aunque notifica que es compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR \_ CS \_ cifrado \_ \_ archivo cifrado existente \_**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



El archivo está cifrado y debe abrirse en el modo de cifrado del lado cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR \_ CS \_ cifrado \_ nuevo \_ archivo cifrado \_**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Se está creando un nuevo archivo cifrado y debe proporcionarse un $EFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR \_ de \_ archivo de cifrado CS \_ \_ no \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



El cliente SMB solicitó un FSCTL de CSE en un archivo que no es de CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**la \_ Directiva de cifrado de errores \_ \_ deniega la \_ operación**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



La Directiva bloqueó la operación solicitada. Para obtener más información, póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR \_ no \_ \_ se encontraron servidores de explorador \_**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



La lista de servidores de este grupo de trabajo no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**el \_ servicio sched E \_ no es \_ \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



El servicio de Programador de tareas debe estar configurado para ejecutarse en la cuenta del sistema para funcionar correctamente. Las tareas individuales se pueden configurar para ejecutarse en otras cuentas.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**SECTOR de registro de errores \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



El servicio de registro encontró un sector de registro no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**paridad del sector de registro de errores \_ \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



El servicio de registro encontró un sector de registro con paridad de bloque no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**SECTOR de registro de errores \_ \_ \_ reasignado**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



El servicio de registro encontró un sector de registro reasignado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloque de registro de errores \_ \_ \_ incompleto**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



El servicio de registro encontró un bloque de registro parcial o incompleto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervalo no válido de registro de errores \_**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



El servicio de registro detectó un intento de obtener acceso a datos fuera del intervalo de registros activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**bloques de registro de errores \_ \_ \_ agotados**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Los búferes de serialización de usuario del servicio de registro están agotados.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexto de lectura de registro de errores \_ \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



El servicio de registro detectó un intento de leer desde un área de cálculo de referencias con un contexto de lectura no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**reinicio de registro de errores \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



El servicio de registro encontró un área de reinicio de registro no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versión de \_ bloque de registro de errores \_**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



El servicio de registro encontró una versión de bloque de registro no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloque de registro de errores \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



El servicio de registro encontró un bloque de registro no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**modo de lectura de registro de errores \_ \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



El servicio de registro detectó un intento de leer el registro con un modo de lectura no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**\_ \_ no reiniciar el registro de errores \_**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



El servicio de registro encontró una secuencia de registro sin área de reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadatos de registro de errores \_ \_ \_ dañados**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadatos de registro de errores \_ \_ \_ no válidos**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos que el sistema de archivos de registro no pudo crear.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadatos de registro de errores \_ \_ \_ incoherentes**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos con datos incoherentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Reserva de registro de errores \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



El servicio de registro detectó un intento de asignar o eliminar el espacio de reserva.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**no se pudo eliminar el registro de errores \_ \_ \_**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



El servicio de registro no puede eliminar el archivo de registro o el contenedor del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**límite de contenedor de registro de errores \_ \_ \_ \_ superado**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



El servicio de registro ha alcanzado el número máximo de contenedores permitidos asignados a un archivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ Inicio del registro \_ de errores de \_ registro**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



El servicio de registro ha intentado leer o escribir hacia atrás más allá del inicio del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**la \_ Directiva de registro de errores \_ \_ ya está \_ instalada**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



No se pudo instalar la Directiva de registro porque ya hay una directiva del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**Directiva de registro de errores \_ \_ \_ no \_ instalada**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



La Directiva de registro en cuestión no se instaló en el momento de la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**Directiva de registro de errores \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



El conjunto de directivas instalado en el registro no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflicto de \_ directivas de registro de errores \_**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Una directiva del registro en cuestión impidió que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_cola de \_ archivo anclada al registro \_ de errores \_**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



No se puede reclamar el espacio del registro porque el registro está anclado por la cola del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**entrada de registro de errores no \_ \_ \_ existente**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



La entrada de registro no es un registro del archivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_registros de \_ errores \_ reservados \_ no válidos**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



El número de entradas de registro reservadas o el ajuste del número de entradas de registro reservadas no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**espacio de registro de errores \_ \_ \_ reservado \_ no válido**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



El espacio de registro reservado o el ajuste del espacio de registro no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**cola de registro de errores \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Una cola de archivo nueva o existente o la base del registro activo no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**registro de errores \_ \_ completo**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Se agotó el espacio de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR \_ no se pudo \_ \_ cambiar el tamaño del \_ registro**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



No se pudo establecer el tamaño solicitado en el registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**registro de errores \_ \_ multiplexado**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



El registro se multiplexa, no se permiten escrituras directas en el registro físico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**registro de errores \_ \_ dedicado**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



No se pudo realizar la operación porque el registro es un registro dedicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**el \_ \_ archivo \_ de registro de errores no está \_ en \_ curso**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



La operación requiere un contexto de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ archivo de registro \_ de errores en \_ curso**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



El archivo de registro está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR de \_ Registro \_ efímero**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



La operación requiere un registro no efímero, pero el registro es efímero.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**el \_ registro de errores \_ no tiene \_ suficientes \_ contenedores**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



El registro debe tener al menos dos contenedores antes de que se puedan leer o escribir en él.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**el \_ cliente de registro de errores \_ \_ ya está \_ registrado**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Ya hay un cliente de registro registrado en la secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**cliente de registro de errores \_ \_ \_ no \_ registrado**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



No se ha registrado un cliente de registro en la secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ controlador completo de registro \_ de errores en \_ curso**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Ya se ha realizado una solicitud para administrar la condición de registro completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**error \_ \_ al leer el contenedor del registro de \_ errores \_**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



El servicio de registro encontró un error al intentar leer desde un contenedor de registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**error de escritura en el contenedor de registro de errores \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



El servicio de registro encontró un error al intentar escribir en un contenedor de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**error \_ \_ al abrir el contenedor del registro de \_ errores \_**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



El servicio de registro encontró un error al intentar abrir un contenedor de registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Estado del contenedor de registro de errores \_ \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



El servicio de registro encontró un estado de contenedor no válido al intentar una acción solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Estado de registro de errores \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



El servicio de registro no está en el estado correcto para realizar una acción solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**registro de errores \_ \_ anclado**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



No se puede reclamar el espacio del registro porque el registro está anclado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**error \_ de \_ vaciado de metadatos de registro de \_ errores \_**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Error de vaciado de metadatos de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ seguridad incoherente del registro de errores \_**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



La seguridad en el registro y sus contenedores es incoherente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**error \_ de \_ vaciado anexado de registro de \_ errores \_**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Se anexaron registros al registro o se realizaron cambios en la reserva, pero no se pudo vaciar el registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ reserva anclada del registro de errores \_**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



El registro está anclado debido a la reserva que consume la mayor parte del espacio del registro. Libere algunos registros reservados para dejar espacio disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR \_ de \_ transacción no válida**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



El identificador de transacción asociado a esta operación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR de \_ transacción \_ no \_ activa**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



La operación solicitada se realizó en el contexto de una transacción que ya no está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR \_ de \_ solicitud de transacción \_ no \_ válida**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



La operación solicitada no es válida en el objeto de transacción en su estado actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**\_no se \_ solicitó la transacción de error \_**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



El autor de la llamada ha llamado a una API de respuesta, pero no se espera la respuesta porque TM no ha emitido la solicitud correspondiente al llamador.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transacción de ERROR \_ \_ ya \_ anulada**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Es demasiado tarde para realizar la operación solicitada, ya que la transacción ya se ha anulado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transacción de ERROR \_ \_ ya \_ confirmada**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



Es demasiado tarde para realizar la operación solicitada, puesto que ya se ha confirmado la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR \_ de \_ inicialización de TM \_**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



No se pudo inicializar correctamente el administrador de transacciones. No se admiten las operaciones de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR \_ RESOURCEMANAGER \_ - \_ solo lectura**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



El ResourceManager especificado no realizó cambios ni actualizaciones en el recurso en esta transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR de \_ transacción \_ no \_ unida**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Resource Manager intentó preparar una transacción que no se ha unido correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**existe una transacción de ERROR \_ \_ superior \_ existente**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



El objeto de transacción ya tiene una inscripción superior y el llamador intentó realizar una operación que habría creado un nuevo superior. Solo se permite una inscripción superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**el \_ Protocolo CRM de error \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



El RM ha intentado registrar un protocolo que ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR en la propagación de la \_ transacción \_ \_**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Error al tratar de propagar la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR \_ de \_ Protocolo CRM \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



El protocolo de propagación solicitado no se registró como CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR de \_ búfer de referencia de transacción \_ no válido \_ \_**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



El búfer pasado a PushTransaction o PullTransaction no tiene un formato válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR \_ de \_ transacción actual \_ no \_ válida**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



El contexto de transacción actual asociado al subproceso no es un identificador válido para un objeto de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ no \_ se encontró la transacción de error**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



No se pudo abrir el objeto de transacción especificado porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR \_ RESOURCEMANAGER \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



No se pudo abrir el objeto ResourceManager especificado porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ no se encontró la inscripción \_ de errores**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



No se pudo abrir el objeto de inscripción especificado porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR \_ TRANSACTIONMANAGER \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



No se pudo abrir el objeto TransactionManager especificado porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR \_ TRANSACTIONMANAGER \_ no está \_ en línea**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



No se pudo crear o abrir el objeto especificado porque su TransactionManager asociado no está en línea. El TransactionManager debe estar totalmente en línea mediante una llamada a RecoverTransactionManager para recuperar hasta el final de su archivo de registro antes de que se puedan abrir los objetos de la transacción o los espacios de nombres ResourceManager. Además, los errores en la escritura de registros en el archivo de registro pueden hacer que un TransactionManager quede sin conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR \_ TRANSACTIONMANAGER de la colisión de \_ nombres de recuperación \_ \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



El TransactionManager especificado no pudo crear los objetos contenidos en su archivo de registro en el espacio de nombres ob. Por lo tanto, el TransactionManager no se pudo recuperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR de \_ transacción \_ no \_ raíz**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



No se pudo completar la llamada para crear una inscripción superior en este objeto de transacción porque el objeto de transacción especificado para la inscripción es una rama subordinada de la transacción. Solo se puede dar de alta la raíz de la transacción en como un nivel superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objeto de transacción de ERROR \_ \_ \_ expirado**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Dado que el administrador de transacciones asociado o el administrador de recursos se ha cerrado, el identificador ya no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**respuesta de transacción de ERROR \_ \_ \_ no \_ dada de alta**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



No se pudo realizar la operación especificada en esta inscripción superior porque la inscripción no se creó con la respuesta de finalización correspondiente en NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**registro de transacción de ERROR \_ \_ \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



No se pudo realizar la operación especificada porque el registro que se registraría era demasiado largo. Esto puede deberse a dos condiciones: hay demasiadas inscritos en esta transacción o la combinación de RecoveryInformation que se está registrando en nombre de las inscritos es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR \_ de \_ transacción implícita \_ no \_ compatible**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



No se admiten las transacciones implícitas.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR \_ de \_ integridad de transacción \_ infringida**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



El administrador de transacciones de kernel tenía que anular u olvidar la transacción porque bloqueó el progreso de avance.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR \_ de \_ desigualdad de identidad de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



La identidad TransactionManager suministrada no coincidía con la que se registró en el archivo de registro de TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**\_ \_ no se puede \_ \_ inmovilizar el error RM \_ para la \_ instantánea**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Esta operación de instantánea no puede continuar porque un administrador de recursos transaccional no se puede inmovilizar en su estado actual. Inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transacción de error \_ debe \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



No se puede dar de alta la transacción en con el EnlistmentMask especificado, porque la transacción ya ha completado la fase de prepreparación. Para garantizar la exactitud, ResourceManager debe cambiar a un modo de escritura a través y dejar de almacenar en caché los datos en esta transacción. La inscripción solo en fases posteriores de la transacción puede realizarse correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR de \_ transacción \_ no \_ superior**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



La transacción no tiene una inscripción superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**daños en la heurística de errores \_ \_ \_ posibles**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



Se completó el intento de confirmar la transacción, pero es posible que alguna parte del árbol de transacciones no se confirmara correctamente debido a la heurística. Por lo tanto, es posible que algunos datos modificados en la transacción no se hayan confirmado, lo que provoca una incoherencia transaccional. Si es posible, Compruebe la coherencia de los datos asociados.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**\_conflicto transaccional de errores \_**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



La función intentó utilizar un nombre que está reservado para su uso por otra transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR \_ RM \_ no \_ activo**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



La compatibilidad con transacciones en el administrador de recursos especificado no se inició o se apagó debido a un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR \_ de \_ metadatos de RM \_ dañados**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Los metadatos de RM están dañados. El RM no funcionará.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**directorio de errores \_ \_ no \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



El directorio especificado no contiene un administrador de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transacciones de ERROR \_ \_ remotas no admitidas \_**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



El recurso compartido o el servidor remoto no admiten operaciones de archivo de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**tamaño de registro de errores de \_ \_ \_ tamaño no válido \_**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



El tamaño de registro solicitado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**el objeto de ERROR ya \_ \_ no \_ \_ existe**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



La reversión de un punto de retorno de la transacción ha eliminado el objeto (archivo, secuencia, vínculo) correspondiente al identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ no \_ se encontró la MINIVERSIÓN del flujo de error**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



No se encontró la miniversión de archivo especificada para este archivo de transacción abierto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**la \_ miniversión del flujo de error \_ \_ no \_ es válida**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Se encontró la miniversión de archivo especificada, pero se invalidó. La causa más probable es la reversión de un punto de retorno de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR \_ \_ de MINIVERSIÓN inaccesible \_ desde \_ la \_ transacción especificada**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Una miniversión solo se puede abrir en el contexto de la transacción que la creó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR no se pudo \_ \_ abrir la \_ miniversión con el \_ \_ intento de modificación \_**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



No es posible abrir una miniversión con el acceso de modificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR no se pudo \_ \_ crear \_ más \_ secuencia \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



No es posible crear más miniversions para esta secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de versión de archivo remoto \_**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



El servidor remoto ha enviado un número de versión o FID no coincidente para un archivo abierto con transacciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**el identificador de ERROR ya \_ \_ no \_ \_ es válido**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



Una transacción ha invalidado el identificador. La causa más probable es la presencia de la asignación de memoria en un archivo o un controlador abierto cuando la transacción finaliza o se revierte al punto de retorno.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR: \_ no hay \_ \_ metadatos de TxF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



No hay metadatos de transacción en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**daños en el registro de errores \_ \_ \_ detectados**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Los datos de registro están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR no se pudo \_ \_ recuperar \_ con el \_ identificador \_ abierto**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



No se puede recuperar el archivo porque todavía hay un controlador abierto en él.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR de \_ RM \_ desconectado**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



El resultado de la transacción no está disponible porque el administrador de recursos responsable se ha desconectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**INSCRIPCIÓN de ERROR \_ \_ no \_ superior**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



Se rechazó la solicitud porque la inscripción en cuestión no es una inscripción superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**recuperación de errores \_ \_ no \_ necesaria**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



El administrador de recursos transaccional ya es coherente. No es necesaria la recuperación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR \_ RM \_ ya \_ iniciado**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



El administrador de recursos de transacciones ya se ha iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**la \_ identidad del archivo de error \_ no es \_ \_ persistente**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



No se puede abrir el archivo de transacciones, porque su identidad depende del resultado de una transacción no resuelta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR no se pudo \_ \_ interrumpir la \_ \_ dependencia transaccional**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



No se puede realizar la operación porque otra transacción depende del hecho de que esta propiedad no cambie.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**no se pudo obtener el \_ \_ \_ límite de RM cruzado \_**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



La operación implicaría un solo archivo con dos administradores de recursos transaccionales y, por lo tanto, no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR \_ dir de TxF \_ \_ no \_ vacío**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



El directorio $Txf debe estar vacío para que esta operación se realice correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_ \_ existen transacciones de ERROR de errores \_**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



La operación dejaría un administrador de recursos transaccional en un estado incoherente y, por lo tanto, no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR \_ TM \_ volatile**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



No se pudo completar la operación porque el administrador de transacciones no tiene un registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR \_ del temporizador de reversión \_ \_ expirado**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



No se pudo programar una reversión porque ya se ejecutó una reversión programada anteriormente o se puso en cola para su ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**atributo de TxF de ERROR \_ \_ \_ dañado**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



El atributo de metadatos transaccional del archivo o directorio está dañado y es ilegible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR \_ \_ de EFS no \_ permitido en la \_ \_ transacción**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



No se pudo completar la operación de cifrado porque una transacción está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR de \_ apertura transaccional \_ \_ no \_ permitida**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



No se permite abrir este objeto en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**error de \_ crecimiento del registro de errores \_ \_**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Error al tratar de crear espacio en el registro del administrador de recursos transaccionales. El estado de error se ha registrado en el registro de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR de \_ asignación de transacción \_ \_ remota no admitida \_**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



No se admite la asignación de memoria (creación de una sección asignada) a un archivo remoto en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**los \_ metadatos de TxF de error \_ \_ ya están \_ presentes**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Los metadatos de transacción ya están presentes en este archivo y no se pueden reemplazar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR \_ de \_ devoluciones de llamada de ámbito de transacción \_ \_ no \_ establecida**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



No se pudo especificar un ámbito de transacción porque el controlador de ámbito no se ha inicializado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**promoción de la transacción de ERROR \_ \_ necesaria \_**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



La promoción era necesaria para permitir que el administrador de recursos se inscriba, pero la transacción se configuró para no permitirla.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR: \_ no se puede \_ ejecutar el \_ archivo en la \_ \_ transacción**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Este archivo está abierto para su modificación en una transacción no resuelta y solo se puede abrir para ejecutarlo un lector de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transacciones de ERROR \_ \_ no \_ inmovilizadas**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



Se omitió la solicitud para reanudar las transacciones inmovilizadas porque las transacciones no se han inmovilizado previamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR \_ \_ en la inmovilización \_ de transacciones en \_ curso**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



No se pueden inmovilizar las transacciones porque ya hay una inmovilización en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR \_ : \_ volumen de instantánea \_**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



El volumen de destino no es un volumen de instantánea. Esta operación solo es válida en un volumen montado como una instantánea.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR: \_ no hay ningún \_ punto \_ de retorno con \_ \_ archivos abiertos**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



No se pudo realizar la operación de punto de retorno porque los archivos están abiertos en la transacción. Esto no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**reparación de errores de \_ datos \_ perdidos \_**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows ha detectado daños en un archivo y ese archivo se ha reparado desde entonces. Es posible que se haya producido una pérdida de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR \_ disperso \_ no \_ permitido \_ en la \_ transacción**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



No se pudo completar la operación dispersa porque hay una transacción activa en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR \_ de \_ incoherencia de identidad de TM \_**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



Error en la llamada para crear un objeto TransactionManager porque la identidad de TM almacenada en el archivo de registro no coincide con la identidad de TM que se pasó como argumento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR de la \_ \_ sección flotante**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Se intentó una operación de e/s en un objeto de sección que se ha flotado como resultado de la finalización de una transacción. No hay datos válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**el ERROR \_ no puede \_ aceptar el \_ trabajo de transacción \_**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



El administrador de recursos de transacciones no puede aceptar actualmente el trabajo de transacción debido a una condición transitoria como recursos insuficientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR \_ no se pueden \_ anular \_ las transacciones**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



El administrador de recursos transaccional tenía demasiados contabilizan pendientes que no se pudieron anular. Se ha cerrado el administrador de recursos transaccionales.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR \_ de \_ clústeres erróneos**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



No se pudo completar la operación debido a clústeres defectuosos en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_no se \_ permite la compresión de error en la \_ \_ \_ transacción**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



No se pudo completar la operación de compresión porque hay una transacción activa en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR de \_ volumen \_ modificado**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



No se pudo completar la operación porque el volumen está sucio. Ejecute CHKDSK e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR: \_ no hay \_ \_ seguimiento \_ de vínculos en la \_ transacción**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



No se pudo completar la operación de seguimiento de vínculos porque una transacción está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_no se \_ admite la operación de error en la \_ \_ \_ transacción**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Esta operación no se puede realizar en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**identificador de ERROR \_ expirado \_**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



El identificador ya no está asociado correctamente a su transacción. Es posible que se haya abierto en un administrador de recursos transaccional que se forzó posteriormente para reiniciarse. Cierre el identificador y abra uno nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**no se ha dado de \_ alta la transacción de error \_ \_**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



No se pudo realizar la operación especificada porque el administrador de recursos no está dado de alta en la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR \_ CTX en \_ el nombre de la estación de \_ nombres \_ no válido**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



El nombre de sesión especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR \_ CTX \_ no válido \_ PD**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



El controlador de protocolo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR \_ CTX \_ PD \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



No se encontró el controlador de protocolo especificado en la ruta de acceso del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR \_ CTX \_ WD \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



No se encontró el controlador de conexión de terminal especificado en la ruta de acceso del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR \_ CTX \_ no se puede \_ crear la entrada del registro de \_ eventos \_**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



No se pudo crear una clave del registro para el registro de eventos para esta sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR \_ CTX \_ \_ colisión de nombre de servicio \_**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Ya existe un servicio con el mismo nombre en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR \_ CTX \_ cierre \_ pendiente**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Hay una operación de cierre pendiente en la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR \_ CTX \_ no \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



No hay ningún búfer de salida disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR \_ CTX \_ modem \_ INF \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



El módem. No se encontró el archivo INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR \_ CTX \_ MODEMNAME no válido \_**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



No se encontró el nombre del módem en MODEM. INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**error \_ de \_ respuesta de módem CTX \_ \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



El módem no aceptó el comando que se le ha enviado. Compruebe que el nombre del módem configurado coincide con el módem conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR \_ CTX \_ \_ tiempo de espera de respuesta del módem \_**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



El módem no respondió al comando que se le ha enviado. Compruebe que el módem está correctamente cableado y encendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR \_ CTX \_ respuesta de módem \_ \_ no \_ portadora**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



No se pudo detectar el operador o se quitó el operador debido a la desconexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR \_ CTX \_ respuesta de módem \_ \_ sin \_ ditono**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



No se detectó el tono de marcado en el tiempo requerido. Compruebe que el cable telefónico está conectado correctamente y funciona.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR \_ de \_ respuesta de módem CTX \_ \_ ocupada**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Señal de ocupado detectada en el sitio remoto en la devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR \_ CTX \_ \_ voz de respuesta de módem \_**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Voz detectada en el sitio remoto en la devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**error \_ CTX \_ TD \_ error**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Error del controlador de transporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR \_ CTX-en \_ \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



No se encuentra la sesión especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**el ERROR CTX en la estación de mensaje \_ \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



El nombre de sesión especificado ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR de \_ CTX en \_ \_ ocupado**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



No se puede completar la tarea que está intentando realizar porque Servicios de Escritorio remoto está ocupado actualmente. Inténtalo de nuevo al cabo de un rato. Otros usuarios todavía deben poder iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR \_ CTX \_ \_ modo de vídeo incorrecto \_**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Se ha intentado conectar a una sesión cuyo modo de vídeo no es compatible con el cliente actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR \_ CTX \_ Graphics \_ no válida**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



La aplicación intentó habilitar el modo de gráficos de DOS. No se admite el modo de gráficos de DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR \_ CTX \_ Inicio de sesión \_ deshabilitado**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Se ha deshabilitado el privilegio de inicio de sesión interactivo. Póngase en contacto con el administrador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR \_ CTX \_ no \_ Console**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



La operación solicitada solo se puede realizar en la consola del sistema. Esto suele ser el resultado de un controlador o DLL del sistema que requiere acceso directo a la consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR \_ de \_ tiempo de espera de consulta de cliente CTX \_ \_**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



El cliente no pudo responder al mensaje de conexión de servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR \_ CTX \_ \_ desconexión de consola**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



No se admite la desconexión de la sesión de consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR \_ CTX \_ Console \_ Connect**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



No se puede volver a conectar una sesión desconectada a la consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR \_ CTX \_ sombra \_ denegada**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



Se denegó la solicitud para controlar otra sesión de forma remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR \_ CTX en el \_ \_ acceso \_ denegado**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



Se denegó el acceso a la sesión solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR \_ CTX \_ no válido \_ WD**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



El controlador de conexión de terminal especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR \_ CTX \_ Shadow \_ no válido**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



La sesión solicitada no se puede controlar de forma remota. Esto puede deberse a que la sesión está desconectada o no tiene un usuario que ha iniciado sesión actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR de la \_ \_ sombra CTX \_ deshabilitada**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



La sesión solicitada no está configurada para permitir el control remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR \_ \_ \_ de licencia de cliente CTX \_ en \_ uso**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Se ha rechazado la solicitud de conexión a este Terminal Server. Otro usuario está usando actualmente su Terminal Server número de licencia de cliente. Llame al administrador del sistema para obtener un número de licencia único.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR de la \_ \_ licencia de cliente CTX \_ \_ no \_ establecida**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Se ha rechazado la solicitud de conexión a este Terminal Server. No se ha especificado el número de licencia de cliente de Terminal Server para esta copia del cliente de Terminal Server. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR \_ de \_ licencia de CTX \_ no \_ disponible**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



El número de conexiones a este equipo es limitado y ahora todas las conexiones están en uso. Intente conectarse más tarde o póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR \_ de \_ cliente de licencia CTX \_ \_ no válido**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



El cliente que está usando no tiene licencia para usar este sistema. Se denegó la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR \_ CTX \_ expiró la licencia \_**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



La licencia del sistema ha expirado. Se denegó la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR de la \_ sombra de CTX \_ no en \_ \_ ejecución**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



No se pudo terminar el control remoto porque la sesión especificada no se está controlando de forma remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR \_ \_ de la sombra \_ de CTX terminada \_ por el \_ modo \_**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



El control remoto de la consola ha finalizado porque se ha cambiado el modo de presentación. No se admite el cambio del modo de presentación en una sesión de control remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**recuento de \_ activaciones de errores \_ \_ superado**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



La activación ya se ha restablecido el número máximo de veces para esta instalación. El temporizador de activación no se borrará.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR \_ CTX \_ WINSTATIONS \_ deshabilitado**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Los inicios de sesión remotos están deshabilitados actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR \_ de \_ nivel de cifrado CTX \_ \_ requerido**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



No tiene el nivel de cifrado adecuado para obtener acceso a esta sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR \_ \_ de sesión CTX \_ en \_ uso**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



El usuario% s \\ \\ % s ha iniciado sesión en este equipo. Solo el usuario actual o un administrador pueden iniciar sesión en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR \_ CTX \_ no \_ forzar \_ cierre de sesión**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



El usuario% s \\ \\ % s ya ha iniciado sesión en la consola de este equipo. No tiene permiso para iniciar sesión en este momento. Para resolver este problema, póngase en contacto con% s \\ \\ % s y pídale que cierre la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR \_ de \_ restricción de cuenta de CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



No se puede iniciar la sesión debido a una restricción de cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**error \_ de \_ Protocolo RDP \_ error**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



El componente de protocolo RDP %2 detectó un error en el flujo de protocolo y ha desconectado el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR \_ CTX \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



El servicio de asignación de unidad de cliente se ha conectado en la conexión de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR \_ CTX \_ CDM \_ Disconnect**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



El servicio de asignación de unidad de cliente se ha desconectado en la conexión de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**error \_ CTX error de \_ nivel de seguridad \_ \_**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



El nivel de seguridad de Terminal Server ha detectado un error en el flujo de protocolo y ha desconectado el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR \_ de \_ sesiones incompatibles de TS \_**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



La sesión de destino no es compatible con la sesión actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**error \_ de \_ subsistema de vídeo de TS \_ \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows no se puede conectar a la sesión porque se produjo un problema en el subsistema de vídeo de Windows. Intente conectarse de nuevo más tarde o póngase en contacto con el administrador del servidor para obtener ayuda.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_secuencia de \_ API no válida de FRS Err \_ \_**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



Se llamó incorrectamente a la API del servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**servicio de inicio de FRS \_ Err \_ \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



No se puede iniciar el servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**error de FRS al \_ \_ detener el \_ servicio**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



No se puede detener el servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna de error de FRS \_**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



La API del servicio de replicación de archivos finalizó la solicitud. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**error de FRS \_ \_ interno**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



El servicio de replicación de archivos finalizó la solicitud. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**servicio de error de FRS \_ \_ \_ COMM**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



No se puede establecer contacto con el servicio de replicación de archivos. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ Err \_ insuficiente \_ priv**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**autenticación de FRS \_ Err \_**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ Err \_ Parent \_ insuficiente \_ priv**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes en el controlador de dominio. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ autenticación principal FRS \_ Err**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible en el controlador de dominio. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ Err \_ secundario \_ a \_ elemento primario \_ COMM**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



El servicio de replicación de archivos no se puede comunicar con el servicio de replicación de archivos en el controlador de dominio. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**\_COMM ERR \_ Parent \_ to \_ Child \_ COMM**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



El servicio de replicación de archivos del controlador de dominio no se puede comunicar con el servicio de replicación de archivos de este equipo. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ Err Err \_ SYSVOL \_ rellenar**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un error interno. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ Err error de \_ llenado de SYSVOL \_ \_**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un tiempo de espera interno. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ Err error de \_ SYSVOL \_ está \_ ocupado**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



El servicio de replicación de archivos no puede procesar la solicitud. El volumen del sistema está ocupado con una solicitud anterior.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err error de la \_ \_ degradación**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



El servicio de replicación de archivos no puede detener la replicación del volumen del sistema debido a un error interno. Es posible que el registro de eventos tenga más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parámetro de \_ servicio no válido de FRS Err \_ \_**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



El servicio de replicación de archivos ha detectado un parámetro no válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




