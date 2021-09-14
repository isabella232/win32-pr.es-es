---
description: Describe los códigos de error 6000-8199 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Códigos de error del sistema (6000-8199) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164585"
---
# <a name="system-error-codes-6000-8199"></a>Códigos de error del sistema (6000-8199)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema (errores 6000 a 8199). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR \_ DE CIFRADO \_**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



No se pudo cifrar el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR \_ DE DESCIFRADO \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



No se pudo descifrar el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ARCHIVO \_ DE ERROR \_ CIFRADO**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



El archivo especificado está cifrado y el usuario no tiene la capacidad de descifrarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR \_ NO \_ RECOVERY \_ POLICY**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



No hay ninguna directiva de recuperación de cifrado válida configurada para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR \_ NO \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



El controlador de cifrado necesario no se carga para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR \_ DE \_ EFS INCORRECTO**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



El archivo se ha cifrado con un controlador de cifrado diferente al que está cargado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR \_ SIN CLAVES DE \_ \_ USUARIO**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



No hay claves de EFS definidas para el usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ARCHIVO DE \_ ERROR \_ NO \_ CIFRADO**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



El archivo especificado no está cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR \_ NO EXPORTAR \_ \_ FORMATO**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



El archivo especificado no está en el formato de exportación de EFS definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ARCHIVO DE ERROR \_ \_ DE SOLO \_ LECTURA**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



El archivo especificado es de solo lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR \_ DIR \_ EFS NO \_ PERMITIDO**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



El directorio se ha deshabilitado para el cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR \_ EFS \_ SERVER \_ NOT \_ TRUSTED**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



El servidor no es de confianza para la operación de cifrado remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR \_ DIRECTIVA DE \_ RECUPERACIÓN NO \_ RECUPERADA**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



La directiva de recuperación configurada para este sistema contiene un certificado de recuperación no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR \_ EFS \_ ALG \_ BLOB \_ TOO \_ BIG**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



El algoritmo de cifrado usado en el archivo de origen necesita un búfer de clave mayor que el del archivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**VOLUMEN \_ DE ERROR NO COMPATIBLE CON \_ \_ \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



La partición de disco no admite el cifrado de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR \_ EFS \_ DESHABILITADO**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Esta máquina está deshabilitada para el cifrado de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR \_ NO SE ADMITE LA VERSIÓN \_ \_ DE EFS \_**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Se requiere un sistema más reciente para descifrar este archivo cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR \_ CS \_ ENCRYPTION \_ INVALID \_ SERVER \_ RESPONSE**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



El servidor remoto envió una respuesta no válida para que se abra un archivo con cifrado del lado cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR \_ CS \_ ENCRYPTION \_ UNSUPPORTED \_ SERVER**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



El servidor remoto no admite el cifrado del lado cliente, aunque dice admitirlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR \_ CS \_ ENCRYPTION \_ EXISTING \_ ENCRYPTED \_ FILE**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



El archivo está cifrado y debe abrirse en modo de cifrado del lado cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR \_ CS \_ ENCRYPTION \_ NEW \_ ENCRYPTED \_ FILE**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Se está creando un nuevo archivo cifrado y $EFS se debe proporcionar un nuevo archivo cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR \_ CS \_ ENCRYPTION \_ FILE \_ NOT \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



El cliente SMB solicitó un CSE FSCTL en un archivo que no es de CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR \_ ENCRYPTION \_ POLICY \_ DENIEGA LA \_ OPERACIÓN**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



La directiva bloqueó la operación solicitada. Para obtener más información, póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR \_ NO SE ENCONTRARON SERVIDORES DE \_ \_ \_ EXPLORADOR**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



La lista de servidores de este grupo de trabajo no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ SERVICE \_ NOT \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



El Programador de tareas debe configurarse para que se ejecute en la cuenta del sistema para que funcione correctamente. Las tareas individuales se pueden configurar para ejecutarse en otras cuentas.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**SECTOR DE \_ REGISTRO DE ERRORES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



El servicio de registro encontró un sector de registro no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**PARIDAD \_ DEL SECTOR DEL REGISTRO DE ERRORES NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



El servicio de registro encontró un sector de registro con paridad de bloques no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**SECTOR DE \_ \_ REGISTRO DE ERRORES \_ REMAPPED**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



El servicio de registro encontró un sector de registro que se ha rematado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**BLOQUE \_ DE REGISTRO DE ERRORES \_ \_ INCOMPLETO**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



El servicio de registro encontró un bloque de registro parcial o incompleto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**INTERVALO NO \_ VÁLIDO DEL REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



