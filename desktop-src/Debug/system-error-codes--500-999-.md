---
description: Describe los códigos de error 500-999 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Códigos de error del sistema (500-999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 9430f77c53be29ae0f8b1b4037b3c963b5ac69da446f4755fb19dc40501c69df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539205"
---
# <a name="system-error-codes-500-999"></a>Códigos de error del sistema (500-999)

> [!NOTE]
> Esta información está pensada para desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema (errores 500 a 999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR \_ DE CARGA DE PERFIL DE \_ \_ USUARIO**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



No se puede cargar el perfil de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**DESBORDAMIENTO \_ \_ ARITMÉTICO DE ERROR**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



El resultado aritmético superó los 32 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**CANALIZACIÓN \_ DE ERROR \_ CONECTADA**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Hay un proceso en otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ESCUCHA DE \_ CANALIZACIÓN \_ DE ERRORES**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



Esperando a que un proceso abra el otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR \_ VERIFIER \_ STOP**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



El comprobador de aplicaciones ha encontrado un error en el proceso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR \_ ABIOS \_ ERROR**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Error en el subsistema ABIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR \_ WX86 \_ WARNING**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



Se produjo una advertencia en el subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR \_ WX86 \_ ERROR**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Error en el subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**TEMPORIZADOR \_ DE ERROR NO \_ \_ CANCELADO**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



Se intentó cancelar o establecer un temporizador que tiene un APC asociado y el subproceso del sujeto no es el subproceso que estableció originalmente el temporizador con una rutina de APC asociada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**\_DESENREDO DE ERRORES**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Código de excepción de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**PILA \_ DE ERROR NO ESTÁ \_ BIEN**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



Se encontró una pila no válida o no alineada durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR \_ DESTINO DE \_ DESENREDO \_ NO VÁLIDO**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



Se encontró un destino de desenredo no válido durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR \_ ATRIBUTOS DE PUERTO NO \_ \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Atributos de objeto no válidos especificados en NtCreatePort o atributos de puerto no válidos especificados en NtConnectPort


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**MENSAJE \_ DE PUERTO DE ERROR DEMASIADO \_ \_ \_ LARGO**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



La longitud del mensaje pasado a NtRequestPort o NtRequestWaitReplyPort era mayor que el mensaje máximo permitido por el puerto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR \_ CUOTA INFERIOR NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Se intentó reducir un límite de cuota por debajo del uso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR \_ EL DISPOSITIVO YA ESTÁ \_ \_ CONECTADO**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Se intentó conectar a un dispositivo que ya estaba conectado a otro dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR \_ DE \_ ALINEACIÓN DE INSTRUCCIONES**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Se intentó ejecutar una instrucción en una dirección no alineada y el sistema host no admite referencias de instrucciones no alineadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**NO SE \_ INICIÓ LA \_ GENERACIÓN DE \_ PERFILES DE ERRORES**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



No se inició la generación de perfiles.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**GENERACIÓN \_ DE PERFILES DE \_ ERRORES NO \_ DETENIDA**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



La generación de perfiles no se detiene.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR \_ NO SE PUDO \_ \_ INTERPRETAR**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



La ACL pasada no contenía la información mínima necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**GENERACIÓN \_ DE PERFILES \_ DE ERRORES AL \_ LÍMITE**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



El número de objetos de generación de perfiles activos es máximo y no se puede iniciar más.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR \_ CANT \_ WAIT**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Se usa para indicar que una operación no puede continuar sin bloquear la E/S.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR \_ CANT \_ TERMINATE \_ SELF**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Indica que un subproceso intentó finalizar por sí mismo de forma predeterminada (denominado NtTerminateThread con **NULL)** y que fue el último subproceso del proceso actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR \_ INESPERADO MM CREATE \_ \_ \_ ERR**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que están en el filtro. En este caso, se pierde información, pero el filtro controla correctamente la excepción.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR MM \_ \_ ERROR INESPERADO DE \_ \_ ASIGNACIÓN**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que están en el filtro. En este caso, se pierde información, pero el filtro controla correctamente la excepción.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR \_ INESPERADO MM EXTEND \_ \_ \_ ERR**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que están en el filtro. En este caso, se pierde información, pero el filtro controla correctamente la excepción.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR \_ TABLA DE FUNCIONES NO \_ \_ CORRECTAS**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



Se encontró una tabla de funciones con formato correcto durante una operación de desenredo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR \_ SIN TRADUCCIÓN DE \_ \_ GUID**
</dt> <dd> <dl> <dt>

560 (0x230)
</dt> <dt>



Indica que se intentó asignar protección a un directorio o archivo del sistema de archivos y uno de los SID del descriptor de seguridad no se pudo traducir en un GUID que el sistema de archivos pudiera almacenar. Esto hace que se produce un error en el intento de protección, lo que puede provocar un error en un intento de creación de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR \_ TAMAÑO \_ DE LDT NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Indica que se intentó aumentar un LDT estableciendo su tamaño o que el tamaño no era un número par de selectores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR \_ DESPLAZAMIENTO \_ DE LDT NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Indica que el valor inicial de la información de LDT no era un múltiplo entero del tamaño del selector.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR \_ INVALID \_ LDT \_ DESCRIPTOR**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Indica que el usuario proporcionó un descriptor no válido al intentar configurar descriptores Ldt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR \_ \_ DEMASIADOS \_ SUBPROCESOS**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Indica que un proceso tiene demasiados subprocesos para realizar la acción solicitada. Por ejemplo, la asignación de un token principal solo se puede realizar cuando un proceso tiene cero o uno subprocesos.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**SUBPROCESO DE \_ ERROR \_ NO EN \_ \_ PROCESO**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Se intentó operar en un subproceso dentro de un proceso específico, pero el subproceso especificado no está en el proceso especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR \_ PAGEFILE \_ QUOTA \_ EXCEEDED**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Se superó la cuota de archivos de página.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR \_ LOGON \_ SERVER \_ CONFLICT**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



El servicio Netlogon no se puede iniciar porque otro servicio netlogon que se ejecuta en el dominio entra en conflicto con el rol especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**SE REQUIERE \_ SINCRONIZACIÓN DE \_ ERRORES**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



La base de datos SAM en Windows Server está significativamente fuera de sincronización con la copia en el controlador de dominio. Se requiere una sincronización completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR \_ NET \_ OPEN \_ FAILED**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



Error en la API NtCreateFile. Este error nunca debe devolverse a una aplicación, es un lugar que el redirector de Windows Lan Manager usará en sus rutinas de asignación de errores internos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR \_ AL PRIVILEGIO DE \_ \_ E/S**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Error de privilegio} No se pudieron cambiar los permisos de E/S para el proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR \_ CONTROL \_ C \_ EXIT**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Application Exit by CTRL+C} La aplicación finalizó como resultado de ctrl+C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR \_ FALTA \_ SYSTEMFILE**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{Missing System File} El archivo del sistema %hs necesario es malo o falta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**EXCEPCIÓN \_ NO CONTROLADA POR \_ ERROR**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Error de aplicación} La excepción %s (0x%08lx) se produjo en la aplicación en la ubicación 0x%08lx.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR \_ DE \_ INIT DE LA \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Error de aplicación} La aplicación no se pudo iniciar correctamente (0x%lx). Haga clic en Aceptar para cerrar la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR \_ PAGEFILE \_ CREATE \_ FAILED**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{No se puede crear el archivo de paginación} Error al crear el archivo de paginación %hs (%lx). El tamaño solicitado era %ld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR \_ HASH DE IMAGEN NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Windows puede comprobar la firma digital de este archivo. Un cambio reciente de hardware o software podría haber instalado un archivo firmado incorrectamente o dañado, o que podría ser software malintencionado de un origen desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR \_ NO \_ PAGEFILE**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{No se especificó ningún archivo de paginación} No se especificó ningún archivo de paginación en la configuración del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**CONTEXTO FLOAT \_ NO \_ ES DE \_ ERROR**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



