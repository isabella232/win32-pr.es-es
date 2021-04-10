---
description: Describe los códigos de error 500-999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Códigos de error del sistema (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275031"
---
# <a name="system-error-codes-500-999"></a>Códigos de error del sistema (500-999)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 500 a 999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR \_ al \_ cargar el perfil de usuario \_**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



No se puede cargar el perfil de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_desbordamiento aritmético de errores \_**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



El resultado aritmético superó 32 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**\_canalización de errores \_ conectada**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Hay un proceso en otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**canalización de errores en \_ \_ escucha**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



Esperando a que un proceso Abra el otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**\_detención del comprobador de errores \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



El comprobador de aplicaciones ha encontrado un error en el proceso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**error \_ ABIOS \_**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Error en el subsistema ABIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR \_ WX86 \_ ADVERTENCIA**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



Se produjo una advertencia en el subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Error \_ WX86 \_**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Error en el subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_no se \_ canceló el temporizador de errores \_**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



Se intentó cancelar o establecer un temporizador que tiene un APC asociado y el subproceso de asunto no es el subproceso que estableció originalmente el temporizador con una rutina APC asociada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR de \_ DESenredado**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Código de la excepción de desenredado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR en la \_ \_ pila incorrecta**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



Se encontró una pila no válida o no alineada durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR \_ de \_ desenredado no válido \_**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



Se encontró un destino de desenredado no válido durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR \_ de \_ atributos de puerto no válidos \_**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Atributos de objeto no válidos especificados para NtCreatePort o atributos de puerto no válidos especificados en NtConnectPort


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**mensaje de puerto de ERROR \_ \_ \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



La longitud del mensaje pasado a NtRequestPort o NtRequestWaitReplyPort era mayor que el mensaje máximo permitido por el puerto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR \_ de \_ cuota \_ inferior no válida**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Se intentó reducir un límite de cuota por debajo del uso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**el \_ dispositivo de error \_ ya está \_ conectado**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Se intentó asociar a un dispositivo que ya estaba conectado a otro dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR de alineación de la instrucción de ERROR \_ \_**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Se intentó ejecutar una instrucción en una dirección no alineada y el sistema host no admite referencias de instrucciones no alineadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR de \_ generación de perfiles \_ no \_ iniciada**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



No se ha iniciado la generación de perfiles.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ no se \_ ha detenido la generación de perfiles de errores**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



La generación de perfiles no se ha detenido.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR \_ no se pudo \_ \_ interpretar**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



La ACL pasada no contenía la información mínima necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR \_ al generar perfiles \_ en el \_ límite**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



El número de objetos de generación de perfiles activos es el máximo y no se pueden iniciar más.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR de espera de ERROR \_ \_**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Se utiliza para indicar que una operación no puede continuar sin bloqueos para e/s.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR no se pudo \_ \_ finalizar por \_ sí mismo**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Indica que un subproceso intentó finalizarse de forma predeterminada (denominada NtTerminateThread con **null**) y era el último subproceso del proceso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR \_ inesperado \_ mm \_ Create \_ Err**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro. En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**error \_ inesperado de \_ asignación de mm \_ \_**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro. En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR \_ inesperado \_ mm \_ Extend \_ Err**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro. En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR en la \_ tabla de funciones erróneas \_ \_**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



Se encontró una tabla de funciones incorrecta durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR \_ sin \_ traducción de GUID \_**
</dt> <dd> <dl> <dt>

560 (0x230)
</dt> <dt>



Indica que se ha intentado asignar la protección a un archivo o directorio del sistema de archivos y uno de los SID del descriptor de seguridad no se puede traducir en un GUID que el sistema de archivos pudiera almacenar. Esto hace que se produzca un error en el intento de protección, lo que puede provocar un error al intentar crear un archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR \_ de \_ tamaño de LDT no válido \_**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Indica que se ha intentado aumentar un LDT estableciendo su tamaño o que el tamaño no era un número par de selectores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR en el \_ \_ desplazamiento LDT no válido \_**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Indica que el valor inicial para la información de LDT no era un múltiplo entero del tamaño del selector.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR \_ de \_ \_ descriptor LDT no válido**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Indica que el usuario proporcionó un descriptor no válido al intentar configurar los descriptores de LDT.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR \_ demasiados \_ \_ subprocesos**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Indica que un proceso tiene demasiados subprocesos para realizar la acción solicitada. Por ejemplo, la asignación de un token principal solo se puede realizar cuando un proceso tiene cero o un subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_subproceso \_ de error no \_ en \_ proceso**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Se intentó operar en un subproceso en un proceso específico, pero el subproceso especificado no se encuentra en el proceso especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**cuota de archivo de ERROR \_ \_ \_ superada**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Se superó la cuota del archivo de paginación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**conflicto de servidor de inicio de sesión de ERROR \_ \_ \_**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



No se puede iniciar el servicio NetLogon porque otro servicio NetLogon que se ejecuta en el dominio está en conflicto con el rol especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronización de errores \_ \_ requerida**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



La base de datos SAM de un servidor de Windows está muy fuera de sincronización con la copia en el controlador de dominio. Se requiere una sincronización completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR \_ \_ al abrir net Open \_**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



Error de la API de NtCreateFile. Este error nunca debe devolverse a una aplicación, sino que es un marcador de posición para que el redirector de Windows LAN Manager lo use en sus rutinas de asignación de errores internas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR de \_ privilegio de e/s \_ \_**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Error de privilegio} No se pudieron cambiar los permisos de e/s para el proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**salida de control de errores \_ \_ C \_**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Cierre de la aplicación con CTRL + C} La aplicación terminó como resultado de CTRL + C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR: \_ falta \_ SYSTEMFILE**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{Falta el archivo del sistema} Falta el archivo de sistema requerido% HS o no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR de \_ excepción no controlada \_**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Error de aplicación} La excepción% s (0x% 08lX) se produjo en la aplicación en la ubicación 0x% 08lX.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR \_ de \_ inicialización de la aplicación \_**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Error de aplicación} La aplicación no pudo iniciarse correctamente (0x% LX). Haga clic en Aceptar para cerrar la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR \_ \_ al crear el archivo de paginación \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{No se puede crear el archivo de paginación} No se pudo crear el archivo de paginación% HS (% LX). El tamaño solicitado era% ld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR \_ de \_ valor hash de imagen no válido \_**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Windows no puede comprobar la firma digital de este archivo. Un cambio de hardware o software reciente podría haber instalado un archivo firmado incorrectamente o dañado, o que podría ser software malintencionado de un origen desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR \_ sin archivo de \_ paginación**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{No se especificó ningún archivo de paginación} No se especificó ningún archivo de paginación en la configuración del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR \_ de \_ contexto de punto flotante no válido \_**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



