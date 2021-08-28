---
title: Códigos de error de cliente (Winbio \_ err.h)
description: Códigos de error definidos en el archivo de encabezado \_ err.h de Winbio.
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
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993845"
---
# <a name="client-error-codes"></a>Códigos de error de cliente

Los códigos de error siguientes se definen en el archivo de encabezado \_ err.h de Winbio.



| Constante o valor                                                                                                                                                                                                                                                                                         | Descripción                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ FACTOR \_ 0X80098001**</dt> <dt></dt> </dl>                              | No se admite el factor biométrico especificado.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E \_ Unidad \_ no**</dt> válida <dt>0x80098002</dt> </dl>                                                | El número de identificador de unidad no corresponde a un dispositivo biométrico válido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ IDENTIFICADOR \_ DESCONOCIDO**</dt> <dt>0x80098003</dt> </dl>                                                      | La muestra biométrica no coincide con ninguna identidad conocida.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ CANCELED**</dt> <dt>0x80098004</dt> </dl>                                                             | La operación biométrica se canceló antes de que se pudiera completar.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ NO \_ MATCH**</dt> <dt>0x80098005</dt> </dl>                                                            | La muestra biométrica no coincide con la identidad o el subfactor especificados.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E \_ CAPTURE \_ ABORTED**</dt> <dt>0x80098006</dt> </dl>                                       | No se pudo capturar una muestra biométrica porque se anuló la operación de captura.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ E \_ INSCRIPCIÓN EN CURSO \_ \_ 0X80098007**</dt> <dt></dt> </dl>                 | No se pudo iniciar una transacción de inscripción porque ya hay otra inscripción en curso.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ BAD \_ CAPTURE**</dt> <dt>0x80098008</dt> </dl>                                                   | El ejemplo capturado no se puede usar para realizar más operaciones biométricas.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ CÓDIGO DE CONTROL \_ \_ NO**</dt> <dt>VÁLIDO 0x80098009</dt> </dl>                       | La unidad biométrica no admite el código de control de unidad especificado.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ E \_ \_ RECOPILACIÓN DE \_ DATOS EN CURSO \_ 0X8009800B**</dt> <dt></dt> </dl> | Ya hay una operación de recopilación de datos pendiente en curso.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ FORMATO DE DATOS \_ \_ NO**</dt> <dt>0X8009800C</dt> </dl>              | El controlador del sensor biométrico no admite el formato de datos solicitado.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ TIPOS DE DATOS \_ NO \_**</dt> <dt>ADMITIDOs 0x8009800D</dt> </dl>                    | El controlador del sensor biométrico no admite el tipo de datos solicitado.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ UNSUPPORTED \_ PURPOSE**</dt> <dt>0x8009800E</dt> </dl>                           | El controlador del sensor biométrico no admite el propósito de datos solicitado.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ ESTADO DE DISPOSITIVO \_ \_ NO**</dt> <dt>VÁLIDO 0x8009800F</dt> </dl>                       | La unidad biométrica no está en el estado adecuado para realizar la operación especificada.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ E \_ DEVICE \_ BUSY**</dt> <dt>0x80098010</dt> </dl>                                                   | No se pudo realizar la operación porque el dispositivo del sensor estaba ocupado.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ CREATE**</dt> <dt>0x80098011</dt> </dl>                       | El adaptador de almacenamiento no pudo crear una nueva base de datos.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ OPEN**</dt> <dt>0x80098012</dt> </dl>                             | El adaptador de almacenamiento no pudo abrir una base de datos existente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ CLOSE**</dt> <dt>0x80098013</dt> </dl>                          | El adaptador de almacenamiento no pudo cerrar una base de datos.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT ERASE \_ 0x80098014**</dt> <dt></dt> </dl>                          | El adaptador de almacenamiento no pudo borrar una base de datos.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ FIND**</dt> <dt>0x80098015</dt> </dl>                             | El adaptador de almacenamiento no pudo encontrar una base de datos.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ E \_ DATABASE YA EXISTE \_ \_ 0x80098016**</dt> <dt></dt> </dl>              | El adaptador de almacenamiento no pudo crear una base de datos porque la base de datos especificada ya existe.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ FULL**</dt> <dt>0x80098018</dt> </dl>                                             | El adaptador de almacenamiento no pudo agregar un registro a la base de datos porque la base de datos está llena.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ LOCKED**</dt> <dt>0x80098019</dt> </dl>                                       | La base de datos está bloqueada y su contenido es inaccesible.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CORRUPTED**</dt> <dt>0x8009801A</dt> </dl>                              | El contenido de la base de datos se ha dañado y no es accesible.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO SE HA REGISTRADO \_ \_ \_ 0X8009801B**</dt> <dt></dt> </dl>             | No se eliminó ningún registro porque la identidad y el subfactor especificados no están presentes en la base de datos.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ DUPLICATE \_ ENROLLMENT**</dt> <dt>0x8009801C</dt> </dl>                        | La identidad y el subfactor especificados ya están inscritos en la base de datos.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE READ ERROR \_ \_ 0x8009801D**</dt> <dt></dt> </dl>                          | Error al intentar leer de la base de datos.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE WRITE ERROR \_ \_ 0x8009801E**</dt> <dt></dt> </dl>                       | Se produjo un error al intentar escribir en la base de datos.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ NO \_ RESULTS**</dt> <dt>0x8009801F</dt> </dl>                          | No hay registros en la base de datos que coincidan con la consulta.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO MORE \_ \_ \_ RECORDS**</dt> <dt>0x80098020</dt> </dl>          | Se han recuperado todos los registros de la consulta de base de datos más reciente.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Una operación de base de datos encontró inesperadamente el final del archivo.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ E \_ DATABASE BAD INDEX VECTOR \_ \_ \_ 0x80098022**</dt> <dt></dt> </dl>       | Error en una operación de base de datos debido a un vector de índice con formato correcto.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ error \_ de BSP**</dt> <dt>0x80098024</dt> </dl>                                             | La unidad biométrica no pertenece al proveedor de servicios especificado.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ UN GRUPO DE \_ \_ SENSORES**</dt> <dt>INCORRECTO 0x80098025</dt> </dl>                    | La unidad biométrica no pertenece al grupo de sensores especificado.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ NO CAPTURE DATA \_ \_ 0x80098026**</dt> <dt></dt> </dl>                                      | El búfer de captura del adaptador del sensor está vacío.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ MODO DE SENSOR \_ \_ NO**</dt> <dt>VÁLIDO 0x80098027</dt> </dl>                          | El adaptador del sensor no admite el modo de sensor especificado en la configuración.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ LOCK \_ VIOLATION**</dt> <dt>0x8009802A</dt> </dl>                                          | La operación solicitada no se puede realizar debido a un conflicto de bloqueo.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ DUPLICATE \_ TEMPLATE**</dt> <dt>0x8009802B</dt> </dl>                              | Los datos de una plantilla biométrica coinciden con los de otra plantilla que ya está en la base de datos.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ \_ Operación no**</dt> <dt>válida 0x8009802C</dt> </dl>                                 | La operación solicitada no es válida para el estado actual de la sesión o la unidad biométrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ SESSION \_ BUSY**</dt> <dt>0x8009802D</dt> </dl>                                                | La sesión no puede iniciar una nueva operación porque ya hay otra operación en curso.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ DISABLED**</dt> <dt>0x80098030</dt> </dl>                             | La configuración de la directiva del sistema ha deshabilitado el proveedor de credenciales biométricas.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ NO \_ CREDENTIAL**</dt> <dt>0x80098031</dt> </dl>             | No se encontró la credencial solicitada.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ DISABLED**</dt> <dt>0x80098032</dt> </dl>                                                             | La configuración de directivas del sistema ha deshabilitado el servicio biométrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ E \_ ERROR \_ DE CONFIGURACIÓN**</dt> <dt>0X80098033</dt> </dl>                     | No se pudo configurar la unidad biométrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ E \_ SENSOR \_ NO DISPONIBLE**</dt> <dt>0x80098034</dt> </dl>                              | No se puede crear un grupo privado porque una o varias unidades biométricas no están disponibles.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ ENABLED**</dt> <dt>0x80098035</dt> </dl>                                                   | Se requiere una secuencia de atención segura (CTRL-ALT-DELETE) para el inicio de sesión.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ E \_ ERROR \_ DEL DISPOSITIVO**</dt> <dt>0x80098036</dt> </dl>                                          | Error en un sensor biométrico.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E \_ FAST CAMBIO DE USUARIO DESHABILITADO \_ \_ \_ 0X80098037**</dt> <dt></dt> </dl>       | >el cambio rápido de usuario está deshabilitado.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ NO ESTÁ ACTIVA LA \_ \_ CONSOLA**</dt> <dt>0x80098038</dt> </dl>                             | El grupo de sensores del sistema no se puede abrir desde sesiones de cliente de Terminal Server.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ EVENT \_ MONITOR \_ ACTIVE**</dt> <dt>0x80098039</dt> </dl>                      | Ya hay un monitor de eventos activo asociado a la sesión especificada.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ TIPO DE PROPIEDAD \_ \_ NO**</dt> <dt>VÁLIDO 0x8009803A</dt> </dl>                    | El valor especificado no es un tipo de propiedad válido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ IDENTIFICADOR DE PROPIEDAD \_ \_ NO**</dt> <dt>VÁLIDO 0x8009803B</dt> </dl>                          | El valor especificado no es un identificador de propiedad válido.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E \_ UNSUPPORTED \_ PROPERTY**</dt> <dt>0x8009803C</dt> </dl>                        | La unidad biométrica no admite la propiedad especificada.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ ERROR DE INTEGRIDAD DEL ADAPTADOR \_ \_ \_ 0X8009803D**</dt> <dt></dt> </dl>        | El adaptador no pasó su comprobación de integridad.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> <dt>0x00090001</dt> </dl>                                                         | Se necesita otro ejemplo para la plantilla de inscripción actual.<br/>                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winbio \_ err.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