{EXCEPTION} Una aplicación en modo real emitió una instrucción de punto flotante y el hardware de punto flotante no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR \_ SIN PAR DE \_ \_ EVENTOS**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Se realizó una operación de sincronización de par de eventos mediante el objeto de par de eventos cliente/servidor específico del subproceso, pero no se asoció ningún objeto de par de eventos al subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR \_ DOMAIN \_ CTRLR \_ CONFIG \_ ERROR**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Un Windows Server tiene una configuración incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**CARÁCTER NO \_ ES \_ DE ERROR**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Se encontró un carácter no ilegal. Para un juego de caracteres de varios bytes, esto incluye un byte inicial sin un byte final siguiente. Para el juego de caracteres Unicode, esto incluye los caracteres 0xFFFF y 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**CARÁCTER \_ SIN DEFINIR DE \_ ERROR**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



El carácter Unicode no está definido en el juego de caracteres Unicode instalado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**VOLUMEN \_ DE DISQUETE DE \_ ERROR**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



El archivo de paginación no se puede crear en una disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR \_ BIOS \_ FAILED \_ TO \_ CONNECT \_ INTERRUPT**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



El BIOS del sistema no pudo conectar una interrupción del sistema al dispositivo o bus al que está conectado el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**CONTROLADOR DE \_ COPIA DE SEGURIDAD DE \_ ERRORES**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Esta operación solo se permite para el controlador de dominio principal del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR \_ MUTANT \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



Se ha intentado adquirir un objeto para que se superara su recuento máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR \_ SE REQUIERE EL CONTROLADOR \_ FS \_**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



Se ha accedido a un volumen para el que se requiere un controlador del sistema de archivos que aún no se ha cargado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR \_ NO SE PUEDE CARGAR EL ARCHIVO DEL \_ \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Error de archivo del Registro} El Registro no puede cargar el subárbol (archivo): %hs o su registro o alternativa. Está dañado, ausente o no se puede escribir.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR AL \_ ADJUNTAR \_ LA \_ DEPURACIÓN**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Error inesperado en [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Error inesperado al procesar una solicitud de API **DebugActiveProcess.** Puede elegir Aceptar para finalizar el proceso o Cancelar para omitir el error.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**PROCESO \_ DEL SISTEMA DE ERRORES \_ \_ FINALIZADO**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Error irreales del sistema} El proceso del sistema %hs finalizó inesperadamente con un estado de 0x%08x (0x%08x 0x%08x). El sistema se ha apagado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**DATOS DE ERROR \_ \_ NO \_ ACEPTADOS**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Datos no aceptados} El cliente TDI no pudo controlar los datos recibidos durante una indicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR: \_ ERROR DE DISCO DURO DE VDM \_ \_**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



NTVDM encontró un error grave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**TIEMPO DE \_ ESPERA DE \_ CANCELACIÓN DEL CONTROLADOR DE \_ ERROR**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Cancel Timeout} El controlador %hs no pudo completar una solicitud de E/S cancelada en el tiempo asignado.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR DE \_ COINCIDENCIA DEL MENSAJE DE \_ \_ RESPUESTA**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Error de coincidencia del mensaje de respuesta} Se intentó responder a un mensaje LPC, pero el subproceso especificado por el identificador de cliente en el mensaje no esperaba ese mensaje.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR \_ AL PERDER DATOS \_ WRITEBEHIND \_**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo %hs. Los datos se han perdido. Este error puede deberse a un error en el hardware del equipo o en la conexión de red. Intente guardar este archivo en otro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR: \_ PARÁMETROS DEL SERVIDOR CLIENTE NO \_ \_ \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Los parámetros pasados al servidor en la ventana de memoria compartida cliente/servidor no eran válidos. Es posible que se hayan puesto demasiados datos en la ventana de memoria compartida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR \_ NOT \_ TINY \_ STREAM**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