EXCEPCIONAL Una aplicación en modo real emitió una instrucción de punto flotante y el hardware de punto flotante no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**\_no hay \_ ningún \_ par de eventos de error**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Se ha realizado una operación de sincronización de un par de eventos mediante el objeto de par de eventos cliente/servidor específico del subproceso, pero no hay ningún objeto de par de eventos asociado al subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**error de configuración del dominio de ERROR del \_ \_ control \_ \_**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Un servidor de Windows tiene una configuración incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR \_ de \_ carácter no válido**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Se encontró un carácter no válido. Para un juego de caracteres de varios bytes, esto incluye un byte inicial sin un byte final subsiguiente. En el caso del juego de caracteres Unicode, se incluyen los caracteres 0xFFFF y 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**carácter no definido de ERROR \_ \_**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



El carácter Unicode no está definido en el juego de caracteres Unicode instalado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volumen de disquete de error \_**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



No se puede crear el archivo de paginación en un disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR \_ \_ de BIOS \_ al \_ conectar la \_ interrupción**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



El BIOS del sistema no pudo conectar una interrupción del sistema al dispositivo o al bus al que está conectado el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR de \_ controlador de copia de seguridad \_**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Esta operación solo se permite para el controlador de dominio principal del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_límite de mutaciones de error \_ \_ superado**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



Se intentó adquirir un mutante, de modo que se habría superado su recuento máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR \_ de \_ controlador de FS \_ requerido**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



Se ha tenido acceso a un volumen para el que se requiere un controlador del sistema de archivos que aún no se ha cargado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR: \_ no se puede \_ cargar el \_ archivo de registro \_**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Error del archivo de registro} El registro no puede cargar el subárbol (archivo):% HS o su registro o alternativo. Está dañado, no existe o no se puede escribir en él.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR \_ \_ al adjuntar error de depuración \_**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Error inesperado en [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Error inesperado al procesar una solicitud de API **DebugActiveProcess** . Puede elegir aceptar para finalizar el proceso o cancelar para omitir el error.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR en el \_ proceso del sistema \_ \_**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Error irrecuperable del sistema} El proceso del sistema% HS terminó inesperadamente con un estado de 0x% 08x (0x% 08x 0x% 08x). El sistema se ha cerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**\_no se \_ \_ aceptan datos de error**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Datos no aceptados} El cliente TDI no pudo controlar los datos recibidos durante una indicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**error \_ de \_ VDM \_ error**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



NTVDM ha detectado un error de hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_tiempo de \_ espera de cancelación del controlador de error \_**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Cancelar tiempo de espera} El controlador% HS no pudo completar una solicitud de e/s cancelada en el tiempo asignado.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR \_ de \_ coincidencia de mensaje de respuesta \_**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Error de coincidencia del mensaje de respuesta} Se intentó responder a un mensaje LPC, pero el subproceso especificado por el identificador de cliente en el mensaje no estaba esperando en el mensaje.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR al \_ perder los \_ datos de WRITEBEHIND \_**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS. Se han perdido los datos. Este error puede deberse a un error del hardware del equipo o de la conexión de red. Intente guardar este archivo en otra ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR de \_ parámetros de servidor de cliente \_ \_ \_ no válidos**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Los parámetros pasados al servidor en la ventana memoria compartida de cliente/servidor no eran válidos. Es posible que se hayan colocado demasiados datos en la ventana memoria compartida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR \_ no es un \_ \_ flujo reducido**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