El servicio de registro encontró un intento de acceso a los datos fuera del intervalo de registro activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**BLOQUES \_ DE REGISTRO DE ERRORES \_ \_ AGOTADOS**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Se agotan los búferes de la marshalling de usuario del servicio de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**CONTEXTO DE \_ LECTURA DEL REGISTRO DE ERRORES NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



El servicio de registro encontró un intento de lectura desde un área de marshalling con un contexto de lectura no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**REINICIO DEL \_ REGISTRO DE ERRORES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



El servicio de registro encontró un área de reinicio de registro no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR \_ LOG \_ BLOCK \_ VERSION**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



El servicio de registro encontró una versión de bloque de registro no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**BLOQUE DE \_ REGISTRO DE ERRORES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



El servicio de registro encontró un bloque de registro no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**MODO DE \_ LECTURA DEL REGISTRO DE ERRORES NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



El servicio de registro encontró un intento de leer el registro con un modo de lectura no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**REGISTRO DE \_ ERRORES \_ SIN \_ REINICIO**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



El servicio de registro encontró una secuencia de registro sin área de reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**METADATOS \_ DEL REGISTRO DE ERRORES \_ \_ DAÑADOS**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**METADATOS \_ DEL REGISTRO DE ERRORES NO \_ \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos que el sistema de archivos de registro no pudo crear.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**METADATOS \_ DEL REGISTRO DE ERRORES \_ \_ INCOHERENTES**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



El servicio de registro encontró un archivo de metadatos con datos incoherentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**RESERVA DEL \_ REGISTRO DE ERRORES NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



El servicio de registro encontró un intento de asignar o eliminar espacio de reserva erróneo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR \_ LOG \_ CANT \_ DELETE**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



El servicio de registro no puede eliminar el archivo de registro o el contenedor del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**SE \_ SUPERÓ \_ EL LÍMITE DE CONTENEDOR DEL REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



El servicio de registro ha alcanzado el máximo permitido de contenedores asignados a un archivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**INICIO \_ DEL REGISTRO DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



El servicio de registro ha intentado leer o escribir hacia atrás después del inicio del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**DIRECTIVA \_ DE REGISTRO DE ERRORES YA \_ \_ \_ INSTALADA**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



No se pudo instalar la directiva de registro porque ya existe una directiva del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**DIRECTIVA \_ DE REGISTRO DE ERRORES NO \_ \_ \_ INSTALADA**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



La directiva de registro en cuestión no se instaló en el momento de la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**DIRECTIVA \_ DE REGISTRO DE ERRORES NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



El conjunto de directivas instalado en el registro no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**CONFLICTO DE \_ DIRECTIVA DE REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Una directiva en el registro en cuestión impedía que se completara la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**COLA \_ DE ARCHIVO ANCLADO DEL REGISTRO \_ DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



No se puede reclamar el espacio del registro porque el final del archivo ancla el registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**REGISTRO \_ DE \_ ERRORES \_ INEXISTENTE**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



La entrada de registro no es un registro en el archivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**REGISTROS DE \_ ERRORES \_ \_ RESERVADOS NO \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



El número de registros reservados o el ajuste del número de registros reservados no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ESPACIO DE \_ REGISTRO DE ERRORES RESERVADO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



El espacio de registro reservado o el ajuste del espacio de registro no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**COLA \_ DEL REGISTRO DE ERRORES NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Una cola o base de archivo nueva o existente del registro activo no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**REGISTRO \_ DE ERRORES \_ COMPLETO**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Se agota el espacio de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR \_ NO SE PUDO CAMBIAR EL TAMAÑO DEL \_ \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



No se pudo establecer el registro en el tamaño solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**REGISTRO \_ DE \_ ERRORES MULTIPLEXADO**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



El registro se multiplexa, no se permite ninguna escritura directa en el registro físico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**REGISTRO \_ DE ERRORES \_ DEDICADO**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



Error en la operación porque el registro es un registro dedicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ARCHIVO \_ DE REGISTRO DE ERRORES NO EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



La operación requiere un contexto de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ARCHIVO \_ DE REGISTRO DE ERRORES EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



El archivo de registro está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**REGISTRO \_ DE \_ ERRORES EFÍMERO**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



La operación requiere un registro no efímero, pero el registro es efímero.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**REGISTRO DE \_ ERRORES \_ NO HAY \_ SUFICIENTES \_ CONTENEDORES**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



El registro debe tener al menos dos contenedores para poder leerlo o escribirlo en él.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**CLIENTE DE \_ REGISTRO DE ERRORES YA \_ \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Un cliente de registro ya se ha registrado en la secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**CLIENTE DE \_ REGISTRO DE ERRORES NO \_ \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