La secuencia no es una secuencia pequeña.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR \_ STACK \_ OVERFLOW \_ READ**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



El código de desbordamiento de pila debe controlar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR \_ AL CONVERTIR EN \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Códigos de estado internos de OFS que indican cómo se controla una operación de asignación. Se reintente una vez que se mueve el nodo o nodo de extensión que lo contiene o la secuencia de extensión se convierte en una secuencia grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR \_ ENCONTRADO FUERA DEL \_ \_ \_ ÁMBITO**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



El intento de encontrar el objeto encontró un objeto que coincide por identificador en el volumen, pero está fuera del ámbito del identificador utilizado para la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR \_ AL ASIGNAR \_ CUBO**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



La matriz de cubos debe crecer. Vuelva a intentar la transacción después de hacerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR \_ MARSHALL \_ OVERFLOW**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



Se ha desbordado el búfer de clasificación de usuario/kernel.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR \_ VARIANTE NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



La estructura variante proporcionada contiene datos no válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR \_ BÚFER DE COMPRESIÓN NO ESTÁ \_ \_ BIEN**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



El búfer especificado contiene datos con formato no correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR DE \_ AUDITORÍA \_**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Error de auditoría} Error al intentar generar una auditoría de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**RESOLUCIÓN \_ DEL TEMPORIZADOR DE ERROR NO \_ \_ \_ ESTABLECIDA**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



El proceso actual no estableció previamente la resolución del temporizador.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR \_ INFORMACIÓN DE INICIO DE SESIÓN \_ \_ INSUFICIENTE**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



No hay suficiente información de cuenta para iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR \_ BAD \_ DLL \_ ENTRYPOINT**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{Punto de entrada dll no válido} La biblioteca de vínculos dinámicos %hs no está escrita correctamente. El puntero de pila se ha dejado en un estado incoherente. El punto de entrada debe declararse como WINAPI o STDCALL. Seleccione SÍ para producir un error en la carga del archivo DLL. Seleccione NO para continuar con la ejecución. La selección de NO puede hacer que la aplicación funcione incorrectamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR \_ BAD \_ SERVICE \_ ENTRYPOINT**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Punto de entrada de devolución de llamada de servicio no válido} El servicio %hs no está escrito correctamente. El puntero de pila se ha dejado en un estado incoherente. El punto de entrada de devolución de llamada debe declararse como WINAPI o STDCALL. Al seleccionar Aceptar, el servicio continuará funcionando. Sin embargo, el proceso de servicio puede funcionar incorrectamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR \_ DIRECCIÓN IP \_ \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Hay un conflicto de direcciones IP con otro sistema en la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR \_ DIRECCIÓN IP \_ \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Hay un conflicto de direcciones IP con otro sistema en la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**LÍMITE DE \_ CUOTA DEL REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Espacio bajo en el Registro} El sistema ha alcanzado el tamaño máximo permitido para la parte del sistema del registro. Se omitirán las solicitudes de almacenamiento adicionales.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR \_ NO \_ HAY DEVOLUCIÓN DE LLAMADA \_ ACTIVA**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



No se puede ejecutar un servicio del sistema de devolución de devolución de llamada cuando no hay ninguna devolución de llamada activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR \_ PWD \_ TOO \_ SHORT**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



La contraseña proporcionada es demasiado corta para cumplir la directiva de su cuenta de usuario. Elija una contraseña más larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR \_ PWD \_ TOO \_ RECENT**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



La directiva de su cuenta de usuario no le permite cambiar contraseñas con demasiada frecuencia. Esto se hace para evitar que los usuarios cambien a una contraseña conocida, pero potencialmente detectada. Si cree que la contraseña se ha puesto en peligro, póngase en contacto con el administrador inmediatamente para asignar una nueva.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR \_ PWD \_ HISTORY \_ CONFLICT**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Ha intentado cambiar la contraseña por una que ha usado en el pasado. La directiva de su cuenta de usuario no lo permite. Seleccione una contraseña que no haya usado anteriormente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR \_ COMPRESIÓN NO \_ ADMITIDA**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



No se admite el formato de compresión especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR \_ PERFIL DE HW NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



La configuración del perfil de hardware especificado no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR RUTA \_ DE ACCESO DEL DISPOSITIVO \_ PLUGPLAY NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



La ruta de acceso Plug and Play del registro especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**LISTA DE \_ CUOTAS \_ DE ERRORES \_ INCOHERENTE**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



La lista de cuotas especificada es incoherente internamente con su descriptor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**EXPIRACIÓN \_ DE EVALUACIÓN \_ DE ERRORES**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Windows de evaluación} El período de evaluación para esta instalación de Windows ha expirado. Este sistema se apagará en 1 hora. Para restaurar el acceso a esta instalación de Windows, actualice esta instalación mediante una distribución con licencia de este producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR \_ DE REUBICACIÓN DE \_ DLL NO \_ ES ASÍ**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Reubicación de DLL del sistema no válido} El archivo DLL del sistema %hs se ha reubicado en memoria. La aplicación no se ejecutará correctamente. La reubicación se produjo porque el archivo DLL %hs ocupaba un intervalo de direcciones reservado para Windows archivos DLL del sistema. Se debe ponerse en contacto con el proveedor que suministra el archivo DLL para obtener un nuevo archivo DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR \_ DLL \_ INIT \_ FAILED \_ LOGOFF**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Error de inicialización de DLL} La aplicación no se pudo inicializar porque la estación de ventana se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR \_ VALIDATE \_ CONTINUE**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