La secuencia no es una secuencia pequeña.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR de \_ desbordamiento de pila de errores \_ \_**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



La solicitud debe controlarse mediante el código de desbordamiento de pila.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR \_ \_ al convertir a \_ grande**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Códigos de estado de OFS internos que indican cómo se controla una operación de asignación. Se reintentará después de que se mueva el onode contenedor o hasta que el flujo de la extensión se convierta en una secuencia grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR \_ detectado \_ fuera \_ de \_ ámbito**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



El intento de buscar el objeto encontró un objeto que coincide con el identificador en el volumen pero está fuera del ámbito del identificador usado para la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR al \_ asignar el \_ depósito**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



La matriz de depósitos debe crecer. Vuelva a intentar la transacción después de hacerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**\_desbordamiento de serialización de error \_**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



Se ha desbordado el búfer de serialización de usuario/kernel.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR \_ de \_ variante no válida**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



La estructura de variante proporcionada contiene datos no válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR \_ de \_ búfer de compresión incorrecto \_**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



El búfer especificado contiene datos con formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR de auditoría de errores \_ \_**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Error de auditoría} Error al tratar de generar una auditoría de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_no se \_ estableció la resolución del temporizador \_ \_**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



La resolución del temporizador no se estableció previamente en el proceso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR \_ : \_ información de inicio de sesión insuficiente \_**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



No hay suficiente información de cuenta para iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR de punto de entrada de \_ \_ dll incorrecto \_**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{Punto de entrada de DLL no válido} La biblioteca de vínculos dinámicos% HS no se ha escrito correctamente. El puntero de pila se ha dejado en un estado incoherente. El punto de entrada debe declararse como WINAPI o STDCALL. Seleccione Sí para no realizar la carga de la DLL. Seleccione NO para continuar con la ejecución. La selección de NO puede hacer que la aplicación NO funcione correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR de punto de entrada de \_ \_ servicio incorrecto \_**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Punto de entrada de devolución de llamada de servicio no válido} El servicio% HS no se ha escrito correctamente. El puntero de pila se ha dejado en un estado incoherente. El punto de entrada de devolución de llamada debe declararse como WINAPI o STDCALL. Si selecciona Aceptar, el servicio continuará la operación. Sin embargo, es posible que el proceso de servicio no funcione correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR \_ de \_ dirección IP \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Hay un conflicto de dirección IP con otro sistema de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR \_ de \_ dirección IP \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Hay un conflicto de dirección IP con otro sistema de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_límite de \_ cuota del registro de errores \_**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Espacio insuficiente en el registro} El sistema ha alcanzado el tamaño máximo permitido para la parte del sistema del registro. Se omitirán las solicitudes de almacenamiento adicionales.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR: \_ no hay ninguna \_ devolución de llamada \_ activa**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



No se puede ejecutar un servicio de sistema de devolución de devolución de llamada cuando no hay ninguna devolución de llamada activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR \_ pwd \_ demasiado \_ corto**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



La contraseña proporcionada es demasiado corta para cumplir con la Directiva de su cuenta de usuario. Elija una contraseña más larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR \_ pwd \_ demasiado \_ reciente**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



La Directiva de su cuenta de usuario no permite cambiar las contraseñas con demasiada frecuencia. Esto se hace para evitar que los usuarios cambien a una contraseña conocida, pero potencialmente detectada. Si cree que la contraseña se ha puesto en peligro, póngase en contacto con el administrador inmediatamente para tener una nueva asignada.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**conflicto de historial de ERROR \_ pwd \_ \_**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Ha intentado cambiar la contraseña por una que ha usado en el pasado. La Directiva de su cuenta de usuario no lo permite. Seleccione una contraseña que no haya usado previamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR de \_ compresión no admitida \_**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



El formato de compresión especificado no es compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR \_ de \_ Perfil de HW no válido \_**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



La configuración de Perfil de hardware especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR en la \_ \_ ruta de acceso del dispositivo PLUGPLAY no válida \_ \_**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



La ruta de acceso del dispositivo del registro de Plug and Play especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**lista de cuotas de ERROR \_ \_ \_ incoherente**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



La lista de cuotas especificada es incoherente internamente con su descriptor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**expiración de la evaluación de errores \_ \_**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Notificación de evaluación de Windows} El período de evaluación de esta instalación de Windows ha expirado. Este sistema se apagará en 1 hora. Para restaurar el acceso a esta instalación de Windows, actualice esta instalación mediante una distribución con licencia de este producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR \_ de \_ reubicación de dll no válida \_**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Reubicación de DLL del sistema no válida} La DLL del sistema% HS se reubicaba en la memoria. La aplicación no se ejecutará correctamente. La reubicación se produjo porque el archivo DLL% HS ocupaba un intervalo de direcciones reservado para los archivos DLL del sistema de Windows. Se debe poner en contacto con el proveedor que suministra el archivo DLL para obtener un nuevo archivo DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR \_ \_ \_ al cerrar la sesión de dll init \_**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Error de inicialización de DLL} No se pudo inicializar la aplicación porque la estación de ventana se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR al \_ validar la validación \_**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



