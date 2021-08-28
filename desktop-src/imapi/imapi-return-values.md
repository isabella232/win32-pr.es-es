---
title: Valores devueltos de IMAPI (Imapi2error.h)
description: Los métodos IMAPI devuelven valores no negativos (normalmente S \_ OK) si el método se ha realizado correctamente. Los métodos IMAPI devuelven códigos de error o correctos de Winerror.h, Imapi2error.h o Imapi2fserror.h, en caso de error.
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857f9c018fc34a16a0dc431714aacc1fcdf6a5b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474801"
---
# <a name="imapi-return-values"></a>Valores devueltos de IMAPI

Los métodos IMAPI devuelven valores no negativos (normalmente S \_ OK) si el método se ha realizado correctamente. Los métodos IMAPI devuelven códigos de error o correctos de Winerror.h, Imapi2error.h o Imapi2fserror.h, en caso de error.

Se definen los siguientes códigos de error y correcto.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt><dt>(HRESULT)0xC0AA0007L</dt></dl> | El disco no pasó la comprobación de la grabación y puede contener datos dañados o ser inutilizables.<br /> | 
| <span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt><dt>(HRESULT)0xC0AA0002</dt></dl> | Se ha cancelado la solicitud.<br /> | 
| <span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt><dt>(HRESULT)0xC0AA0003</dt></dl> | La solicitud requiere que se seleccione una grabadora de disco actual.<br /> | 
| <span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0x00AA0302L</dt></dl> | Actualmente no hay ninguna operación de escritura en curso.<br /> | 
| <span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt><dt>(HRESULT)0x00AA0004</dt></dl> | La unidad no admite la velocidad de escritura solicitada y se ha ajustado la velocidad.<br /> | 
| <span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt><dt>(HRESULT)0x00AA0005</dt></dl> | La unidad no admite el tipo de rotación solicitado y se ha ajustado el tipo de rotación.<br /> | 
| <span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt><dt>(HRESULT)0x00AA0006</dt></dl> | La unidad no admite la velocidad de escritura y el tipo de rotación solicitados y ambos se ajustaron.<br /> | 
| <span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt><dt>(HRESULT)0x00AA0200</dt></dl> | El dispositivo aceptó el comando, pero devolvió los datos de sense, lo que indica un error.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt><dt>(HRESULT)0x80AA0A0A00L</dt></dl> | La imagen se ha convertido en de solo lectura debido a una llamada a <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>. Como resultado, el objeto ya no se puede modificar.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt><dt>(HRESULT)0x80AA0A01L</dt></dl> | No se pueden agregar más pistas. Los medios de CD están restringidos a un intervalo de entre 1 y 99 pistas.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt><dt>(HRESULT)0x80AA0A03L</dt></dl> | Se deben agregar pistas a la imagen antes de usar esta función.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0x80AA0A02L</dt></dl> | No se admite el tipo de sector solicitado.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt><dt>(HRESULT)0x80AA0A0A04L</dt></dl> | Es posible que no se puedan agregar pistas a la imagen antes de usar esta función.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt><dt>(HRESULT)0x80AA0A05L</dt></dl> | Agregar esta pista superaría las limitaciones del inicio del cliente potencial.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt><dt>(HRESULT)0x80AA0A06L</dt></dl> | Agregar esta pista superaría el límite de índice 99.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt><dt>(HRESULT)0x80AA0A0A07L</dt></dl> | El desplazamiento de LBA especificado no está en la lista de índices de seguimiento.<br /> | 
| <span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt><dt>(HRESULT)0x00AA0A0A08L</dt></dl> | El desplazamiento de LBA especificado ya está en la lista de índices de seguimiento.<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt><dt>(HRESULT)0x80AA0A0A09L</dt></dl> | No se puede borrar el índice 1 (desplazamiento LBA cero).<br /> | 
| <span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt><dt>(HRESULT)0x80AA0A0AL</dt></dl> | Cada índice debe tener un tamaño mínimo de diez sectores.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt><dt>(HRESULT)0xC0AA0201</dt></dl> | El dispositivo informó de que la página del modo solicitado (y el tipo) no está presente.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt><dt>(HRESULT)0xC0AA0202</dt></dl> | No hay ningún medio en el dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt><dt>(HRESULT)0xC0AA0203</dt></dl> | El medio no es compatible o tiene un formato físico desconocido.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt><dt>(HRESULT)0xC0AA0204</dt></dl> | El medio se inserta al revés.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt><dt>(HRESULT)0xC0AA0205</dt></dl> | La unidad informó de que está en proceso de prepararse. Vuelva a intentar la solicitud más adelante.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0206</dt></dl> | Actualmente se está formateando el medio. Espere a que el formato se complete antes de intentar usar los medios.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt><dt>(HRESULT)0xC0AA0207</dt></dl> | La unidad informó de que está realizando una operación de larga duración, como finalizar una escritura. La unidad puede ser inutilizable durante un largo período de tiempo.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt><dt>(HRESULT)0xC0AA0208</dt></dl> | La unidad informó de que no se admite la combinación de parámetros proporcionada en la página de modo para un comando MODE SELECT.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt><dt>(HRESULT)0xC0AA0209</dt></dl> | La unidad informó de que el medio está protegido por escritura.<br /> | 
| <span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt><dt>(HRESULT)0xC0AA020A</dt></dl> | El dispositivo no admite la página de características solicitada.<br /> | 
| <span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt><dt>(HRESULT)0xC0AA020B</dt></dl> | Se admite la página de características solicitada, pero no está marcada como actual.<br /> | 
| <span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA020C</dt></dl> | La unidad no admite el comando GET CONFIGURATION.<br /> | 
| <span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt><dt>(HRESULT)0xC0AA020D</dt></dl> | El dispositivo no pudo aceptar el comando dentro del período de tiempo de espera. Esto puede deberse a que el dispositivo ha entrado en un estado incoherente o es posible que sea necesario aumentar el valor de tiempo de espera del comando.<br /> | 
| <span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt><dt>(HRESULT)0xC0AA020E</dt></dl> | La estructura de DVD no está presente. Esto puede deberse a que se usa una unidad o un medio incompatibles.<br /> | 
| <span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt><dt>(HRESULT)0xC0AA020F</dt></dl> | La velocidad del medio no es compatible con el dispositivo. Esto puede deberse al uso de medios de mayor o menor velocidad que el intervalo de velocidades admitido por el dispositivo.<br /> | 
| <span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt><dt>(HRESULT)0xC0AA0210</dt></dl> | El dispositivo asociado a esta grabadora durante la última operación se ha bloqueado exclusivamente, lo que provoca un error en esta operación.<br /> | 
| <span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0211</dt></dl> | El nombre de cliente no es válido.<br /> | 
| <span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA02FF</dt></dl> | El dispositivo informó de datos inesperados o no válidos para un comando.<br /> | 
| <span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt><dt>(HRESULT)0xC0AA0300</dt></dl> | Error de escritura porque la unidad no recibió datos lo suficientemente rápido como para continuar escribiendo. El traslado de los datos de origen al equipo local, la reducción de la velocidad de escritura o la habilitación de una opción "buffer underrun free" puede resolver este problema.<br /> | 
| <span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt><dt>(HRESULT)0xC0AA0301</dt></dl> | Error de escritura porque la unidad devolvió información de error de la que no se pudo recuperar.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0400</dt></dl> | Actualmente hay una operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0401</dt></dl> | Actualmente no hay ninguna operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt><dt>(HRESULT)0xC0AA0402</dt></dl> | La operación solicitada solo es válida con medios admitidos.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0403</dt></dl> | No se admite la secuencia proporcionada para escribir.<br /> | 
| <span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt><dt>(HRESULT)0xC0AA0404</dt></dl> | La secuencia proporcionada para escribir es demasiado grande para los medios insertados actualmente.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0405</dt></dl> | No se permite sobrescribir medios que no están en blanco sin la propiedad ForceOverwrite establecida en VARIANT_TRUE.<br /> | 
| <span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0406</dt></dl> | No se admite el tipo de medio actual.<br /> | 
| <span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0407</dt></dl> | Este dispositivo no admite las operaciones requeridas por este formato de disco.<br /> | 
| <span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0408</dt></dl> | El nombre del cliente no es válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0500</dt></dl> | Actualmente hay una operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0501</dt></dl> | Actualmente no hay ninguna operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0502</dt></dl> | La operación solicitada solo es válida cuando los medios se han "preparado".<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0503</dt></dl> | La operación solicitada no es válida cuando los medios se han "preparado" pero no se han liberado.<br /> | 
| <span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt><dt>(HRESULT)0xC0AA0504</dt></dl> | No se puede cambiar la propiedad una vez que se ha escrito el medio en .<br /> | 
| <span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt><dt>(HRESULT)0xC0AA0505</dt></dl> | La tabla de contenido no se puede recuperar de un disco vacío.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0506</dt></dl> | Solo se admiten medios CD-R/RW en blanco.<br /> | 
| <span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0507</dt></dl> | Solo se admiten medios CD-R/RW en blanco.<br /> | 
| <span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt><dt>(HRESULT)0xC0AA0508</dt></dl> | Los medios CD-R y CD-RW admiten un máximo de 99 pistas de audio.<br /> | 
| <span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT)0xC0AA0509</dt></dl> | No queda espacio suficiente en los medios para agregar la pista de audio proporcionada.<br /> | 
| <span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT)0xC0AA050A</dt></dl> | No puede preparar el medio hasta que elija una grabadora para usarla.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt><dt>(HRESULT)0xC0AA050B</dt></dl> | El ISRC proporcionado no es válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt><dt>(HRESULT)0xC0AA050C</dt></dl> | El número de catálogo multimedia proporcionado no es válido.<br /> | 
| <span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA050D</dt></dl> | La secuencia de audio proporcionada no es válida.<br /> | 
| <span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA050E</dt></dl> | Este dispositivo no admite las operaciones requeridas por este formato de disco.<br /> | 
| <span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA050F</dt></dl> | El nombre del cliente no es válido.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0600</dt></dl> | Actualmente hay una operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt><dt>(HRESULT)0xC0AA0601</dt></dl> | Actualmente no hay ninguna operación de escritura en curso.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0602</dt></dl> | La operación solicitada solo es válida cuando los medios se han "preparado".<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt><dt>(HRESULT)0xC0AA0603</dt></dl> | La operación solicitada no es válida cuando los medios se han "preparado" pero no se han liberado.<br /> | 
| <span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA0604</dt></dl> | El nombre del cliente no es válido.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt><dt>(HRESULT)0xC0AA0606</dt></dl> | Solo se admiten medios CD-R/RW en blanco.<br /> | 
| <span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0607</dt></dl> | Solo se admiten medios CD-R/RW en blanco.<br /> | 
| <span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt><dt>(HRESULT)0xC0AA0609</dt></dl> | No hay suficiente espacio en los medios para agregar la sesión proporcionada.<br /> | 
| <span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt><dt>(HRESULT)0xC0AA060A</dt></dl> | No puede preparar el medio hasta que elija una grabadora para usarla.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA060D</dt></dl> | La secuencia de audio proporcionada no es válida.<br /> | 
| <span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA060E</dt></dl> | El tipo de bloque de datos solicitado no es compatible con el dispositivo actual.<br /> | 
| <span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt><dt>(HRESULT)0xC0AA060F</dt></dl> | La secuencia no contiene un número suficiente de sectores en el cliente potencial para los medios actuales.<br /> | 
| <span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0610</dt></dl> | Este dispositivo no admite las operaciones requeridas por este formato de disco.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt><dt>(HRESULT)0x80AA0900</dt></dl> | El formato usa actualmente la grabadora de discos para una operación de borrado. Espere a que se complete el borrado antes de intentar establecer o borrar la grabadora de disco actual.<br /> | 
| <span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt><dt>(HRESULT)0x80AA0901</dt></dl> | El formato de borrado solo admite una grabadora. Debe borrar la grabadora actual antes de establecer una nueva.<br /> | 
| <span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt><dt>(HRESULT)0x80AA0902</dt></dl> | La unidad no notifió suficientes datos para un comando READ DISC INFORMATION. Es posible que la unidad no sea compatible o que el medio no sea correcto.<br /> | 
| <span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt><dt>(HRESULT)0x80AA0903</dt></dl> | La unidad no notifió suficientes datos para un comando MODE SENSE (página 0x2A). Es posible que la unidad no sea compatible o que el medio no sea correcto.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt><dt>(HRESULT)0x80AA0904</dt></dl> | La unidad informó de que el medio no se puede borrar.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt><dt>(HRESULT)0x80AA0905</dt></dl> | Error en la unidad del comando de borrado.<br /> | 
| <span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt><dt>(HRESULT)0x80AA0906</dt></dl> | La unidad no ha completado el borrado en una hora. La unidad puede requerir un ciclo de energía, la eliminación de medios u otra intervención manual para reanudar el funcionamiento correcto.<br /><blockquote>[!Note]<br />Actualmente, este valor también se devolverá si se produce un error en un intento de borrar en medios CD-RW o DVD-RW a través de la interfaz <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> como resultado de que el medio sea malo.</blockquote><br /> | 
| <span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt><dt>(HRESULT)0x80AA0907</dt></dl> | La unidad devolvió un error inesperado durante el borrado. Es posible que el medio no se pueda usar, que el borrado esté completo o que la unidad todavía esté en proceso de borrar el disco.<br /> | 
| <span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt><dt>(HRESULT)0x80AA0908</dt></dl> | La unidad devolvió un error para un comando START UNIT (spinup). Puede ser necesaria la intervención manual.<br /> | 
| <span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA0909</dt></dl> | No se admite el tipo de medio actual.<br /> | 
| <span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AA090A</dt></dl> | Este dispositivo no admite las operaciones requeridas por este formato de disco.<br /> | 
| <span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt><dt>(HRESULT)0xC0AA090B</dt></dl> | El nombre de cliente no es válido.<br /> | 