No se ha registrado un cliente de registro en la secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**CONTROLADOR \_ COMPLETO DEL REGISTRO DE ERRORES EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Ya se ha realizado una solicitud para controlar la condición completa del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR AL \_ LEER EL CONTENEDOR DEL REGISTRO DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



El servicio de registro encontró un error al intentar leer desde un contenedor de registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR AL \_ ESCRIBIR EN EL CONTENEDOR DE \_ \_ REGISTROS \_**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



El servicio de registro encontró un error al intentar escribir en un contenedor de registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR AL \_ ABRIR EL CONTENEDOR DEL REGISTRO DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



El servicio de registro encontró un error al intentar abrir un contenedor de registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ESTADO DEL \_ CONTENEDOR DEL REGISTRO DE ERRORES NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



El servicio de registro encontró un estado de contenedor no válido al intentar una acción solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ESTADO DEL \_ REGISTRO DE ERRORES NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



El servicio de registro no está en el estado correcto para realizar una acción solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**REGISTRO \_ DE \_ ERRORES ANCLADO**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



No se puede reclamar el espacio de registro porque el registro está anclado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR DE \_ VACIADO DE \_ \_ METADATOS DEL REGISTRO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Error de vaciado de metadatos de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**SEGURIDAD \_ \_ INCOHERENTE DEL REGISTRO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



La seguridad en el registro y sus contenedores es incoherente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR DE \_ VACIADO \_ ANEXADO \_ DEL REGISTRO \_ DE ERRORES**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Los registros se anexaron al registro o se realizaron cambios en la reserva, pero no se pudo vaciar el registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**RESERVA \_ ANCLADA \_ DEL REGISTRO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



El registro se ancla debido a que la reserva consume la mayor parte del espacio del registro. Liberar algunos registros reservados para hacer que el espacio esté disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR \_ TRANSACCIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



El identificador de transacción asociado a esta operación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR \_ TRANSACTION \_ NOT \_ ACTIVE**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



La operación solicitada se realizó en el contexto de una transacción que ya no está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**SOLICITUD DE \_ \_ TRANSACCIÓN DE ERROR \_ NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



La operación solicitada no es válida en el objeto Transaction en su estado actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**NO SE \_ SOLICITÓ \_ LA \_ TRANSACCIÓN DE ERROR**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



El autor de la llamada ha llamado a una API de respuesta, pero no se espera la respuesta porque la TM no ha emite la solicitud correspondiente al autor de la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**TRANSACCIÓN \_ DE ERROR \_ YA \_ ANULADA**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



Es demasiado tarde para realizar la operación solicitada, ya que la transacción ya se ha anulado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**TRANSACCIÓN \_ DE ERROR \_ YA \_ CONFIRMADA**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



Es demasiado tarde para realizar la operación solicitada, ya que la transacción ya se ha confirmado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR \_ AL \_ INICIALIZAR TM \_**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



El Administrador de transacciones no se pudo inicializar correctamente. No se admiten las operaciones de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR \_ RESOURCEMANAGER \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



El ResourceManager especificado no realizó cambios ni actualizaciones en el recurso en esta transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR \_ TRANSACTION \_ NOT \_ JOINED**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



El administrador de recursos ha intentado preparar una transacción que no se ha unido correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR \_ TRANSACTION \_ SUPERIOR \_ EXISTS**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



El objeto Transaction ya tiene una alta superior y el autor de la llamada intentó una operación que habría creado un nuevo superior. Solo se permite una única alta superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR \_ CRM \_ PROTOCOL \_ ALREADY \_ EXISTS**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



El rm intentó registrar un protocolo que ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR DE \_ \_ PROPAGACIÓN DE \_ TRANSACCIONES**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Error al intentar propagar la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL PROTOCOLO \_ \_ \_ CRM**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



El protocolo de propagación solicitado no se registró como CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR \_ TRANSACTION \_ INVALID \_ MARSHALL \_ BUFFER**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



El búfer pasado a PushTransaction o PullTransaction no tiene un formato válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR \_ TRANSACCIÓN \_ ACTUAL NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



El contexto de transacción actual asociado al subproceso no es un identificador válido para un objeto de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**NO SE \_ ENCONTRÓ \_ LA TRANSACCIÓN DE \_ ERROR**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



No se pudo abrir el objeto Transaction especificado, porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR \_ RESOURCEMANAGER \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



No se pudo abrir el objeto ResourceManager especificado porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR \_ ENLISTMENT \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



No se pudo abrir el objeto Enlistment especificado, porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR \_ TRANSACTIONMANAGER \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



No se pudo abrir el objeto TransactionManager especificado, porque no se encontró.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR \_ TRANSACTIONMANAGER \_ NOT \_ ONLINE**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