El proceso de validación debe continuar con el paso siguiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR: \_ no hay \_ más \_ coincidencias**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



No hay más coincidencias para la enumeración de índice actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflicto de \_ lista de intervalos de errores \_**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



No se pudo agregar el intervalo a la lista de intervalos debido a un conflicto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR \_ de \_ coincidencia de SID de servidor \_**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



El proceso de servidor se está ejecutando con un SID diferente del que requiere el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR no se \_ \_ permite habilitar \_ solo denegar \_**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



No se puede habilitar un grupo marcado como usar para denegar únicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR \_ float \_ varios \_ errores**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



EXCEPCIONAL Varios errores de punto flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR \_ float \_ varias \_ capturas**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



EXCEPCIONAL Varias capturas de punto flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR \_ NOinterface**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



No se admite la interfaz solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR \_ \_ al \_ suspender el controlador**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Error de espera del sistema} El controlador% HS no admite el modo de espera. La actualización de este controlador puede permitir que el sistema entre en modo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR \_ de \_ archivo de sistema dañado \_**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



El archivo de sistema %1 se ha dañado y se ha reemplazado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**compromiso de ERROR \_ \_ mínimo**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Memoria virtual mínima demasiado baja} El sistema tiene poca memoria virtual. Windows está aumentando el tamaño del archivo de paginación de la memoria virtual. Durante este proceso, es posible que se denieguen las solicitudes de memoria para algunas aplicaciones. Para obtener más información, vea la ayuda de.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR \_ de \_ enumeración de reinicio PNP \_**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Se quitó un dispositivo, por lo que la enumeración debe reiniciarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**\_ \_ firma incorrecta de imagen de sistema \_ \_**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Error irrecuperable del sistema} La imagen del sistema% s no está firmada correctamente. El archivo se ha reemplazado por el archivo firmado. El sistema se ha cerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR \_ se \_ requiere reinicio de PNP \_**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



El dispositivo no se iniciará sin necesidad de reiniciar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR \_ de \_ energía insuficiente**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



No hay suficiente capacidad para completar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR \_ de \_ infracción de varios errores \_**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



ERROR \_ de \_ infracción de varios errores \_


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR \_ de \_ apagado del sistema**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



El sistema está en proceso de cierre.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_no se \_ ha \_ establecido el puerto de error**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Se ha intentado quitar un proceso depurado, pero aún no se ha asociado un puerto al proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR \_ de \_ comprobación de versión de DS \_ \_**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Esta versión de Windows no es compatible con la versión de comportamiento del bosque de directorio, el dominio o el controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_ \_ no \_ se encontró el intervalo de errores**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



No se pudo encontrar el intervalo especificado en la lista de intervalos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR \_ de \_ \_ controlador de modo seguro \_**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



No se cargó el controlador porque el sistema se está iniciando en modo seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR en la \_ \_ entrada del controlador \_**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



No se cargó el controlador porque no se pudo realizar la llamada de inicialización.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**error \_ de \_ enumeración de dispositivos error \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"% HS" encontró un error al aplicar la energía o leer la configuración del dispositivo. Esto puede deberse a un error del hardware o a una mala conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_no se \_ \_ ha \_ resuelto el punto de montaje de error**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



No se pudo realizar la operación de creación porque el nombre contenía al menos un punto de montaje que se resuelve en un volumen al que no está asociado el objeto de dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR \_ de \_ \_ parámetro de objeto de dispositivo no válido \_**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



El parámetro de objeto de dispositivo no es un objeto de dispositivo válido o no está asociado al volumen especificado por el nombre de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR \_ MCA \_**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Se ha producido un error de comprobación del equipo. Compruebe el registro de eventos del sistema para obtener información adicional.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**error \_ de \_ base de datos de controlador de error \_**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Error \[ %2 al \] procesar la base de datos del controlador.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**\_subárbol del sistema de errores \_ \_ demasiado \_ grande**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



El tamaño de Hive del sistema ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR de la \_ \_ \_ \_ descarga anterior del controlador de errores**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



No se pudo cargar el controlador porque una versión anterior del controlador todavía está en la memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR de \_ VOLSNAP \_ preparar \_ hibernación**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Servicio de instantáneas de volumen} Espere mientras el Servicio de instantáneas de volumen prepara el volumen% HS para la hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR de \_ hibernación de errores \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



No se pudo hibernar el sistema (el código de error es% HS). La hibernación se deshabilitará hasta que se reinicie el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR \_ pwd \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



La contraseña proporcionada es demasiado larga para cumplir con la Directiva de su cuenta de usuario. Elija una contraseña más corta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_ \_ limitación del sistema de archivos de error \_**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



no se pudo completar la operación solicitada por una limitación del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**error de aserción de ERROR \_ \_**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Error de aserción.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**error \_ ACPI de error \_**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