El proceso de validación debe continuar con el paso siguiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR \_ NO \_ MÁS \_ COINCIDENCIAS**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



No hay más coincidencias para la enumeración de índice actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**CONFLICTO DE \_ LISTA \_ DE INTERVALOS DE \_ ERRORES**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



No se pudo agregar el intervalo a la lista de intervalos debido a un conflicto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR \_ SERVER \_ SID \_ MISMATCH**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



El proceso de servidor se ejecuta con un SID diferente del requerido por el cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR \_ CANT \_ ENABLE \_ DENY \_ ONLY**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Un grupo marcado como uso solo para denegar no se puede habilitar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR \_ FLOAT \_ MULTIPLE \_ FAULTS**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



{EXCEPTION} Varios errores de punto flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR \_ FLOAT \_ MULTIPLE \_ TRAPS**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



{EXCEPTION} Varias capturas de punto flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR \_ NOINTERFACE**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



No se admite la interfaz solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR \_ DRIVER \_ FAILED \_ SLEEP**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Error en espera del sistema} El controlador %hs no admite el modo de espera. La actualización de este controlador puede permitir que el sistema vaya al modo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR \_ AL DAÑAR EL ARCHIVO DEL \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



El archivo del sistema %1 se ha dañado y se ha reemplazado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**COMPROMISO \_ MÍNIMO DE \_ ERROR**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Memoria virtual mínima demasiado baja} El sistema tiene poca memoria virtual. Windows aumenta el tamaño del archivo de paginación de memoria virtual. Durante este proceso, se pueden denegar las solicitudes de memoria para algunas aplicaciones. Para obtener más información, vea Ayuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR \_ PNP \_ RESTART \_ ENUMERATION**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Se quitó un dispositivo, por lo que se debe reiniciar la enumeración.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR \_ SIGNATURA \_ NO VÁLIDA DE LA IMAGEN DEL \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Error irreales del sistema} La imagen del sistema %s no está firmada correctamente. El archivo se ha reemplazado por el archivo firmado. El sistema se ha cerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR \_ NECESARIO PARA REINICIAR \_ \_ PNP**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



El dispositivo no se iniciará sin un reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR \_ POTENCIA \_ INSUFICIENTE**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



No hay suficiente potencia para completar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR \_ DE INFRACCIÓN \_ DE ERROR \_ MÚLTIPLE**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



ERROR \_ DE INFRACCIÓN \_ DE ERROR \_ MÚLTIPLE


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR \_ DE APAGADO DEL \_ SISTEMA**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



El sistema está en proceso de apagado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**PUERTO \_ DE ERROR NO \_ \_ ESTABLECIDO**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Se intentó quitar un proceso DebugPort, pero aún no se ha asociado un puerto al proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR \_ DS \_ VERSION \_ CHECK \_ FAILURE**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Esta versión de Windows no es compatible con la versión de comportamiento del bosque de directorios, dominio o controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**NO \_ SE ENCONTRÓ EL INTERVALO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



No se encontró el intervalo especificado en la lista de intervalos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR \_ NOT SAFE MODE DRIVER (CONTROLADOR DE MODO NO \_ \_ \_ SEGURO)**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



El controlador no se cargó porque el sistema arranca en modo seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR \_ AL ENTRAR EN EL \_ \_ CONTROLADOR**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



El controlador no se cargó porque no se pudo llamar a la inicialización.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR DE \_ \_ ENUMERACIÓN DE \_ DISPOSITIVOS**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"%hs" encontró un error al aplicar energía o leer la configuración del dispositivo. Esto puede deberse a un error del hardware o a una conexión deficiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**PUNTO \_ DE MONTAJE DE ERROR NO \_ \_ \_ RESUELTO**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



Error en la operación de creación porque el nombre contenía al menos un punto de montaje que se resuelve en un volumen al que no está conectado el objeto de dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR \_ PARÁMETRO DE OBJETO DE DISPOSITIVO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



El parámetro de objeto de dispositivo no es un objeto de dispositivo válido o no está asociado al volumen especificado por el nombre de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR \_ MCA \_ OCCURED**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Se ha producido un error de comprobación de máquina. Consulte el registro de eventos del sistema para obtener información adicional.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR DE \_ BASE DE DATOS DEL CONTROLADOR DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Error \[ %2 al procesar \] la base de datos del controlador.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**\_SUBÁRBOL DEL SISTEMA DE ERRORES DEMASIADO \_ \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



El tamaño del subárbol del sistema ha superado su límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR DEL \_ CONTROLADOR ANTES DE LA \_ \_ \_ DESCARGA**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



No se pudo cargar el controlador porque una versión anterior del controlador todavía está en memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR \_ VOLSNAP \_ PREPARE \_ HIBERNATE**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Servicio de instantáneas de volumen} Espere mientras el Servicio de instantáneas de volumen prepara el volumen %hs para la hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR \_ DE \_ HIBERNACIÓN**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



El sistema no pudo hibernar (el código de error es %hs). La hibernación se deshabilitará hasta que se reinicie el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR \_ PWD \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



La contraseña proporcionada es demasiado larga para cumplir la directiva de su cuenta de usuario. Elija una contraseña más corta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**LIMITACIÓN \_ DEL SISTEMA DE ARCHIVOS DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



no se pudo completar la operación solicitada por una limitación del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR DE \_ ASERCIÓN \_ DE ERROR**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Se ha producido un error de aserción.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR \_ ACPI \_ ERROR**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