No se pudo crear ni abrir el objeto especificado, porque su TransactionManager asociado no está en línea. TransactionManager debe estar totalmente conectado llamando a RecoverTransactionManager para recuperarse hasta el final de su LogFile antes de que se puedan abrir los objetos de sus espacios de nombres Transaction o ResourceManager. Además, los errores al escribir registros en su LogFile pueden hacer que transactionManager se desconecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR \_ TRANSACTIONMANAGER \_ RECOVERY \_ NAME \_ COLLISION**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



TransactionManager especificado no pudo crear los objetos contenidos en su archivo de registro en el espacio de nombres Ob. Por lo tanto, TransactionManager no pudo recuperarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR \_ TRANSACTION \_ NOT \_ ROOT**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



No se pudo completar la llamada para crear una alta superior en este objeto Transaction, porque el objeto Transaction especificado para la lista es una rama subordinada de transaction. Solo la raíz de la transacción se puede agregar como superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR \_ TRANSACTION \_ OBJECT \_ EXPIRED**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Dado que se ha cerrado el administrador de transacciones o el administrador de recursos asociado, el identificador ya no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR \_ TRANSACTION \_ RESPONSE \_ NOT \_ ENLISTED**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



La operación especificada no se pudo realizar en esta alta superior, porque la lista no se creó con la respuesta de finalización correspondiente en NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**REGISTRO DE \_ \_ TRANSACCIÓN \_ DE ERROR DEMASIADO \_ LARGO**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



No se pudo realizar la operación especificada, porque el registro que se registraría era demasiado largo. Esto puede ocurrir debido a dos condiciones: o hay demasiadas inscciones en esta transacción, o bien la clase RecoveryInformation combinada que se registra en nombre de esas inscciones es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR \_ TRANSACCIÓN \_ IMPLÍCITA NO \_ \_ ADMITIDA**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



No se admite la transacción implícita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR AL \_ \_ INFRINGIR \_ LA INTEGRIDAD DE LA TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



El administrador de transacciones del kernel tenía que anular u olvidar la transacción porque bloqueaba el progreso hacia delante.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR \_ TRANSACTIONMANAGER \_ IDENTITY \_ MISMATCH**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



La identidad de TransactionManager proporcionada no coincide con la registrada en el archivo de registro de TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR \_ RM NO SE PUEDE \_ \_ \_ INMOVILIZAR PARA LA \_ \_ INSTANTÁNEA**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Esta operación de instantánea no puede continuar porque un administrador de recursos transaccional no se puede inmovilizar en su estado actual. Inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR \_ TRANSACTION \_ MUST \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



No se puede dar de alta la transacción con la enlistmentMask especificada, porque la transacción ya ha completado la fase de preparación previa. Para garantizar la corrección, ResourceManager debe cambiar a un modo de escritura a través y dejar de almacenar en caché los datos dentro de esta transacción. La alta solo para las fases de transacción posteriores puede seguir siendo correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR \_ TRANSACTION \_ NO \_ SUPERIOR**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



La transacción no tiene una alta superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**POSIBLES \_ DAÑOS \_ HEURÍSTICOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



El intento de confirmar la transacción se completó, pero es posible que alguna parte del árbol de transacciones no se confirmara correctamente debido a la heurística. Por lo tanto, es posible que algunos datos modificados en la transacción no se haya confirmado, lo que da lugar a una incoherencia transaccional. Si es posible, compruebe la coherencia de los datos asociados.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR \_ TRANSACTIONAL \_ CONFLICT**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



La función intentó usar un nombre que está reservado para su uso por otra transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR \_ RM \_ NOT \_ ACTIVE**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



La compatibilidad con transacciones en el administrador de recursos especificado no se ha iniciado o se ha cerrado debido a un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR \_ RM \_ METADATA \_ CORRUPT**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Los metadatos del rm se han dañado. Rm no funcionará.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR \_ DIRECTORY \_ NOT \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



El directorio especificado no contiene un administrador de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**TRANSACCIONES \_ DE ERROR \_ REMOTAS NO \_ ADMITIDAS**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



El servidor remoto o recurso compartido no admite operaciones de archivos con transacciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**TAMAÑO NO \_ VÁLIDO DEL REGISTRO DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



El tamaño del registro solicitado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**EL \_ OBJETO DE ERROR YA NO \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



El objeto (archivo, secuencia, vínculo) correspondiente al identificador se ha eliminado mediante una reversión del punto de retorno de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR \_ STREAM \_ MINIVERSION \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