Error en el subsistema ACPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR \_ de \_ aserción wow**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Error de aserción WOW.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR en la \_ \_ \_ \_ tabla MPS errónea de PNP**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



Falta un dispositivo en la tabla MPS del BIOS del sistema. Este dispositivo no se usará. Póngase en contacto con el proveedor del sistema para actualizar el BIOS del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR \_ de \_ traducción de PNP \_**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Un traductor no pudo traducir los recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR \_ de \_ conversión de IRQ PNP \_ \_**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Un traductor de IRQ no pudo traducir los recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR \_ de \_ identificador no válido de PNP \_**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



El controlador %2 devolvió un ID. no válido para un dispositivo secundario (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR de \_ reactivación \_ del sistema del \_ depurador**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Se activó el depurador de kernel} una interrupción activó el depurador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_identificadores de error \_ cerrados**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Identificadores cerrados} Los identificadores de los objetos se han cerrado automáticamente como resultado de la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_información extraña de error \_**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Demasiada información} La lista de control de acceso (ACL) especificada contiene más información de la esperada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR \_ RXACT la \_ confirmación \_ necesaria**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Este estado de nivel de advertencia indica que el estado de la transacción ya existe para el subárbol del registro, pero que se anuló previamente una confirmación de transacción. La confirmación no se ha completado, pero no se ha revertido (por lo que se puede seguir confirmando si se desea).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_comprobación de medios de error \_**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Contenido multimedia cambiado} Es posible que el medio haya cambiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**sustitución de GUID de ERROR \_ \_ \_ realizada**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Sustitución de GUID} Durante la traducción de un identificador global (GUID) a un identificador de seguridad de Windows (SID), no se encontró ningún prefijo GUID definido por el administrador. Se usó un prefijo sustitutivo, lo que no afectará A la seguridad del sistema. Sin embargo, esto puede proporcionar un acceso más restrictivo que el previsto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR \_ detenido \_ en \_ SYMLINK**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



La operación de creación se detuvo después de llegar a un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



Se ha ejecutado un salto largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR \_ PLUGPLAY \_ consulta \_ vetada**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



La operación de consulta de Plug and Play no se realizó correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR al \_ DESenredar la \_ consolidación**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



Se ha ejecutado una consolidación de fotogramas.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR \_ de \_ subárbol del registro \_ recuperado**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{Subárbol del registro recuperado} El subárbol del registro (archivo):% HS estaba dañado y se ha recuperado. Algunos datos podrían haberse perdido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**el \_ archivo dll de error \_ puede no \_ ser \_ seguro**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



La aplicación está intentando ejecutar código ejecutable desde el módulo% HS. Esto puede ser inseguro. Existe una alternativa,% HS, disponible. ¿La aplicación debe usar el módulo seguro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**\_es posible que la dll de error no \_ \_ sea \_ compatible**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



La aplicación está cargando código ejecutable del módulo% HS. Esto es seguro, pero puede que no sea compatible con las versiones anteriores del sistema operativo. Existe una alternativa,% HS, disponible. ¿La aplicación debe usar el módulo seguro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR \_ dbg \_ \_ no se ha controlado la excepción \_**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



El depurador no controló la excepción.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR \_ dbg: \_ respuesta \_ posterior**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



El depurador responderá más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR \_ dbg \_ no se puede \_ \_ proporcionar el \_ identificador**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



El depurador no puede proporcionar el identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR \_ dbg: \_ finalizar \_ subproceso**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



El depurador finalizó el subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR \_ dbg: \_ finalizar \_ proceso**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



El depurador finalizó el proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR \_ dbg ( \_ control) \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



El depurador tiene el control C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR \_ dbg \_ PRINTEXCEPTION \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



Excepción impresa del depurador en el control C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR \_ dbg \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



El depurador recibió una excepción RIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR \_ dbg \_ ( \_ interrupción de control)**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