Error en el subsistema ACPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ASERCIÓN \_ DE WOW \_ DE ERROR**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Error de aserción wow.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR \_ PNP \_ BAD \_ MPS \_ TABLE**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



Falta un dispositivo en la tabla MPS del BIOS del sistema. Este dispositivo no se usará. Póngase en contacto con el proveedor del sistema para obtener información sobre la actualización del BIOS del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR \_ AL TRADUCIR PNP \_ \_**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Un traductor no pudo traducir los recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR \_ AL TRADUCIR \_ IRQ DE PNP \_ \_**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Un traductor de IRQ no pudo traducir recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR \_ PNP \_ INVALID \_ ID**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



El controlador %2 devolvió un identificador no válido para un dispositivo secundario (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**DEPURADOR DEL \_ \_ SISTEMA DE REACTIVACIÓN DE \_ ERRORES**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Kernel Debugger Debugger Debuggered} el depurador del sistema se ha interrumpido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**IDENTIFICADORES \_ DE ERROR \_ CERRADOS**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Handles Closed} Los identificadores de los objetos se han cerrado automáticamente como resultado de la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**INFORMACIÓN \_ ADICIONAL DE \_ ERROR**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Demasiada información} La lista de control de acceso (ACL) especificada contenía más información de la esperada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR \_ RXACT \_ COMMIT \_ NECESSARY**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Este estado de nivel de advertencia indica que el estado de transacción ya existe para el subárquico del Registro, pero que se anuló previamente una confirmación de transacción. La confirmación NO se ha completado, pero tampoco se ha revertido (por lo que puede confirmarse si lo desea).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**COMPROBACIÓN \_ DE MEDIOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Media Changed} Es posible que el medio haya cambiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**SUSTITUCIÓN \_ DE GUID DE ERROR \_ \_ REALIZADA**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Sustitución de GUID} Durante la traducción de un identificador global (GUID) a un identificador Windows seguridad (SID), no se encontró ningún prefijo GUID definido administrativamente. Se usó un prefijo de sustitución, lo que no pondrá en peligro la seguridad del sistema. Sin embargo, esto puede proporcionar un acceso más restrictivo de lo previsto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR \_ DETENIDO \_ EN \_ SYMLINK**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



La operación de creación se detuvo después de alcanzar un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



Se ha ejecutado un salto largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR \_ PLUGPLAY \_ QUERY \_ VETOED**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



La Plug and Play operación de consulta no se ha realizado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**CONSOLIDACIÓN \_ DE DESENREDO \_ DE ERRORES**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



Se ha ejecutado una consolidación de fotogramas.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**HIVE \_ DEL REGISTRO DE ERRORES \_ \_ RECUPERADO**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{Registry Hive Recovered} Subárbol del Registro (archivo): %hs está dañado y se ha recuperado. Es posible que se hayan perdido algunos datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**EL \_ ARCHIVO DLL DE ERROR PODRÍA SER \_ \_ \_ INSEGURO**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



La aplicación está intentando ejecutar código ejecutable desde el módulo %hs. Esto puede no ser seguro. Hay disponible una alternativa, %hs. ¿Debe la aplicación usar el módulo seguro %hs?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**EL \_ ARCHIVO DLL DE ERROR PODRÍA SER \_ \_ \_ INCOMPATIBLE**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



La aplicación está cargando código ejecutable desde el módulo %hs. Esto es seguro, pero puede ser incompatible con versiones anteriores del sistema operativo. Hay disponible una alternativa, %hs. ¿Debe la aplicación usar el módulo seguro %hs?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR \_ EXCEPCIÓN DBG \_ NO \_ \_ CONTROLADA**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



El depurador no controló la excepción.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR \_ DBG \_ REPLY \_ LATER**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



El depurador responderá más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR \_ DBG \_ UNABLE \_ TO \_ PROVIDE \_ HANDLE**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



El depurador no puede proporcionar identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR \_ DBG \_ TERMINATE \_ THREAD**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



Subproceso terminado del depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR \_ DBG \_ TERMINATE \_ PROCESS**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



Proceso finalizado por el depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR \_ DBG \_ CONTROL \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



El depurador tiene el control C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR \_ DBG \_ PRINTEXCEPTION \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



Excepción impresa del depurador en el control C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR \_ DBG \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



El depurador recibió la excepción RIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR \_ DBG \_ CONTROL \_ BREAK**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