No se encontró la miniversión de archivo especificada para este archivo de transacción abierto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR \_ STREAM \_ MINIVERSION \_ NOT \_ VALID**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Se encontró la miniversión de archivo especificada, pero se ha invalidado. La causa más probable es una reversión del punto de retorno de transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR \_ MINIVERSION \_ INACCESIBLE \_ DESDE LA \_ TRANSACCIÓN \_ ESPECIFICADA**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Una miniversión solo se puede abrir en el contexto de la transacción que la creó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR \_ NO SE PUEDE ABRIR \_ \_ MINIVERSION CON LA INTENCIÓN \_ \_ \_ MODIFY**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



No es posible abrir una miniversión con modificar el acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR \_ CANT \_ CREATE \_ MORE \_ STREAM \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



No es posible crear más miniversiones para esta secuencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR \_ REMOTE \_ FILE \_ VERSION \_ MISMATCH**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



El servidor remoto envió un número de versión no coincidente o Fid para un archivo abierto con transacciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**EL \_ IDENTIFICADOR DE ERROR YA NO ES \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



Una transacción ha invalidado el identificador. La causa más probable es la presencia de asignación de memoria en un archivo o un identificador abierto cuando la transacción finalizó o revierte al punto de guardado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR \_ NO \_ TXF \_ METADATA**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



No hay metadatos de transacción en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**SE \_ DETECTARON \_ DAÑOS EN EL REGISTRO \_ DE ERRORES**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Los datos de registro están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR \_ NO SE PUEDE RECUPERAR CON EL IDENTIFICADOR \_ \_ \_ \_ ABIERTO**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



El archivo no se puede recuperar porque todavía hay un identificador abierto en él.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR \_ RM \_ DESCONECTADO**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



El resultado de la transacción no está disponible porque el administrador de recursos responsable de ella se ha desconectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR \_ ENLISTMENT \_ NOT \_ SUPERIOR**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



La solicitud se rechazó porque la lista en cuestión no es una alta superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**RECUPERACIÓN \_ DE ERRORES NO \_ \_ NECESARIA**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



El administrador de recursos transaccional ya es coherente. La recuperación no es necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR \_ RM \_ YA \_ INICIADO**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



El administrador de recursos transaccional ya se ha iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**IDENTIDAD DEL \_ ARCHIVO DE ERROR NO \_ \_ \_ PERSISTENTE**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



El archivo no se puede abrir transaccionalmente, porque su identidad depende del resultado de una transacción sin resolver.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR \_ NO PUEDE INTERRUMPIR LA DEPENDENCIA \_ \_ \_ TRANSACCIONAL**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



La operación no se puede realizar porque otra transacción depende del hecho de que esta propiedad no cambiará.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR \_ CANT \_ CROSS \_ RM \_ BOUNDARY**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



La operación implicaría un único archivo con dos administradores de recursos transaccionales y, por tanto, no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR \_ TXF \_ DIR \_ NOT \_ EMPTY**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



El $Txf debe estar vacío para que esta operación se pueda realizar correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**EXISTEN \_ TRANSACCIONES INDOUBT \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



La operación dejaría un administrador de recursos transaccional en un estado incoherente y, por lo tanto, no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR \_ TM \_ VOLATILE**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



No se pudo completar la operación porque el administrador de transacciones no tiene un registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**HA \_ EXPIRADO EL \_ TEMPORIZADOR DE REVERSIÓN DE \_ ERRORES**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



No se pudo programar una reversión porque una reversión programada previamente ya se ha ejecutado o se ha puesto en cola para su ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR \_ TXF \_ ATTRIBUTE \_ CORRUPT**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



El atributo de metadatos transaccional del archivo o directorio está dañado e ilegible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR \_ EFS \_ NO PERMITIDO EN \_ LA \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



No se pudo completar la operación de cifrado porque una transacción está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR \_ NO SE PERMITE ABRIR \_ \_ \_ TRANSACCIONAL**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



No se permite que este objeto se abra en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR DE \_ CRECIMIENTO DEL REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Error al intentar crear espacio en el registro del administrador de recursos transaccional. El estado de error se ha registrado en el registro de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR \_ DE \_ ASIGNACIÓN DE TRANSACCIONES \_ NO ADMITIDA \_ REMOTA**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



No se admite la asignación de memoria (creación de una sección asignada) de un archivo remoto en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR \_ TXF \_ METADATA \_ ALREADY \_ PRESENT**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Los metadatos de transacción ya están presentes en este archivo y no se pueden reemplazar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**DEVOLUCIONES DE \_ LLAMADA DE ÁMBITO DE \_ \_ TRANSACCIÓN DE ERROR NO \_ \_ ESTABLECIDAS**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