El depurador recibió un salto de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR \_ dbg \_ excepción del comando \_**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Excepción de comunicación de comandos del depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_el nombre del objeto de error \_ \_ existe**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Objeto existente} Se intentó crear un objeto y el nombre del objeto ya existía.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**el \_ subproceso de error \_ se \_ suspendió**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Subproceso suspendido} Se ha producido una terminación del subproceso mientras se suspendió el subproceso. El subproceso se reanudó y la terminación continuó.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_imagen \_ de error no \_ en \_ base**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Imagen reubicada} No se pudo asignar un archivo de imagen en la dirección especificada en el archivo de imagen. Las correcciones locales deben realizarse en esta imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR de \_ RXACT de \_ estado \_ creado**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Este estado de nivel informativo indica que el estado de una transacción de subárbol del registro especificada no existía todavía y se tenía que crear.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notificación de segmento de error \_**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Carga de segmento} Una máquina DOS virtual (VDM) está cargando, descargando o moviendo una imagen de segmento de programa de MS-DOS o Win16. Se produce una excepción para que un depurador pueda cargar, descargar o realizar un seguimiento de símbolos y puntos de interrupción dentro de estos segmentos de 16 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR \_ de \_ directorio actual no válido \_**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Directorio actual no válido} El proceso no puede cambiar al directorio actual de inicio% HS. Seleccione Aceptar para establecer el directorio actual en% HS o seleccione Cancelar para salir.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR \_ ft \_ leer \_ recuperación \_ de \_ copia de seguridad**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Lectura redundante} Para satisfacer una solicitud de lectura, el sistema de archivos tolerante a errores de NT leyó correctamente los datos solicitados de una copia redundante. Esto se ha hecho porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área de error del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR en la recuperación de escritura de \_ ft \_ \_**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Escritura redundante} Para satisfacer una solicitud de escritura, el sistema de archivos tolerante a errores de NT escribió correctamente una copia redundante de la información. Esto se ha hecho porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área de error del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de tipo de máquina de imagen \_**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Error de coincidencia de tipo de máquina} El archivo de imagen% HS es válido, pero es para un tipo de máquina distinto del equipo actual. Seleccione Aceptar para continuar o cancelar para que se produzca un error en la carga del archivo DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR de \_ recepción \_ parcial**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Datos parciales recibidos} El transporte de red devolvió datos parciales a su cliente. Los datos restantes se enviarán más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR de \_ recepción \_ acelerada**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Datos expedidos recibidos} El transporte de red devolvió datos a su cliente que se marcó como expedido por el sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR de \_ recepción \_ parcial \_ rápida**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Se recibieron datos inmediatos parciales} El transporte de red devolvió datos parciales a su cliente y estos datos se marcaron como expedidos por el sistema remoto. Los datos restantes se enviarán más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento de ERROR \_ \_ finalizado**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Evento TDI terminado} La indicación TDI se ha completado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento de ERROR \_ \_ pendiente**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Evento TDI pendiente} La indicación TDI ha entrado en el estado pendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR al \_ comprobar el \_ sistema de archivos \_**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Comprobando el sistema de archivos en% wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR \_ irrecuperable de salida de la \_ aplicación \_**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Final de aplicación irrecuperable}% HS.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_identificador PREdefinido de error \_**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



Un identificador predefinido hace referencia a la clave del registro especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR \_ \_ desbloqueado**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Página desbloqueada} La protección de página de una página bloqueada se cambió a "sin acceso" y la página se desbloqueó de la memoria y del proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notificación del servicio de error \_**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Page Locked} Una de las páginas que se van a bloquear ya estaba bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_error de registro de errores \_ \_**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Menú emergente de aplicación: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR \_ ya \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



ERROR \_ ya \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR \_ de \_ falta de \_ coincidencia de tipo de máquina de \_ imagen \_**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Error de coincidencia de tipo de máquina} El archivo de imagen% HS es válido, pero es para un tipo de máquina distinto del equipo actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR: no se ha \_ \_ realizado ningún resultado \_**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



Se ha realizado una ejecución de Yield y no hay ningún subproceso disponible para ejecutarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**se \_ ha \_ omitido el reanudación del temporizador \_**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



Se omitió la marca reanudable de una API de temporizador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**Arbitraje de ERROR \_ \_ no controlado**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



El árbitro ha diferido el arbitraje de estos recursos a su elemento primario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR \_ CardBus \_ no \_ compatible**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



No se puede iniciar el dispositivo CardBus insertado debido a un error de configuración en "% HS".


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR \_ de \_ incoherencia del procesador MP \_**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



Las CPU de este sistema multiprocesador no tienen el mismo nivel de revisión. Para usar todos los procesadores, el sistema operativo se restringe a las características del procesador menos capaz en el sistema. En caso de que se produzcan problemas con este sistema, póngase en contacto con el fabricante de la CPU para ver si se admite esta combinación de procesadores.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR \_ hibernado**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



El sistema se puso en hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR al \_ reanudar la \_ hibernación**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



El sistema se reanudó de la hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE de ERROR \_ \_ actualizado**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