El depurador recibió un salto de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR \_ DBG \_ COMMAND \_ EXCEPTION**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Excepción de comunicación de comandos del depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR \_ NOMBRE DE OBJETO \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Object Exists} Se intentó crear un objeto y el nombre del objeto ya existía.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**SUBPROCESO DE ERROR \_ \_ \_ SUSPENDIDO**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Subproceso suspendido} Se produjo una terminación de subproceso mientras se suspendía el subproceso. Se reanudó el subproceso y se presentó la finalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**IMAGEN \_ DE ERROR NO EN \_ \_ \_ BASE**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Imagen reubicada} No se pudo asignar un archivo de imagen en la dirección especificada en el archivo de imagen. Las fijaciones locales deben realizarse en esta imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR \_ RXACT \_ STATE \_ CREATED**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Este estado de nivel informativo indica que un estado de transacción de subárido del Registro especificado aún no existía y tenía que crearse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**NOTIFICACIÓN \_ DE SEGMENTO DE \_ ERROR**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Carga de segmento} Una máquina VIRTUAL DOS (VDM) carga, descarga o mueve una imagen de segmento del programa MS-DOS o Win16. Se produce una excepción para que un depurador pueda cargar, descargar o realizar un seguimiento de símbolos y puntos de interrupción dentro de estos segmentos de 16 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR \_ BAD \_ CURRENT \_ DIRECTORY**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Directorio actual no válido} El proceso no puede cambiar al directorio actual de inicio %hs. Seleccione Aceptar para establecer el directorio actual en %hs o seleccione CANCELAR para salir.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR \_ FT \_ READ \_ RECOVERY \_ FROM \_ BACKUP**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Lectura redundante} Para satisfacer una solicitud de lectura, el sistema de archivos nt tolerante a errores lee correctamente los datos solicitados de una copia redundante. Esto se hizo porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área con errores del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR \_ FT \_ WRITE \_ RECOVERY**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Escritura redundante} Para satisfacer una solicitud de escritura, el sistema de archivos nt tolerante a errores escribió correctamente una copia redundante de la información. Esto se hizo porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área con errores del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR \_ IMAGE \_ MACHINE \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Error de coincidencia de tipo de máquina} El archivo de imagen %hs es válido, pero es para un tipo de máquina distinto de la máquina actual. Seleccione Aceptar para continuar o CANCELAR para producir un error en la carga del archivo DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR \_ RECEIVE \_ PARTIAL**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Datos parciales recibidos} El transporte de red devolvió datos parciales a su cliente. Los datos restantes se enviarán más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR \_ RECEIVE \_ EXPEDITED**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Datos rápidos recibidos} El transporte de red devolvió datos a su cliente marcados como acelerados por el sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR \_ RECEIVE \_ PARTIAL \_ EXPEDITED**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Partial Expedited Data Received} El transporte de red devolvió datos parciales a su cliente y estos datos se marcaron como acelerados por el sistema remoto. Los datos restantes se enviarán más adelante.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**EVENTO \_ DE ERROR \_ REALIZADO**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Evento TDI listo} La indicación de TDI se ha completado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**EVENTO \_ DE ERROR \_ PENDIENTE**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Evento TDI pendiente} La indicación TDI ha entrado en el estado pendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR \_ AL COMPROBAR EL SISTEMA DE \_ \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Comprobación del sistema de archivos en %wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR \_ AL SALIR DE LA \_ \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Fatal Application Exit} %hs.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**IDENTIFICADOR \_ PREDEFINIDO DE \_ ERROR**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



Un identificador predefinido hace referencia a la clave del Registro especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR \_ \_ DESBLOQUEADO**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Página desbloqueada} La protección de página de una página bloqueada se cambió a "Sin acceso" y la página se desbloqueó de la memoria y del proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**NOTIFICACIÓN \_ DEL SERVICIO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



%hs


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR \_ BLOQUEADO \_**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Page Locked} Una de las páginas que se bloquearon ya estaba bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR \_ DE DISCO DURO DEL REGISTRO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Ventana emergente de la aplicación: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR \_ YA \_ WIN32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



ERROR \_ YA \_ WIN32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR \_ IMAGE \_ MACHINE \_ TYPE \_ MISMATCH \_ EXE**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Error de coincidencia de tipo de máquina} El archivo de imagen %hs es válido, pero es para un tipo de máquina distinto de la máquina actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR \_ NO \_ YIELD \_ PERFORMED**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



Se realizó una ejecución de rendimiento y no había ningún subproceso disponible para ejecutarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**REANUDACIÓN \_ DEL TEMPORIZADOR DE ERROR \_ \_ OMITIDO**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



Se omitió la marca reanudable a una API de temporizador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR \_ DE ARBITRAJE NO \_ CONTROLADA**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



El mediar ha aplazado el arbitraje de estos recursos a su elemento primario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR \_ CARDBUS \_ NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



No se puede iniciar el dispositivo CardBus insertado debido a un error de configuración en "%hs".


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR \_ DE COINCIDENCIA DEL PROCESADOR DE \_ \_ MP**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



Las CPU de este sistema de varios procesadores no tienen el mismo nivel de revisión. Para usar todos los procesadores, el sistema operativo se restringe a las características del procesador menos compatible del sistema. Si se producen problemas con este sistema, póngase en contacto con el fabricante de cpu para ver si se admite esta combinación de procesadores.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR \_ HIBERNADO**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



El sistema se ha puesto en hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR \_ AL REANUDAR \_ HIBERNACIÓN**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



El sistema se reanudó desde la hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE \_ DE ERROR \_ ACTUALIZADO**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



Windows ha detectado que el firmware del sistema (BIOS) se actualizó antes de la fecha de \[ firmware = %2, fecha de firmware actual %3 \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**CONTROLADORES DE \_ ERROR \_ QUE PIERDEN PÁGINAS \_ \_ BLOQUEADAS**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Un controlador de dispositivo está filtrando páginas de E/S bloqueadas que provocan la degradación del sistema. El sistema ha habilitado automáticamente el código de seguimiento para intentar capturar el responsable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**SISTEMA DE \_ REACTIVACIÓN \_ DE ERRORES**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



El sistema se ha puesto en marcha.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR \_ WAIT \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



ERROR \_ WAIT \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR \_ WAIT \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



ERROR \_ WAIT \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR \_ WAIT \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



ERROR \_ WAIT \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR \_ WAIT \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



ERROR \_ WAIT \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR \_ ABANDONED \_ WAIT \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



ERROR \_ ABANDONED \_ WAIT \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR \_ ABANDONED \_ WAIT \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



ERROR \_ ABANDONED \_ WAIT \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR \_ USER \_ APC**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



ERROR \_ USER \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR \_ KERNEL \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



ERROR \_ KERNEL \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR \_ ALERTADO**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



ERROR \_ ALERTADO


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**SE REQUIERE \_ ELEVACIÓN \_ DE ERRORES**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



La operación solicitada requiere elevación.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR \_ REPARSE**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



El Administrador de objetos debe realizar un análisis, ya que el nombre del archivo ha dado lugar a un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR \_ OLOCK \_ BREAK IN \_ \_ PROGRESS**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Se ha completado una operación de apertura y creación mientras se está en curso una interrupción del bloqueo operativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUMEN \_ DE ERROR \_ MONTADO**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Un sistema de archivos ha montado un nuevo volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR \_ RXACT \_ COMMITTED**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Este estado de nivel correcto indica que el estado de transacción ya existe para el subárquico del Registro, pero que se anuló previamente una confirmación de transacción. La confirmación ya se ha completado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR \_ NOTIFY \_ CLEANUP**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Esto indica que se ha completado una solicitud de cambio de notificación debido al cierre del identificador que realizó la solicitud de cambio de notificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR \_ CONEXIÓN DE TRANSPORTE PRINCIPAL CON \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Conectar error en el transporte principal} Se intentó conectarse al servidor remoto %hs en el transporte principal, pero no se pudo establecer la conexión. El equipo pudo conectarse en un transporte secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**TRANSICIÓN DE \_ ERROR DE PÁGINA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