No se pudo especificar un ámbito de transacción porque no se ha inicializado el controlador de ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**PROMOCIÓN NECESARIA \_ DE \_ TRANSACCIÓN \_ DE ERROR**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



La promoción era necesaria para permitir que el administrador de recursos se dara de alta, pero la transacción se estableció para no permitirla.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR \_ NO SE PUEDE EJECUTAR EL ARCHIVO EN LA \_ \_ \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Este archivo está abierto para su modificación en una transacción sin resolver y solo un lector de transacciones puede abrir para su ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**TRANSACCIONES \_ DE ERROR NO \_ \_ INMOVILIZADAS**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



La solicitud de descongelar transacciones inmovilizadas se omitió porque las transacciones no se habían inmovilizado previamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR \_ DE \_ INMOVILIZACIÓN DE \_ TRANSACCIONES EN \_ CURSO**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Las transacciones no se pueden inmovilizar porque ya hay una inmovilización en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR \_ NO VOLUMEN DE \_ \_ INSTANTÁNEAS**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



El volumen de destino no es un volumen de instantáneas. Esta operación solo es válida en un volumen montado como una instantánea.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR \_ NO \_ SAVEPOINT \_ WITH \_ OPEN \_ FILES**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



Error en la operación de punto de guardado porque los archivos están abiertos en la transacción. Esto no se permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**REPARACIÓN PERDIDA \_ DE \_ DATOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows ha detectado daños en un archivo y ese archivo se ha reparado desde entonces. Es posible que se haya producido una pérdida de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR \_ DISPERSO NO PERMITIDO EN LA \_ \_ \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



No se pudo completar la operación dispersa porque una transacción está activa en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR \_ TM \_ IDENTITY \_ MISMATCH**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



Error en la llamada para crear un objeto TransactionManager porque la identidad de Tm almacenada en el archivo de registro no coincide con la identidad tm que se pasó como argumento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**SECCIÓN \_ FLOTANTE DE \_ ERROR**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Se intentó realizar E/S en un objeto de sección que se ha flotante como resultado de una finalización de la transacción. No hay datos válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR \_ NO SE PUEDE ACEPTAR EL TRABAJO DE \_ \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



El administrador de recursos transaccional no puede aceptar actualmente el trabajo de transacción debido a una condición transitoria, como los recursos bajos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR \_ NO SE PUEDEN ANULAR \_ \_ TRANSACCIONES**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



El administrador de recursos transaccional tenía demasiadas tranacciones pendientes que no se pudieron anular. Se ha cerrado el administrador de recursos transaccional.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**CLÚSTERES \_ \_ CON ERRORES**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



No se pudo completar la operación debido a clústeres no correctos en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**COMPRESIÓN \_ DE ERRORES NO PERMITIDA EN LA \_ \_ \_ \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



No se pudo completar la operación de compresión porque una transacción está activa en el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR \_ EN EL VOLUMEN \_ DESDESOCIADO**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



No se pudo completar la operación porque el volumen está desnuciado. Ejecute chkdsk e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR \_ NO \_ LINK \_ TRACKING \_ IN \_ TRANSACTION**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



No se pudo completar la operación de seguimiento de vínculos porque una transacción está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**OPERACIÓN \_ DE ERROR NO ADMITIDA EN \_ \_ \_ TRANSACTION \_**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Esta operación no se puede realizar en una transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**IDENTIFICADOR DE ERROR \_ \_ EXPIRADO**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



El identificador ya no está asociado correctamente a su transacción. Es posible que se haya abierto en un administrador de recursos transaccional que posteriormente se vio obligado a reiniciarse. Cierre el identificador y abra uno nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR \_ TRANSACTION \_ NOT \_ ENLISTED**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



No se pudo realizar la operación especificada porque el administrador de recursos no está dado de alta en la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR \_ CTX \_ WINSTATION \_ NAME \_ INVALID**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



El nombre de sesión especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR \_ CTX \_ INVALID \_ PD**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



El controlador de protocolo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR \_ CTX \_ PD \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



No se encontró el controlador de protocolo especificado en la ruta de acceso del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR \_ CTX \_ WD \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



No se encontró el controlador de conexión de terminal especificado en la ruta de acceso del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR \_ CTX \_ NO PUEDE REALIZAR LA ENTRADA DEL REGISTRO DE \_ \_ \_ EVENTOS**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



No se pudo crear una clave del Registro para el registro de eventos para esta sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR \_ CTX \_ SERVICE \_ NAME \_ COLLISION**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Ya existe un servicio con el mismo nombre en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR \_ CTX \_ CLOSE \_ PENDING**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Hay una operación de cierre pendiente en la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR \_ CTX \_ NO \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