Windows ha detectado que el firmware del sistema (BIOS) se actualizó en la \[ fecha de firmware anterior = %2, fecha de firmware actual %3 \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERRORES \_ en \_ \_ las páginas bloqueadas de los controladores de error \_**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Un controlador de dispositivo pierde las páginas de e/s bloqueadas que causan la degradación del sistema. El sistema ha habilitado automáticamente el código de seguimiento para intentar detectar la causa.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR de \_ Wake \_ System**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



El sistema tiene awoken.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR de \_ espera \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



ERROR de \_ espera \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**Espera de ERROR \_ \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



Espera de ERROR \_ \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR de \_ espera \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



ERROR de \_ espera \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR de \_ espera \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



ERROR de \_ espera \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR \_ abandonada \_ Wait \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



ERROR \_ abandonada \_ Wait \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR \_ abandonada \_ Wait \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



ERROR \_ abandonada \_ Wait \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR de \_ usuario \_ APC**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



ERROR de \_ usuario \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR \_ de \_ APC kernel**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



ERROR \_ de \_ APC kernel


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR de \_ alerta**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



ERROR de \_ alerta


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**elevación de errores \_ \_ necesaria**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



La operación solicitada requiere elevación.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR al volver a \_ analizar**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



El administrador de objetos debe realizar un reanálisis, ya que el nombre del archivo dio como resultado un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**\_ \_ interrupción del error \_ de bloqueo oportunista en \_ curso**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Se completó una operación de apertura/creación mientras se está realizando una interrupción de bloqueo oportunista.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**volumen de ERROR \_ \_ montado**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Un sistema de archivos ha montado un nuevo volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR \_ RXACT \_ confirmado**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Este estado de nivel de éxito indica que el estado de la transacción ya existe para el subárbol del registro, pero que se anuló previamente una confirmación de transacción. La confirmación se ha completado ahora.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR de \_ notificación de \_ limpieza**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Esto indica que se ha completado una solicitud NOTIFY Change debido al cierre del identificador que realizó la solicitud NOTIFY Change.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR \_ de \_ conexión de transporte principal \_ \_**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Error de conexión en el transporte principal} Se intentó conectar con el servidor remoto% HS en el transporte principal, pero se produjo un error en la conexión. El equipo pudo conectarse en un transporte secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transición de \_ errores de página de error \_**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



El error de página era un error de transición.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**solicitud de ERROR de \_ página \_ \_ \_ cero**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



El error de página era un error de petición cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR \_ \_ en la \_ copia \_ de errores de página al \_ escribir**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



El error de página era un error de petición cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Página de ERROR: \_ \_ protección de errores \_ \_**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



El error de página era un error de petición cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_archivo de \_ \_ paginación de errores de página \_**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



El error de página se ha satisfecho mediante la lectura de un dispositivo de almacenamiento secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_Página caché de errores \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



La página en caché se bloqueó durante la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**volcado de errores \_ \_**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



El volcado de memoria existe en el archivo de paginación.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**búfer de ERROR: \_ \_ todos \_ ceros**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



El búfer especificado contiene ceros.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR al volver a \_ analizar el \_ objeto**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



El administrador de objetos debe realizar un reanálisis, ya que el nombre del archivo dio como resultado un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**requisitos de recursos de ERROR \_ \_ \_ modificados**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



El dispositivo ha finalizado correctamente una detención de consulta y sus requisitos de recursos han cambiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**traducción de errores \_ \_ completada**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



El traductor ha traducido estos recursos al espacio global y no se deben realizar más traducciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**no \_ \_ se pudo \_ Finalizar nada**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Un proceso terminado no tiene ningún subproceso para finalizar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**el \_ proceso \_ de error no está \_ en el \_ trabajo**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



El proceso especificado no forma parte de un trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR \_ \_ de proceso en el \_ trabajo**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



El proceso especificado forma parte de un trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR \_ VOLSNAP \_ \_ preparado para hibernar**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Servicio de instantáneas de volumen} El sistema ya está listo para la hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR \_ FSFILTER \_ operación \_ completada \_ correctamente**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Un sistema de archivos o un controlador de filtro del sistema de archivos ha completado correctamente una operación de FsFilter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**Vector de interrupción de ERROR \_ \_ \_ ya \_ conectado**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



El vector de interrupción especificado ya estaba conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interrupción de ERROR \_ \_ todavía \_ conectada**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



El vector de interrupción especificado todavía está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR \_ \_ de espera de \_ bloqueo oportunista**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Una operación está bloqueada a la espera de un bloqueo oportunista.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR \_ dbg \_ excepción \_ controlada**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Excepción controlada por el depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR \_ dbg \_ continue**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



El depurador continuó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_pila pop de devolución de llamada de error \_ \_**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Se produjo una excepción en una devolución de llamada del modo de usuario y debe quitarse el marco de devolución de llamada del kernel.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**compresión de ERROR \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



La compresión está deshabilitada para este volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



El proveedor de datos no puede recuperarse hacia atrás a través de un conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR \_ CANTSCROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



El proveedor de datos no se puede desplazar hacia atrás a través de un conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR \_ ROWSNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



El proveedor de datos requiere que se liberen los datos capturados anteriormente antes de solicitar más datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR \_ de \_ marcas de descriptor de acceso incorrecto \_**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



El proveedor de datos no pudo interpretar las marcas establecidas para un enlace de columna en un descriptor de acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_errores \_ encontrados**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Se produjeron uno o más errores al procesar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR \_ no \_ compatible**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



La implementación no es capaz de realizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_solicitud \_ de error fuera \_ de \_ secuencia**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



El cliente de un componente solicitó una operación que no es válida dado el estado de la instancia del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**error de \_ análisis de versión de error \_ \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



No se pudo analizar un número de versión.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR \_ BADSTARTPOSITION**
</dt> <dd> <dl> <dt>

778 (0x30A)
</dt> <dt>



La posición inicial del iterador no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware de memoria de error \_**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



El hardware ha detectado un error de memoria incorregible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR \_ al \_ reparar el disco \_ deshabilitado**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