Error de página fue un error de transición.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR DE \_ LA PÁGINA DE ERROR \_ \_ PETICIÓN DE ERROR \_ CERO**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



Error de página era un error de demanda cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**COPIA DE \_ ERROR DE LA PÁGINA DE ERROR AL \_ \_ \_ \_ ESCRIBIR**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



Error de página era un error de demanda cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**PÁGINA DE \_ ERROR DE LA PÁGINA PROTECCIÓN DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



Error de página era un error de demanda cero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ARCHIVO DE \_ \_ PAGINACIÓN DE \_ ERRORES DE PÁGINA DE \_ ERROR**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



El error de página se ha satisfecho mediante la lectura desde un dispositivo de almacenamiento secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**PÁGINA CACHÉ \_ DE \_ ERRORES \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



La página almacenada en caché se bloqueó durante la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR \_ CRASH \_ DUMP**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



El volcado de memoria existe en el archivo de paginación.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**BÚFER \_ DE ERRORES TODOS LOS \_ \_ CEROS**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



El búfer especificado contiene todos los ceros.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR \_ REPARSE \_ (OBJETO)**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



El Administrador de objetos debe realizar un análisis, ya que el nombre del archivo ha dado lugar a un vínculo simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**SE HAN \_ CAMBIADO LOS \_ REQUISITOS DE RECURSOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



El dispositivo ha hecho correctamente una detención de consulta y sus requisitos de recursos han cambiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**TRADUCCIÓN DE ERRORES \_ \_ COMPLETADA**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



El traductor ha traducido estos recursos al espacio global y no se deben realizar más traducciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR \_ NOTHING \_ TO \_ TERMINATE**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Un proceso que finaliza no tiene subprocesos para finalizar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**PROCESO \_ DE ERROR NO EN EL \_ \_ \_ TRABAJO**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



El proceso especificado no forma parte de un trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**PROCESO \_ DE ERROR EN EL \_ \_ TRABAJO**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



El proceso especificado forma parte de un trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR \_ VOLSNAP \_ HIBERNATE \_ READY**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Servicio de instantáneas de volumen} El sistema ya está listo para hibernación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR \_ FSFILTER \_ OP \_ COMPLETED \_ SUCCESSFULLY**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Un sistema de archivos o un controlador de filtro del sistema de archivos ha completado correctamente una operación FsFilter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**VECTOR \_ DE \_ INTERRUPCIÓN DE ERROR YA \_ \_ CONECTADO**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



El vector de interrupción especificado ya estaba conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**INTERRUPCIÓN \_ DE ERROR \_ TODAVÍA \_ CONECTADA**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



El vector de interrupción especificado sigue conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR \_ WAIT \_ FOR \_ OPLOCK**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Una operación se bloquea a la espera de un bloqueo temporal.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR \_ DBG \_ EXCEPTION \_ HANDLED**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Excepción controlada por el depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR \_ DBG \_ CONTINUE**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



Depurador continuado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**PILA POP \_ DE DEVOLUCIÓN \_ DE LLAMADA DE \_ ERROR**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Se produjo una excepción en una devolución de llamada en modo de usuario y se debe quitar el marco de devolución de llamada del kernel.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**COMPRESIÓN DE \_ ERRORES \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



La compresión está deshabilitada para este volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



El proveedor de datos no puede capturar hacia atrás a través de un conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR \_ CAROLROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



El proveedor de datos no puede desplazarse hacia atrás a través de un conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**FILAS \_ DE ERRORNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



El proveedor de datos requiere que se liberan los datos previamente obtenidos antes de solicitar más datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**MARCAS \_ DE \_ ACCESSOR DE ERROR \_**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



El proveedor de datos no pudo interpretar las marcas establecidas para un enlace de columna en un accessor.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERRORES \_ \_ DETECTADOS**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Se produjeron uno o varios errores al procesar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR \_ NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



La implementación no es capaz de realizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**SOLICITUD \_ DE ERROR FUERA DE \_ \_ \_ SECUENCIA**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



El cliente de un componente solicitó una operación que no es válida dado el estado de la instancia del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR \_ DE ANÁLISIS DE VERSIÓN DE \_ \_ ERROR**
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

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**HARDWARE DE \_ MEMORIA \_ DE ERROR**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



El hardware ha notificado un error de memoria incorregible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR DE \_ REPARACIÓN \_ DE DISCO \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



La operación intentada requería que se habilitara la recuperación automática.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR \_ DE RECURSO INSUFICIENTE PARA EL TAMAÑO DE SECCIÓN COMPARTIDO \_ \_ \_ \_ \_ \_ ESPECIFICADO**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



