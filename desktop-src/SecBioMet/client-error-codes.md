---
title: Códigos de error de cliente (Winbio \_ Err. h)
description: Códigos de error definidos en el \_ archivo de encabezado Winbio Err. h.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 000723612a2f7f9f5575fc767924d4d6c697468a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079676"
---
# <a name="client-error-codes"></a>Códigos de error de cliente

Los siguientes códigos de error se definen en el \_ archivo de encabezado Winbio Err. h.



| Constante o valor                                                                                                                                                                                                                                                                                         | Descripción                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ 0x80098001 \_ factor no admitido**</dt> <dt></dt> </dl>                              | No se admite el factor biométrico especificado.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E 0x80098002 de \_ \_ unidad no válida**</dt> <dt></dt> </dl>                                                | El número de ID. de unidad no se corresponde con un dispositivo biométrico válido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ \_ ID**</dt> <dt>0x80098003</dt> desconocido </dl>                                                      | El ejemplo biométrico no coincide con ninguna identidad conocida.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ cancelado**</dt> <dt>0x80098004</dt> </dl>                                                             | La operación biométrica se canceló antes de poder completarse.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ no hay \_ coincidencias**</dt> <dt>0x80098005</dt> </dl>                                                            | El ejemplo biométrico no coincide con la identidad o el subfactor especificados.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E \_ Capture \_ anulada**</dt> <dt>0x80098006</dt> </dl>                                       | No se pudo capturar un ejemplo biométrico porque se anuló la operación de captura.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ E \_ inscripción \_ en \_ curso**</dt> <dt>0x80098007</dt> </dl>                 | No se pudo iniciar una transacción de inscripción porque ya hay otra inscripción en curso.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E 0x80098008 de \_ \_ captura incorrecta**</dt> <dt></dt> </dl>                                                   | El ejemplo capturado no se puede usar para operaciones biométricas adicionales.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ código de control no válido**</dt> <dt>0x80098009</dt> </dl>                       | La unidad biométrica no admite el código de control de unidad especificado.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ E \_ \_ recopilación \_ de datos en \_ curso**</dt> <dt>0x8009800B</dt> </dl> | Ya hay una operación de recopilación de datos pendiente en curso.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ 0x8009800C formato de \_ datos \_ no admitido**</dt> <dt></dt> </dl>              | El controlador del sensor biométrico no admite el formato de datos solicitado.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E 0x8009800D de \_ \_ \_ tipo de datos no admitidos**</dt> <dt></dt> </dl>                    | El controlador del sensor biométrico no es compatible con el tipo de datos solicitado.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ 0x8009800E \_ propósito no compatible**</dt> <dt></dt> </dl>                           | El controlador del sensor biométrico no admite el propósito de los datos solicitados.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E 0x8009800F de \_ \_ \_ Estado de dispositivo no válidos**</dt> <dt></dt> </dl>                       | La unidad biométrica no está en el estado apropiado para realizar la operación especificada.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ Dispositivo E 0x80098010 \_ \_ ocupado**</dt> <dt></dt> </dl>                                                   | No se pudo realizar la operación porque el dispositivo de sensor estaba ocupado.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ La base de datos E no se pudo \_ \_ \_ crear**</dt> <dt>0x80098011</dt> </dl>                       | El adaptador de almacenamiento no pudo crear una nueva base de datos.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E no se pudo \_ \_ \_ abrir la base de datos**</dt> <dt>0x80098012</dt> </dl>                             | El adaptador de almacenamiento no pudo abrir una base de datos existente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E no se pudo \_ \_ \_ cerrar la base de datos**</dt> <dt>0x80098013</dt> </dl>                          | El adaptador de almacenamiento no pudo cerrar una base de datos.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ La base de datos E no se pudo \_ \_ \_ Borrar**</dt> <dt>0x80098014</dt> </dl>                          | El adaptador de almacenamiento no pudo borrar una base de datos.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ No \_ se \_ \_ encuentra la base de datos E**</dt> <dt>0x80098015</dt> </dl>                             | El adaptador de almacenamiento no pudo encontrar una base de datos.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ La \_ base de datos E \_ ya \_ existe**</dt> <dt>0x80098016</dt> </dl>              | El adaptador de almacenamiento no pudo crear una base de datos porque la base de datos especificada ya existe.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E & 0x80098018 \_ \_ completo**</dt> de la base de datos <dt></dt> </dl>                                             | El adaptador de almacenamiento no pudo agregar un registro a la base de datos porque la base de datos está llena.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E & 0x80098019 de \_ base de datos \_ bloqueada**</dt> <dt></dt> </dl>                                       | La base de datos está bloqueada y no se puede obtener acceso a su contenido.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ E 0x8009801A de \_ base de datos \_ dañada**</dt> <dt></dt> </dl>                              | El contenido de la base de datos se ha dañado y no se puede obtener acceso a él.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ \_Base de datos E \_ no \_ tal \_ registro**</dt> <dt>0x8009801B</dt> </dl>             | No se eliminó ningún registro porque la identidad y el subfactor especificados no están presentes en la base de datos.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ \_ inscripción duplicada**</dt> <dt>0x8009801C</dt> </dl>                        | La identidad y el subfactor especificados ya están inscritos en la base de datos.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E 0x8009801D de \_ \_ \_ error de lectura de base de datos**</dt> <dt></dt> </dl>                          | Se produjo un error al intentar leer la base de datos.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ \_Error de \_ escritura \_ de base de datos E**</dt> <dt>0x8009801E</dt> </dl>                       | Se produjo un error al intentar escribir en la base de datos.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E & 0x8009801F de \_ datos \_ sin \_ resultados**</dt> <dt></dt> </dl>                          | No hay registros en la base de datos que coincidan con la consulta.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ La \_ base de datos E \_ no hay \_ más \_ registros**</dt> <dt>0x80098020</dt> </dl>          | Se han recuperado todos los registros de la consulta de base de datos más reciente.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ base de datos \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Una operación de base de datos encontró inesperadamente el final del archivo.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ \_Vector de \_ \_ índice incorrecto \_ de la base de datos E**</dt> <dt>0x80098022</dt> </dl>       | No se pudo realizar una operación de base de datos debido a un vector de índice con formato incorrecto.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E 0x80098024 de \_ \_ BSP incorrecta**</dt> <dt></dt> </dl>                                             | La unidad biométrica no pertenece al proveedor de servicios especificado.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E 0x80098025 de \_ \_ \_ grupo de sensores incorrecto**</dt> <dt></dt> </dl>                    | La unidad biométrica no pertenece al grupo de sensores especificado.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ no \_ 0x80098026 \_ datos de captura**</dt> <dt></dt> </dl>                                      | El búfer de captura del adaptador de sensor está vacío.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ 0x80098027 \_ \_ modo de sensor no válido**</dt> <dt></dt> </dl>                          | El adaptador de sensor no es compatible con el modo de sensor especificado en la configuración.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ \_ infracción de bloqueo**</dt> <dt>0x8009802A</dt> </dl>                                          | No se puede realizar la operación solicitada debido a un conflicto de bloqueo.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ duplicar \_ plantilla**</dt> <dt>0x8009802B</dt> </dl>                              | Los datos de una plantilla biométrica coinciden con los de otra plantilla que ya está en la base de datos.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E 0x8009802C de \_ \_ operación no válida**</dt> <dt></dt> </dl>                                 | La operación solicitada no es válida para el estado actual de la sesión o de la unidad biométrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ sesión \_ ocupada**</dt> <dt>0x8009802D</dt> </dl>                                                | La sesión no puede iniciar una nueva operación porque ya hay otra operación en curso.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ Prov \_ deshabilitada**</dt> <dt>0x80098030</dt> </dl>                             | La configuración de directiva del sistema ha deshabilitado el proveedor de credenciales biométricas.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ Prov. \_ sin \_ credencial**</dt> <dt>0x80098031</dt> </dl>             | No se encontró la credencial solicitada.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ deshabilitar**</dt> <dt>0x80098032</dt> </dl>                                                             | La configuración de directiva del sistema ha deshabilitado el servicio biométrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ \_ \_ Error de configuración de E**</dt> <dt>0x80098033</dt> </dl>                     | No se pudo configurar la unidad biométrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ E \_ sensor \_ no disponible**</dt> <dt>0x80098034</dt> </dl>                              | No se puede crear un grupo privado porque una o varias unidades biométricas no están disponibles.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ habilitada**</dt> para <dt>0x80098035</dt> </dl>                                                   | Se requiere una secuencia de atención segura (CTRL-ALT-DELETE) para el inicio de sesión.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ E \_ \_**</dt> <dt>0x80098036</dt> de error de dispositivo </dl>                                          | Error en un sensor biométrico.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ \_Cambio de \_ usuario \_ rápido \_ deshabilitado**</dt> <dt>0x80098037</dt> </dl>       | >cambio rápido de usuario está deshabilitado.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ no \_ Active \_ Console**</dt> <dt>0x80098038</dt> </dl>                             | No se puede abrir el grupo de sensores del sistema desde Terminal Server sesiones de cliente.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ Active 0x80098039 monitor de eventos**</dt> <dt></dt> </dl>                      | Ya hay un monitor de eventos activo asociado a la sesión especificada.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ tipo de propiedad no válido**</dt> <dt>0x8009803A</dt> </dl>                    | El valor especificado no es un tipo de propiedad válido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ identificador de propiedad no válido**</dt> <dt>0x8009803B</dt> </dl>                          | El valor especificado no es un identificador de propiedad válido.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E 0x8009803C de \_ \_ propiedad no admitida**</dt> <dt></dt> </dl>                        | La unidad biométrica no admite la propiedad especificada.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ E 0x8009803D de \_ \_ \_ error de integridad del adaptador**</dt> <dt></dt> </dl>        | El adaptador no superó su comprobación de integridad.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ más \_ datos**</dt> <dt>0x00090001</dt> </dl>                                                         | Se necesita otro ejemplo para la plantilla de inscripción actual.<br/>                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Err. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