La operación que se ha intentado requiere que se habilite la recuperación automática.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR \_ \_ de recurso insuficiente \_ para \_ \_ \_ \_ el tamaño de sección compartida especificado**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



El montón de escritorio encontró un error al asignar memoria de sesión. Hay más información en el registro de eventos del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**transición de sistema de errores \_ \_ POWERSTATE \_**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



El estado de la alimentación del sistema está pasando de %2 a %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**\_ \_ \_ transición compleja del sistema de errores \_**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



El estado de la alimentación del sistema está pasando de %2 a %3, pero puede escribir %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR \_ MCA \_ excepción**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Un subproceso se envía con excepción de MCA debido a la MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR \_ \_ de auditoría \_ de acceso por \_ Directiva**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



El acceso a %1 está supervisado por la regla de directiva %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR \_ \_ de acceso deshabilitado \_ sin \_ \_ interfaz de usuario más segura \_ por \_ Directiva**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



La regla de directiva %2 ha restringido el acceso a %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR al \_ abandonar \_ hibernación**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Se ha invalidado un archivo de hibernación válido y debe abandonarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR \_ perdido \_ WRITEBEHIND de \_ red de datos \_ \_ desconectado**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos. Este error puede deberse a problemas de conectividad de red. Intente guardar este archivo en otra ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**error \_ perdido \_ WRITEBEHIND \_ de \_ servidor de red de datos \_ \_**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos. Este error fue devuelto por el servidor en el que existe el archivo. Intente guardar este archivo en otra ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**error \_ perdido error de \_ \_ \_ disco local de datos WRITEBEHIND \_ \_**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos. Este error puede deberse a que se ha quitado el dispositivo o a que el medio está protegido contra escritura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR en la \_ \_ tabla MCFG errónea \_**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Los recursos necesarios para este dispositivo entran en conflicto con la tabla MCFG.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR \_ al \_ reparar el disco \_ Redirigido**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



No se pudo reparar el volumen mientras está en línea. Programe la desconexión del volumen para que se pueda reparar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR \_ de \_ reparación de disco \_ incorrecta**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



La reparación del volumen no se ha realizado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR \_ de \_ Registro \_ dañado**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



Uno de los registros de daños del volumen está lleno. No se registrarán más daños que puedan detectarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR \_ de \_ Registro \_ dañado dañado**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



Uno de los registros de daños del volumen está dañado internamente y debe volver a crearse. El volumen puede contener daños no detectados y se debe analizar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR \_ de \_ registro dañado \_ no disponible**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



Uno de los registros de daños del volumen no está disponible para su funcionamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR \_ de \_ registro dañado \_ eliminado \_ completo**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



Se eliminó uno de los registros de daños del volumen al seguir teniendo registros dañados en ellos. El volumen contiene daños detectados y debe analizarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR \_ de \_ Registro \_ dañado**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



CHKDSK borró uno de los registros de daños del volumen y ya no contiene daños reales.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR \_ de \_ nombre huérfano \_ agotado**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



Existen archivos huérfanos en el volumen, pero no se pudieron recuperar porque no se pueden crear más nombres nuevos en el directorio de recuperación. Los archivos deben moverse desde el directorio de recuperación.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR \_ de bloqueo oportunista \_ cambiado \_ a \_ nuevo \_ identificador**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



El bloqueo oportunista asociado a este identificador está asociado ahora a un identificador diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR \_ no se puede \_ conceder el \_ \_ bloqueo oportunista solicitado**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



No se puede conceder un bloqueo oportunista del nivel solicitado. Puede haber disponible un bloqueo oportunista de un nivel inferior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR \_ no se puede \_ interrumpir el \_ bloqueo oportunista**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



La operación no se completó correctamente porque haría que se interrumpiera un bloqueo oportunista. El autor de la llamada ha solicitado que bloqueos oportunistas existente no se interrumpa.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**\_identificador de bloqueo oportunista de error \_ \_ cerrado**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



Se ha cerrado el identificador con el que se asoció este bloqueo oportunista. El bloqueo oportunista se ha interrumpido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR: \_ no hay ninguna \_ \_ condición ACE**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



La entrada de control de acceso (ACE) especificada no contiene ninguna condición.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR de la \_ \_ condición ACE no válida \_**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



La entrada de control de acceso (ACE) especificada contiene una condición no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**identificador de archivo de ERROR \_ \_ \_ revocado**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



Se ha revocado el acceso al identificador de archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_imagen \_ de error en \_ \_ base diferente**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Un archivo de imagen se asignó a una dirección diferente a la especificada en el archivo de imagen, pero las correcciones se seguirán realizando automáticamente en la imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR \_ EA \_ acceso \_ denegado**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



Se denegó el acceso al atributo extendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operación de ERROR \_ \_ anulada**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**\_e/s de error \_ incompleta**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



El evento de e/s superpuesta no se encuentra en un estado señalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_e/s de errores \_ pendientes**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



La operación de e/s superpuesta está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR \_ NOaccess**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Acceso no válido a la ubicación de memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Error al realizar la operación de INPAGE.


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

 

 