No hay búferes de salida disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR \_ CTX \_ MODEM \_ INF \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



MÓDEM. No se encontró el archivo INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR \_ CTX \_ INVALID \_ MODEMNAME**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



El nombre del módem no se encontró en MODEM.INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR \_ CTX \_ MODEM \_ RESPONSE \_ ERROR**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



El módem no aceptó el comando que se le envió. Compruebe que el nombre del módem configurado coincide con el módem conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR \_ CTX \_ MODEM \_ RESPONSE \_ TIMEOUT**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



El módem no respondió al comando que se le envió. Compruebe que el módem está cableado y encendido correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR \_ CTX \_ MODEM \_ RESPONSE \_ NO \_ CARRIER**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



Se ha detectado un error en la detección del operador o se ha eliminado el operador debido a la desconexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR \_ CTX \_ MODEM \_ RESPONSE \_ NO \_ DIALTONE**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



No se detectó el tono de marcado en el tiempo necesario. Compruebe que el cable del teléfono está conectado correctamente y funciona.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR \_ RESPUESTA DE MÓDEM CTX \_ \_ \_ OCUPADA**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Se detectó una señal ocupada en el sitio remoto en la devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR \_ CTX \_ MODEM \_ RESPONSE \_ VOICE**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Se detectó la voz en el sitio remoto en la devolución de llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR \_ CTX \_ TD \_ ERROR**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Error del controlador de transporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR \_ CTX \_ WINSTATION \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



No se encuentra la sesión especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR \_ CTX \_ WINSTATION \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



El nombre de sesión especificado ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR \_ CTX \_ WINSTATION \_ BUSY**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



La tarea que intenta realizar no se puede completar porque Servicios de Escritorio remoto está ocupado actualmente. Inténtalo de nuevo al cabo de un rato. Otros usuarios todavía deben poder iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR \_ CTX \_ BAD \_ VIDEO \_ MODE**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Se ha intentado conectarse a una sesión cuyo modo de vídeo no es compatible con el cliente actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR \_ CTX \_ GRAPHICS \_ INVALID**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



La aplicación intentó habilitar el modo de gráficos DOS. No se admite el modo gráfico DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR \_ CTX \_ LOGON \_ DISABLED**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Se ha deshabilitado el privilegio de inicio de sesión interactivo. Póngase en contacto con el administrador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR \_ CTX \_ NOT \_ CONSOLE**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



La operación solicitada solo se puede realizar en la consola del sistema. Esto suele ser el resultado de un controlador o dll del sistema que requiere acceso directo a la consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR \_ CTX \_ CLIENT \_ QUERY \_ TIMEOUT**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



El cliente no pudo responder al mensaje de conexión del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR \_ CTX \_ CONSOLE \_ DISCONNECT**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



No se admite la desconexión de la sesión de consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR \_ CTX \_ CONSOLE \_ CONNECT**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



No se admite la reconexión de una sesión desconectada a la consola.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR \_ CTX \_ SHADOW \_ DENIED**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



Se denegó la solicitud para controlar otra sesión de forma remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR \_ CTX \_ WINSTATION \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



Se deniega el acceso a la sesión solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR \_ CTX \_ INVALID \_ WD**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



El controlador de conexión de terminal especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR \_ CTX \_ SHADOW \_ INVALID**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



La sesión solicitada no se puede controlar de forma remota. Esto puede deberse a que la sesión está desconectada o no tiene un usuario conectado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR \_ CTX \_ SHADOW \_ DISABLED**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



La sesión solicitada no está configurada para permitir el control remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR \_ CTX \_ CLIENT \_ LICENSE \_ IN \_ USE**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Se ha rechazado la solicitud para conectarse a este servidor de Terminal Server. Otro usuario está utilizando actualmente el número de licencia de cliente de Terminal Server. Llame al administrador del sistema para obtener un número de licencia único.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR \_ CTX \_ CLIENT \_ LICENSE \_ NOT \_ SET**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Se ha rechazado la solicitud para conectarse a este servidor de Terminal Server. No se ha especificado el número de licencia del cliente de Terminal Server para esta copia del cliente de Terminal Server. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR \_ LA LICENCIA CTX NO ESTÁ \_ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



El número de conexiones a este equipo es limitado y todas las conexiones están en uso en este momento. Intente conectarse más tarde o póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR \_ CTX \_ LICENSE \_ CLIENT \_ INVALID**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



El cliente que usa no tiene licencia para usar este sistema. Se deniega la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR \_ LA LICENCIA DE CTX \_ \_ EXPIRÓ**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



La licencia del sistema ha expirado. Se deniega la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR \_ CTX \_ SHADOW \_ NOT \_ RUNNING**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