Los siguientes códigos de error y correcto se definen en Imapi2fserror.h.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt><dt>(HRESULT)0xC0AAB100</dt></dl> | Error interno: %1!ls!.<br /> | 
| <span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt><dt>(HRESULT)0xC0AAB101</dt></dl> | Valor especificado para el parámetro '%1!ls!' no es válida.<br /> | 
| <span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl><dt><strong>IMAPI_E_READONLY</strong></dt><dt>(HRESULT)0xC0AAB102</dt></dl> | El objeto FileSystemImage está en modo de solo lectura.<br /> | 
| <span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt><dt>(HRESULT)0xC0AAB103</dt></dl> | No se ha especificado ningún sistema de archivos de salida.<br /> | 
| <span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt><dt>(HRESULT)0xC0AAB104</dt></dl> | El identificador de volumen especificado es demasiado largo o contiene uno o varios caracteres no válidos.<br /> | 
| <span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl><dt><strong>IMAPI_E_INVALID_DATE</strong></dt><dt>(HRESULT)0xC0AAB105</dt></dl> | Fechas de archivo no válidas. %1!ls! el tiempo es anterior a %2!ls! momento.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB106</dt></dl> | El sistema de archivos debe estar vacío para esta función.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt><dt>(HRESULT)0xC0AAB163L</dt></dl> | No se puede cambiar el sistema de archivos especificado para su creación, porque el sistema de archivos de la sesión importada y el sistema de archivos de la sesión actual no coinciden.<br /> | 
| <span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl><dt><strong>IMAPI_E_NOT_FILE</strong></dt><dt>(HRESULT)0xC0AAB108</dt></dl> | Ruta de acceso especificada '%1!ls!' no identifica un archivo.<br /> | 
| <span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl><dt><strong>IMAPI_E_NOT_DIR</strong></dt><dt>(HRESULT)0xC0AAB109</dt></dl> | Ruta de acceso especificada '%1!ls!' no identifica un directorio.<br /> | 
| <span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt><dt>(HRESULT)0xC0AAB10A</dt></dl> | El directorio '%1!s!' no está vacío.<br /> | 
| <span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt><dt>(HRESULT)0xC0AAB10B</dt></dl> | ls!' no forma parte del sistema de archivos. Debe agregarse para completar esta operación.<br /> | 
| <span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl><dt><strong>IMAPI_E_INVALID_PATH</strong></dt><dt>(HRESULT)0xC0AAB110</dt></dl> | Ruta de acceso '%1!s!' tiene un formato no correcto o contiene caracteres no válidos.<br /> | 
| <span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt><dt>(HRESULT)0xC0AAB111</dt></dl> | El nombre '%1!ls!' especificado no es válido: el nombre del objeto de archivo o directorio creado mientras se establece la propiedad UseRestrictedCharacterSet solo puede contener caracteres ANSI.<br /> | 
| <span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl><dt><strong>IMAPI_E_DUP_NAME</strong></dt><dt>(HRESULT)0xC0AAB112</dt></dl> | ls!' name ya existe.<br /> | 
| <span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt><dt>(HRESULT)0xC0AAB113</dt></dl> | Intento de agregar '%1!ls!' error: no se puede crear un nombre único específico del sistema de archivos para %2!ls! .<br /> | 
| <span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB118</dt></dl> | No se encuentra el elemento '%1!ls!' en FileSystemImage hierarchy.<br /> | 
| <span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB119</dt></dl> | El archivo '%1!s!' no se encuentra en la jerarquía FileSystemImage.<br /> | 
| <span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB11A</dt></dl> | El directorio '%1!s!' no se encuentra en la jerarquía FileSystemImage.<br /> | 
| <span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt><dt>(HRESULT)0xC0AAB120</dt></dl> | Agregar "%1!ls!". daría lugar a que una imagen de resultado tenga un tamaño mayor que el límite configurado actual.<br /> | 
| <span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB121</dt></dl> | El valor especificado para la propiedad FreeMediaBlocks es demasiado pequeño para el tamaño estimado de la imagen en función de los datos actuales. <br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt><dt>(HRESULT)0xC0AAB200L</dt></dl> | La imagen no está alineada en un límite de sector de 2 kb.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt><dt>(HRESULT)0xC0AAB201L)</dt></dl> | La imagen no contiene un descriptor de volumen válido.<br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt><dt>(HRESULT)0xC0AAB202L</dt></dl> | La imagen no se ha establecido mediante los métodos <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> o <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> antes de llamar al <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>método IIsoImageManager::Validate.</strong></a><br /> | 
| <span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB203L</dt></dl> | La imagen proporcionada es demasiado grande para validarse, ya que el tamaño supera <strong>MAXLONG.</strong><br /> | 
| <span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt><dt>(HRESULT)0xC0AAB128</dt></dl> | Flujo de datos proporcionado para el archivo '%1!ls!' es incoherente: se esperaba %2. I64d! bytes, se encontró %3! I64d!. <br /> | 
| <span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB129</dt></dl> | No se pueden leer datos de la secuencia proporcionada para el archivo '%1!ls!'.<br /> | 
| <span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12A</dt></dl> | Se encontró el siguiente error al intentar crear un flujo de datos para el archivo '%1!ls!': <br /> | 
| <span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB12BL</dt></dl> | No se puede acceder a los archivos en el árbol de directorios debido a permisos.<br /> | 
| <span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt><dt>(HRESULT)0xC0AAB130</dt></dl> | Esta imagen del sistema de archivos tiene demasiados directorios para %1!ls! .<br /> | 
| <span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt><dt>(HRESULT)0xC0AAB131</dt></dl> | ISO9660 está limitado a 8 niveles de directorios.<br /> | 
| <span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt><dt>(HRESULT)0xC0AAB132</dt></dl> | El archivo de datos es demasiado grande para '%1!ls!' .<br /> | 
| <span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB138</dt></dl> | No se puede inicializar %1!ls! archivo stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB139</dt></dl> | Error al buscar en '%1!ls!' archivo stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB13A</dt></dl> | Error al escribir en '%1!ls!' archivo stash.<br /> | 
| <span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB13B</dt></dl> | Error al leer "%1!ls!". archivo stash.<br /> | 
| <span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt><dt>(HRESULT)0xC0AAB140</dt></dl> | El directorio de trabajo '%1!ls!' no es válida.<br /> | 
| <span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt><dt>(HRESULT)0xC0AAB141</dt></dl> | No se puede establecer el directorio de trabajo en '%1!ls!'. El espacio disponible es %2. I64d! bytes, aproximadamente %3! I64d! bytes requeridos. <br /> | 
| <span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt><dt>(HRESULT)0xC0AAB142</dt></dl> | Intento de mover el archivo de almacenamiento temporal de datos al directorio '%1!ls!' no se ha realizado correctamente.<br /> | 
| <span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt><dt>(HRESULT)0xC0AAB148</dt></dl> | No se pudo agregar el objeto de arranque a la imagen.<br /> | 
| <span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt><dt>(HRESULT)0xC0AAB149</dt></dl> | Un objeto de arranque solo se puede incluir en una imagen de disco inicial.<br /> | 
| <span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt><dt>(HRESULT)0xC0AAB14A</dt></dl> | El tipo de emulación solicitado no coincide con el tamaño de la imagen de arranque.<br /> | 
| <span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt><dt>(HRESULT)0xC0AAB150</dt></dl> | Los medios ópticos están vacíos.<br /> | 
| <span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt><dt>(HRESULT)0xC0AAB151</dt></dl> | El disco especificado no contiene uno de los sistemas de archivos admitidos.<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt><dt>(HRESULT)0xC0AAB152</dt></dl> | El disco especificado no contiene '%1!ls!' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt><dt>(HRESULT)0xC0AAB153</dt></dl> | Error de coherencia al importar '%1!ls!' .<br /> | 
| <span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0xC0AAB154</dt></dl> | El '%1!ls!' El sistema de archivos del disco seleccionado contiene una característica que no se admite para la importación: %2!ls!.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt><dt>(HRESULT)0xC0AAB155</dt></dl> | No se pudo importar %2!ls! sistema de archivos del disco. El archivo '%1!ls!' ya existe en la jerarquía de imágenes como un directorio.<br /> | 
| <span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB156</dt></dl> | No se puede intentar bloquear %1. I64d! en el disco de origen. <br /> | 
| <span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt><dt>(HRESULT)0xC0AAB157</dt></dl> | Error al importar desde la sesión anterior debido a un error al leer un bloque en el medio (lo más probable es que bloque %1!u!).<br /> | 
| <span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt><dt>(HRESULT)0xC0AAB158</dt></dl> | El disco actual no es el mismo desde el que se importó el sistema de archivos.<br /> | 
| <span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt><dt>(HRESULT)0xC0AAB159</dt></dl> | IMAPI no permite varias sesiones con el tipo de medio actual.<br /> | 
| <span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt><dt>(HRESULT)0xC0AAB15A</dt></dl> | IMAPI no puede realizar varias sesiones con el medio actual porque no admite una revisión de UDF compatible para escritura.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT)0xC0AAB15B</dt></dl> | IMAPI no admite el tipo de multisesión solicitado.<br /> | 
| <span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt><dt>(HRESULT)0xC0AAB133</dt></dl> | Error en la operación debido a un diseño incompatible de la sesión anterior importada desde el medio.<br /> | 
| <span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt><dt>(HRESULT)0xC0AAB15C</dt></dl> | IMAPI no admite ninguno de los tipos de multisesión proporcionados en el medio actual.<br /><blockquote>[!Note]<br />[<strong>El método IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) devuelve este error si no hay ningún medio en el dispositivo de grabación.</blockquote><br /> | 
| <span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt><dt>(HRESULT)0xC0AAB15D</dt></dl> | La propiedad MultisessionInterfaces debe establecerse antes de llamar a este método.<br /> | 
| <span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt><dt>(HRESULT)0xC0AAB15E</dt></dl> | No se pudo importar %2!ls! sistema de archivos del disco. El directorio '%1!ls!' ya existe en la jerarquía de imágenes como un archivo.<br /> | 
| <span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt><dt>(HRESULT)0xC0AAB162</dt></dl> | Uno de los parámetros de varias sesiones no se puede recuperar o tiene un valor incorrecto.<br /> | 
| <span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt><dt>(HRESULT)0x00AAB15FL</dt></dl> | Esta característica no se admite para la revisión actual del sistema de archivos. La imagen se creará sin esta característica.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                            |
| Encabezado<br/>                   | <dl> <dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt> </dl> |



 

 