El montón desktop encontró un error al asignar memoria de sesión. Hay más información en el registro de eventos del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR \_ SYSTEM \_ POWERSTATE \_ TRANSITION**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



El estado de energía del sistema está transfiriendo de %2 a %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR \_ SYSTEM \_ POWERSTATE \_ COMPLEX \_ TRANSITION**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



El estado de energía del sistema está transfiriendo de %2 a %3, pero podría escribir %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR \_ EXCEPCIÓN DE MCA \_**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Un subproceso se envía con excepción de MCA debido a MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR \_ ACCESS \_ AUDIT \_ BY \_ POLICY**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



El acceso a %1 se supervisa mediante la regla de directiva %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR ACCESS DISABLED NO SAFER UI BY POLICY (ACCESO DE ERROR \_ DESHABILITADO SIN INTERFAZ DE USUARIO MÁS SEGURA POR \_ \_ \_ \_ \_ \_ DIRECTIVA)**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



El administrador ha restringido el acceso a %1 mediante la regla de directiva %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR \_ ABANDON \_ HIBERFILE**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Se ha invalidado un archivo de hibernación válido y se debe abandonar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR AL PERDER LA RED DE DATOS \_ \_ \_ WRITEBEHIND \_ \_ DESCONECTADA**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo %hs; los datos se han perdido. Este error puede deberse a problemas de conectividad de red. Intente guardar este archivo en otro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR \_ PERDIDO \_ WRITEBEHIND \_ DATA NETWORK SERVER \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo %hs; los datos se han perdido. El servidor en el que existe el archivo devolvió este error. Intente guardar este archivo en otro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR \_ AL PERDER EL DISCO \_ LOCAL DE DATOS \_ WRITEBEHIND \_ \_ \_**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo %hs; los datos se han perdido. Este error puede deberse a que se ha quitado el dispositivo o si el medio está protegido por escritura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR \_ TABLA \_ MCFG \_ INCORRECTA**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Los recursos necesarios para este dispositivo están en conflicto con la tabla MCFG.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR \_ DE REPARACIÓN DE DISCO \_ \_ REDIRIGIDO**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



No se pudo realizar la reparación del volumen mientras está en línea. Programe para desconectar el volumen para que se pueda reparar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR AL \_ REPARAR EL \_ DISCO \_ INCORRECTAMENTE**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



La reparación del volumen no se ha realizado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR \_ AL DAÑAR EL REGISTRO \_ \_ OVERFULL**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



Uno de los registros de daños en el volumen está lleno. No se registrarán más daños que se puedan detectar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR: \_ REGISTRO \_ DAÑADO \_**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



Uno de los registros de daños en el volumen está dañado internamente y debe volver a crearse. El volumen puede contener daños no detectados y debe examinarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR REGISTRO \_ DAÑADO \_ NO \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



Uno de los registros de daños en el volumen no está disponible para su funcionamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR \_ AL ELIMINAR EL REGISTRO \_ \_ COMPLETO \_**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



Uno de los registros de daños en el volumen se eliminó mientras aún tenía registros de daños. El volumen contiene daños detectados y debe examinarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR \_ AL BORRAR EL REGISTRO \_ DAÑADO \_**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



Chkdsk ha borrado uno de los registros de daños en el volumen y ya no contiene daños reales.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR \_ NOMBRE HUÉRFANO \_ \_ AGOTADO**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



Los archivos huérfanos existen en el volumen, pero no se pudieron recuperar porque no se pudieron crear más nombres nuevos en el directorio de recuperación. Los archivos deben moverse desde el directorio de recuperación.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR \_ OPLOCK \_ CAMBIADO A NUEVO \_ \_ \_ IDENTIFICADOR**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



El bloqueo de operación asociado a este identificador ahora está asociado a un identificador diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR \_ NO SE PUEDE CONCEDER \_ \_ \_ OPLOCK SOLICITADO**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



No se puede conceder un bloqueo de operación del nivel solicitado. Puede haber disponible un bloqueo de operación de un nivel inferior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR \_ NO SE PUEDE INTERRUMPIR \_ \_ OPLOCK**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



La operación no se ha completado correctamente porque provocaría que se rompa un bloqueo de operación. El autor de la llamada ha solicitado que los bloqueos de operación existentes no se rompa.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR \_ OPLOCK \_ HANDLE \_ CLOSED**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



Se ha cerrado el identificador con el que se asoció este bloqueo operativo. El bloqueo de operación ahora se ha roto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR \_ NO \_ ACE \_ CONDITION**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



La entrada de control de acceso (ACE) especificada no contiene una condición.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR \_ CONDICIÓN ACE NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



La entrada de control de acceso (ACE) especificada contiene una condición no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**IDENTIFICADOR \_ DE ARCHIVO DE ERROR \_ \_ REVOCADO**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



Se ha revocado el acceso al identificador de archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**IMAGEN \_ DE ERROR EN BASE \_ \_ \_ DIFERENTE**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Un archivo de imagen se asignó en una dirección diferente de la especificada en el archivo de imagen, pero las correcciones se seguirán realizando automáticamente en la imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR \_ ACCESO DE EA \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



Se denegó el acceso al atributo extendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**OPERACIÓN DE ERROR \_ \_ ANULADA**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



La operación de E/S se ha anulado debido a una salida del subproceso o a una solicitud de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR \_ E/S \_ INCOMPLETA**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



El evento de E/S superpuesta no está en un estado señalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**E/S DE ERROR \_ \_ PENDIENTE**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



La operación de E/S superpuesta está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR \_ NOACCESS**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Acceso no válido a la ubicación de memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Error al realizar la operación de página.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 