No se pudo finalizar el control remoto porque la sesión especificada no se está controlando de forma remota actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR \_ CTX \_ SHADOW \_ ENDED \_ BY \_ MODE \_ CHANGE**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



El control remoto de la consola se finalizó porque se cambió el modo de presentación. No se admite el cambio del modo de presentación en una sesión de control remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**NÚMERO DE \_ ACTIVACIÓN \_ DE ERRORES \_ SUPERADO**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



La activación ya se ha restablecido el número máximo de veces para esta instalación. El temporizador de activación no se borrará.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR \_ CTX \_ WINSTATIONS \_ DISABLED**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Los inicios de sesión remotos están deshabilitados actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR \_ SE REQUIERE EL NIVEL DE CIFRADO \_ \_ \_ CTX**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



No tiene el nivel de cifrado adecuado para acceder a esta sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR \_ CTX \_ SESSION \_ IN \_ USE**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



El usuario %s \\ \\ %s ha iniciado sesión actualmente en este equipo. Solo el usuario actual o un administrador pueden iniciar sesión en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR \_ CTX \_ NO \_ FORCE \_ LOGOFF**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



El usuario %s \\ \\ %s ya ha iniciado sesión en la consola de este equipo. No tiene permiso para iniciar sesión en este momento. Para resolver este problema, póngase en contacto con %s \\ \\ %s y haga que cierren la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR \_ RESTRICCIÓN DE LA CUENTA \_ CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



No se puede iniciar sesión debido a una restricción de cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR \_ DEL PROTOCOLO RDP \_ \_**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



El componente de protocolo RDP %2 detectó un error en la secuencia de protocolo y desconectó el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR \_ CTX \_ CDM \_ CONNECT**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



El servicio de asignación de unidades de cliente se ha conectado en la conexión de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR \_ CTX \_ CDM \_ DISCONNECT**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



El servicio de asignación de unidades de cliente se ha desconectado en la conexión de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR \_ CTX \_ SECURITY \_ LAYER \_ ERROR**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



La capa de seguridad de Terminal Server detectó un error en el flujo de protocolo y desconectó el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**SESIONES \_ INCOMPATIBLES DE TS \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



La sesión de destino no es compatible con la sesión actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR \_ DEL SUBSISTEMA DE \_ \_ VÍDEO TS \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows no se puede conectar a la sesión porque se produjo un problema en el subsistema Windows vídeo. Intente conectarse de nuevo más tarde o póngase en contacto con el administrador del servidor para obtener ayuda.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS \_ ERR \_ INVALID \_ API \_ SEQUENCE**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



Se llamó incorrectamente a la API del servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**SERVICIO DE INICIO \_ DE ERROR \_ DE FRS \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



No se puede iniciar el servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**SERVICIO DE DETENCIÓN \_ DE ERRORES \_ DE FRS \_**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



No se puede detener el servicio de replicación de archivos.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS \_ ERR \_ INTERNAL \_ API**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



La API del servicio de replicación de archivos finalizó la solicitud. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ ERR \_ INTERNAL**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



El servicio de replicación de archivos finalizó la solicitud. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ ERR \_ SERVICE \_ COMM**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



No se puede ponerse en contacto con el servicio de replicación de archivos. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ ERR \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**AUTENTICACIÓN DE ERRORES DE FRS \_ \_**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ ERR \_ PARENT \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes en el controlador de dominio. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**AUTENTICACIÓN \_ PRIMARIA DE FRS ERR \_ \_**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible en el controlador de dominio. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ ERR \_ CHILD \_ TO \_ PARENT \_ COMM**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



El servicio de replicación de archivos no puede comunicarse con el servicio de replicación de archivos en el controlador de dominio. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ ERR \_ PARENT \_ TO \_ CHILD \_ COMM**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



El servicio de replicación de archivos en el controlador de dominio no puede comunicarse con el servicio de replicación de archivos en este equipo. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ ERR \_ SYSVOL \_ POPULATE**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un error interno. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ ERR \_ SYSVOL \_ POPULATE \_ TIMEOUT**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un tiempo de espera interno. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ ERR \_ SYSVOL ESTÁ \_ \_ OCUPADO**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



El servicio de replicación de archivos no puede procesar la solicitud. El volumen del sistema está ocupado con una solicitud anterior.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ ERR \_ SYSVOL \_ DEMOTE**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



El servicio de replicación de archivos no puede detener la replicación del volumen del sistema debido a un error interno. El registro de eventos puede tener más información.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS \_ ERR \_ INVALID \_ SERVICE \_ PARAMETER**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



El servicio de replicación de archivos detectó un parámetro no válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




