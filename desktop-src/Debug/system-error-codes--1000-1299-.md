---
description: Describe los códigos de error 1000-1299 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Códigos de error del sistema (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538938"
---
# <a name="system-error-codes-1000-1299"></a>Códigos de error del sistema (1000-1299)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 1000 a 1299. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_desbordamiento de pila de errores \_**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Recursividad demasiado profunda; desbordamiento de la pila.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR \_ de \_ mensaje no válido**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



La ventana no puede actuar sobre el mensaje enviado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**\_no se \_ puede \_ completar el error**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



No se puede completar esta función.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR de \_ marcas no válidas \_**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Marcas no válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR de \_ \_ volumen desconocido**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



El volumen no contiene un sistema de archivos reconocido. Asegúrese de que todos los controladores del sistema de archivos necesarios estén cargados y de que el volumen no esté dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**archivo de ERROR \_ \_ no válido**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



El volumen de un archivo se ha modificado externamente, por lo que el archivo abierto ya no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR en \_ modo de pantalla completa \_**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



La operación solicitada no se puede realizar en el modo de pantalla completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR: \_ no hay \_ token**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Se ha intentado hacer referencia a un token que no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



La base de datos del registro de configuración está dañada.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



La clave del registro de configuración no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



No se pudo abrir la clave del registro de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



No se pudo leer la clave del registro de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



No se pudo escribir la clave del registro de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**registro de errores \_ \_ recuperado**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Uno de los archivos de la base de datos del registro tenía que recuperarse mediante el uso de un registro o una copia alternativa. La recuperación se realizó correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**registro de errores \_ \_ dañado**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



El registro está dañado. La estructura de uno de los archivos que contiene datos del registro está dañada o la imagen de memoria del sistema del archivo está dañada, o bien no se pudo recuperar el archivo porque la copia o el registro alternativos no estaban presentes o estaban dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR \_ de \_ e/s del registro de errores \_**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Error irrecuperable en una operación de e/s iniciada por el registro. El registro no pudo leer, escribir o vaciar, uno de los archivos que contienen la imagen del sistema del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**no se pudo obtener el \_ \_ archivo de registro \_**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



El sistema intentó cargar o restaurar un archivo en el registro, pero el archivo especificado no se encuentra en un formato de archivo de registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**clave de ERROR \_ \_ eliminada**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Se intentó realizar una operación no válida en una clave del registro que se ha marcado para su eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR: \_ no hay \_ espacio de registro \_**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



El sistema no pudo asignar el espacio necesario en un registro del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**la \_ clave de error \_ tiene \_ elementos secundarios**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



No se puede crear un vínculo simbólico en una clave del registro que ya tiene subclaves o valores.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**el \_ secundario del error \_ debe \_ ser \_ volátil**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



No se puede crear una subclave estable en una clave primaria volátil.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR de \_ notificación de \_ enumeración \_ dir**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Se está completando una solicitud de notificación de cambio y la información no se devuelve en el búfer del llamador. Ahora, el autor de la llamada necesita enumerar los archivos para buscar los cambios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_servicios dependientes de errores en \_ \_ ejecución**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Se ha enviado un control de detención a un servicio del que dependen otros servicios en ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR \_ de \_ control de servicio no válido \_**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



El control solicitado no es válido para este servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_tiempo de \_ espera de solicitud de servicio de error \_**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



El servicio no respondió a la petición de inicio o control de manera oportuna.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR de \_ servicio \_ sin \_ subproceso**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



No se pudo crear un subproceso para el servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**base de datos de servicio de ERROR \_ \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



La base de datos del servicio está bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**el \_ servicio de error \_ ya se \_ está ejecutando**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Ya se está ejecutando una instancia del servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR \_ de \_ cuenta de servicio no válida \_**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



El nombre de cuenta no es válido o no existe o la contraseña no es válida para el nombre de cuenta especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**servicio de ERROR \_ \_ deshabilitado**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



No se puede iniciar el servicio porque está deshabilitado o porque no tiene ningún dispositivo habilitado asociado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR \_ de \_ dependencia circular**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



Se especificó una dependencia de servicio circular.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**el servicio de ERROR no \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



El servicio especificado no existe como servicio instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**el \_ servicio de error \_ no puede \_ Aceptar \_ Ctrl**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



El servicio no puede aceptar mensajes de control en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**servicio de ERROR \_ \_ no \_ activo**
</dt> <dd> <dl> <dt>

1062 (0x426 al)
</dt> <dt>



El servicio no se ha iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR \_ al \_ \_ conectar el controlador de servicio \_**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



El proceso de servicio no se pudo conectar al controlador de servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_excepción \_ de error en el \_ servicio**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Se produjo una excepción en el servicio al controlar la solicitud de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**la base de datos de errores no \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



La base de datos especificada no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**\_ \_ error específico del servicio de error \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



El servicio ha devuelto un código de error específico del servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR en el \_ proceso \_ anulado**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



El proceso finalizó inesperadamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR de \_ dependencia de servicio de error \_ \_**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



No se pudo iniciar el servicio o grupo de dependencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR \_ de \_ Inicio de sesión del servicio \_**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



El servicio no se inició debido a un error de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR al \_ iniciar el servicio de error \_ \_**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Después de iniciarse, el servicio permanece en estado pendiente de inicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR \_ de \_ bloqueo de servicio no válido \_**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



El bloqueo de la base de datos del servicio especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_servicio \_ de error marcado \_ para \_ eliminación**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



El servicio especificado se ha marcado para su eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**el \_ servicio de error \_ existe**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



El servicio especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR \_ al \_ ejecutar \_ válida conocida**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



El sistema se está ejecutando actualmente con la última configuración válida conocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dependencia de servicio de ERROR \_ \_ \_ eliminada**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



El servicio de dependencia no existe o se ha marcado para su eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**el \_ Inicio de error \_ ya se \_ aceptó**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



El arranque actual ya se aceptó para su uso como el último conjunto de control válido conocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**no \_ se \_ ha iniciado nunca el servicio de errores \_**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



No se ha realizado ningún intento de iniciar el servicio desde el último arranque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR \_ de \_ nombre de servicio duplicado \_**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



El nombre ya está en uso como nombre de servicio o como nombre para mostrar del servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR \_ de \_ cuenta de servicio diferente \_**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



La cuenta especificada para este servicio es diferente de la cuenta especificada para otros servicios que se ejecutan en el mismo proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR: \_ no se puede \_ detectar el \_ error del controlador \_**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Las acciones de error solo se pueden establecer para los servicios de Win32, no para los controladores.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR \_ no se puede \_ detectar la \_ \_ anulación del proceso**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Este servicio se ejecuta en el mismo proceso que el administrador de control de servicios. Por lo tanto, el administrador de control de servicios no puede tomar medidas si el proceso de este servicio finaliza de forma inesperada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR: \_ no hay \_ programa de recuperación \_**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



No se ha configurado ningún programa de recuperación para este servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR el \_ servicio \_ no está en el \_ \_ archivo exe**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



El programa ejecutable para el que este servicio está configurado para ejecutarse no implementa el servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR \_ no \_ \_ servicio SafeBoot**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



Este servicio no se puede iniciar en modo seguro.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fin \_ del error de \_ medio**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



Se ha alcanzado el final físico de la cinta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marca de ERROR de ERROR \_ \_ detectada**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Un acceso a cinta ha alcanzado una marca de acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR al \_ iniciar el \_ \_ medio**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



Se encontró el principio de la cinta o una partición.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR \_ SETMARK \_ detectado**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Un acceso a cinta llegó al final de un conjunto de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR \_ no \_ se \_ detectó ningún dato**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



No hay más datos en la cinta.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR de \_ partición \_**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



No se pudo crear la partición de la cinta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR \_ de \_ longitud de bloque no válida \_**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Al acceder a una nueva cinta de una partición multivolumen, el tamaño de bloque actual es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**el \_ dispositivo de error \_ no tiene \_ particiones**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



No se encontró la información de la partición de cinta al cargar una cinta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR \_ no se puede \_ \_ bloquear el \_ medio**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



No se puede bloquear el mecanismo de expulsión de medios.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR: \_ no se puede \_ descargar el \_ \_ medio**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



No se puede descargar el medio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**medios de ERROR \_ \_ modificados**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Es posible que el medio de la unidad haya cambiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_restablecimiento del bus de error \_**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Se restableció el bus de e/s.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR: \_ no hay \_ medios \_ en la \_ unidad**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



No hay medios en la unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR \_ sin \_ traducción Unicode \_**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



No existe ninguna asignación para el carácter Unicode en la página de códigos multibyte de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR \_ \_ al inicializar el archivo dll \_**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Error en una rutina de inicialización de la biblioteca de vínculos dinámicos (DLL).


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR \_ \_ de apagado en \_ curso**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



Está en curso un cierre del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR: \_ no hay ningún \_ apagado \_ en \_ curso**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



No se puede anular el cierre del sistema porque no había ningún cierre en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR de \_ dispositivo de e/s \_**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



La solicitud no se pudo realizar debido a un error de dispositivo de E/S.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR de \_ serie \_ sin \_ dispositivo**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



No se inicializó correctamente ningún dispositivo serie. El controlador serie se descargará.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**IRQ de ERROR \_ \_ ocupado**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



No se puede abrir un dispositivo que compartía una solicitud de interrupción (IRQ) con otros dispositivos. Al menos otro dispositivo que utiliza esa IRQ ya estaba abierto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERRORES \_ más \_ escrituras**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Una operación de e/s en serie se completó mediante otra escritura en el puerto serie. El \_ \_ contador XOFF serie ioctl llegó a \_ cero.)


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**tiempo de espera del \_ contador de errores \_**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Se completó una operación de e/s en serie porque expiró el período de tiempo de espera. El \_ \_ contador XOFF serie ioctl \_ no llegó a cero.)


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR de \_ marca de ID. de disquete \_ \_ \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



No se encontró ninguna marca de dirección de identificador en el disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR de \_ cilindro de disquete \_ incorrecto \_**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Discrepancia entre el campo ID. de sector de disquete y la dirección de pista de la controladora de disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**error \_ desconocido en el disquete \_ \_**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



El controlador de disquete ha detectado un error no reconocido por el controlador de disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR de \_ \_ registros incorrectos de disquete \_**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



El controlador de disquete devolvió resultados incoherentes en sus registros.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR en la \_ \_ recalibración del disco \_**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Al tener acceso al disco duro, se produjo un error en la operación de recalibración, incluso después de los reintentos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR en la \_ operación de disco \_ \_**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Al tener acceso al disco duro, se produjo un error en una operación de disco incluso después de los reintentos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR \_ \_ al restablecer el disco \_**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Al tener acceso al disco duro, se necesitaba un restablecimiento del controlador de disco, pero se produjo un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**desbordamiento de ERROR \_ FDM \_**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Se encontró el final físico de la cinta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR \_ de \_ memoria insuficiente en el \_ servidor \_**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



No hay suficiente espacio de almacenamiento en servidores para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR \_ de \_ interbloqueo posible**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



Se ha detectado una posible condición de interbloqueo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_alineación asignada de error \_**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



La dirección base o el desplazamiento de archivo especificados no tienen la alineación adecuada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR al \_ establecer el \_ Estado de energía \_ \_ vetado**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Un intento de cambiar el estado de energía del sistema fue vetado por otra aplicación o controlador.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR \_ al establecer el \_ Estado de energía \_ \_**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Error del BIOS del sistema al intentar cambiar el estado de energía del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR \_ demasiados \_ \_ vínculos**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



Se intentó crear más vínculos en un archivo de los que admite el sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR \_ de \_ versión anterior de Win \_**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



El programa especificado requiere una versión más reciente de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR \_ de \_ aplicación \_ del sistema operativo incorrecto**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



El programa especificado no es un programa para Windows o MS-DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR \_ de \_ aplicación de instancia única \_**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



No se puede iniciar más de una instancia del programa especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR en la \_ \_ aplicación RMODE**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



El programa especificado se ha escrito para una versión anterior de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR \_ de \_ dll no válida**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Uno de los archivos de biblioteca necesarios para ejecutar esta aplicación está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR \_ sin \_ Asociación**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



No hay ninguna aplicación asociada al archivo especificado para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR de \_ DDE \_**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Error al enviar el comando a la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_ \_ no \_ se encontró el archivo dll de error**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



No se encuentra uno de los archivos de biblioteca necesarios para ejecutar esta aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR: \_ no hay \_ más \_ \_ identificadores de usuario**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



El proceso actual ha utilizado todos los identificadores del sistema para los objetos de administrador de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ solo sincronización de mensajes de error \_**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



El mensaje solo se puede usar con operaciones sincrónicas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**elemento de origen de ERROR \_ \_ \_ vacío**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



El elemento de origen indicado no tiene ningún medio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**elemento de destino de ERROR \_ \_ \_ completo**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



El elemento de destino indicado ya contiene medios.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR \_ de \_ dirección de elemento no válida \_**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



El elemento indicado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR \_ revista \_ no \_ presente**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



El elemento indicado es parte de una revista que no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR \_ de \_ reinicialización de dispositivo \_ necesaria**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



El dispositivo indicado requiere reinicialización debido a errores de hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**el \_ dispositivo de error \_ requiere \_ limpieza**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



El dispositivo ha indicado que se requiere limpieza antes de intentar realizar más operaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR \_ al \_ abrir la puerta del dispositivo \_**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



El dispositivo ha indicado que la puerta está abierta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR de \_ dispositivo \_ no \_ conectado**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



El dispositivo no está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**\_no \_ se encontró el error**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Elemento no encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR \_ sin \_ coincidencia**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



No hay ninguna coincidencia para la clave especificada en el índice.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ no \_ se encontró el conjunto de errores**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



El conjunto de propiedades especificado no existe en el objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_ \_ no \_ se encontró el punto de error**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



El punto pasado a GetMouseMovePoints no está en el búfer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR: \_ no hay \_ servicio de seguimiento \_**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



El servicio de seguimiento (estación de trabajo) no se está ejecutando.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR: \_ no hay \_ \_ ID. de volumen**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



No se pudo encontrar el ID. de volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**\_no se \_ puede \_ quitar el \_ reemplazo**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



No se puede quitar el archivo que se va a reemplazar.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR \_ no se puede \_ \_ cambiar el \_ reemplazo**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



No se puede trasladar el archivo de reemplazo al archivo que se va a reemplazar. El archivo que se va a reemplazar ha conservado su nombre original.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR \_ no se puede \_ \_ trasladar el \_ reemplazo \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



No se puede trasladar el archivo de reemplazo al archivo que se va a reemplazar. Se ha cambiado el nombre del archivo que se va a reemplazar con el nombre de la copia de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ eliminación \_ en curso del diario de errores \_**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



Se está eliminando el diario de cambios de volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**diario de errores \_ \_ no \_ activo**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



El diario de cambios de volumen no está activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_ \_ se encontró un archivo potencial de error \_**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



Se encontró un archivo, pero es posible que no sea el archivo correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrada de diario de errores \_ \_ \_ eliminada**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



La entrada del diario se ha eliminado del diario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**el \_ cierre de errores \_ está \_ programado**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Ya se ha programado un cierre del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR al \_ cerrar \_ los usuarios que \_ iniciaron sesión \_**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



No se puede iniciar el apagado del sistema porque otros usuarios han iniciado sesión en el equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR \_ de \_ dispositivo incorrecto**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



El nombre de dispositivo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR de \_ conexión sin \_ DISP.**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



El dispositivo no está conectado actualmente, pero es una conexión recordada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo de ERROR \_ \_ ya \_ recordado**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



El nombre del dispositivo local tiene una conexión recordada a otro recurso de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**NO se ha podido obtener una \_ \_ \_ ruta de red o no \_ válida \_**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



La ruta de acceso de red se escribió incorrectamente, no existe o el proveedor de red no está disponible en este momento. Vuelva a escribir la ruta de acceso o póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR \_ de \_ proveedor incorrecto**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



El nombre de proveedor de red especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR \_ no se puede \_ abrir el \_ Perfil**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



No se puede abrir el perfil de conexión de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR \_ de \_ perfil incorrecto**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



El perfil de conexión de red está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR \_ no \_ contenedor**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



No se puede enumerar un contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**error de ERROR \_ extendido \_**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Se ha producido un error extendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR \_ de \_ GROUPNAME no válido**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



El formato del nombre de grupo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR \_ de \_ nombre de equipo no válido**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



El formato del nombre de equipo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR \_ EVENTNAME no válido \_**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



El formato del nombre de evento especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR \_ domainname no válido \_**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



El formato del nombre de dominio especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR \_ de \_ ServiceName no válido**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



El formato del nombre de servicio especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR \_ de \_ la**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



El formato del nombre de red especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR \_ SHARENAME no válido \_**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



El formato del nombre de recurso compartido especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR \_ PASSWORDNAME no válido \_**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



El formato de la contraseña especificada no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR \_ de \_ MESSAGENAME no válido**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



El formato del nombre de mensaje especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR \_ MESSAGEDEST no válido \_**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



El formato del destino del mensaje especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflicto de \_ credenciales de sesión de error \_**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



No se permiten varias conexiones a un servidor o recurso compartido por el mismo usuario, usando más de un nombre de usuario. Desconecte todas las conexiones anteriores al servidor o recurso compartido e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR \_ de \_ límite de sesión remota \_ \_ superado**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



Se intentó establecer una sesión en un servidor de red, pero ya hay demasiadas sesiones establecidas en ese servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR \_ DUP \_ nombreDominio**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



El nombre de grupo de trabajo o dominio ya está siendo utilizado por otro equipo de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR: \_ no hay \_ red**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



La red no está presente o no se ha iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR \_ cancelado**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



El usuario canceló la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_ \_ archivo asignado al usuario con errores \_**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



La operación solicitada no se puede realizar en un archivo con una sección asignada por el usuario abierta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR de \_ conexión \_ rechazada**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



El equipo remoto rechazó la conexión de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR \_ de \_ desconexión correcta**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



La conexión de red se cerró correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**Dirección de ERROR \_ \_ ya \_ asociada**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



El punto de conexión de transporte de red ya tiene una dirección asociada.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Dirección de ERROR \_ \_ no \_ asociada**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Todavía no se ha asociado una dirección al punto de conexión de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**conexión de ERROR \_ \_ no válida**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Se intentó realizar una operación en una conexión de red inexistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR de \_ conexión \_ activa**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Se intentó realizar una operación no válida en una conexión de red activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR de \_ red \_ inaccesible**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



No se puede tener acceso a la ubicación de red. Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR de \_ host no \_ accesible**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



No se puede tener acceso a la ubicación de red. Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**Protocolo de ERROR \_ \_ inaccesible**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



No se puede tener acceso a la ubicación de red. Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**no \_ se \_ puede tener acceso al puerto de error**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



No hay ningún servicio funcionando en el punto de conexión de la red de destino del sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**solicitud de ERROR \_ \_ anulada**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



Se anuló la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR de \_ conexión \_ anulada**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



El sistema local anuló la conexión de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR de \_ reintento**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



No se pudo completar la operación. Se debe realizar un reintento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_límite de \_ número de conexiones de error \_**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



No se pudo establecer una conexión con el servidor porque se ha alcanzado el límite del número de conexiones simultáneas para esta cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**restricción de tiempo de inicio de sesión de ERROR \_ \_ \_**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Intentando iniciar sesión durante una hora del día no autorizada para esta cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR de \_ Inicio de sesión \_ WKSTA \_ RESTRICTION**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



La cuenta no está autorizada para iniciar sesión desde esta estación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR \_ de \_ dirección incorrecta**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



No se pudo usar la dirección de red para la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR \_ ya \_ registrado**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



El servicio ya está registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ no \_ se encontró el servicio de error**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



El servicio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR \_ no \_ autenticado**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



No se realizó la operación solicitada porque el usuario no se ha autenticado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR \_ al \_ iniciar sesión \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



No se realizó la operación solicitada porque el usuario no ha iniciado sesión en la red. El servicio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR de \_ continuación**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Continúe con el trabajo en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR \_ ya \_ inicializado**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



Se intentó realizar una operación de inicialización cuando ya se ha completado la inicialización.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR: \_ no hay \_ más \_ dispositivos**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



No hay más dispositivos locales.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**NO se ha podido \_ \_ este \_ sitio**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



El sitio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**\_existe un \_ controlador de dominio de error \_**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Ya existe un controlador de dominio con el nombre especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR \_ solo \_ si \_ está conectado**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Esta operación solo se admite cuando se está conectado al servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR al \_ invalidar \_ nochanges**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



El marco de directiva de grupo debe llamar a la extensión incluso si no hay ningún cambio.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR \_ de \_ Perfil de usuario incorrecto \_**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



El usuario especificado no tiene un perfil válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR \_ no \_ compatible \_ con \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



Esta operación no se admite en un equipo que ejecute Windows Server 2003 para Small Business Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR \_ \_ de apagado \_ del servidor en \_ curso**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



El equipo servidor se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR de \_ host \_ inactivo**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



El sistema remoto no está disponible. Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR \_ de \_ SID sin cuenta \_**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



El identificador de seguridad proporcionado no procede de un dominio de cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR \_ de \_ SID sin dominio \_**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



El identificador de seguridad proporcionado no tiene un componente de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR de el \_ \_ bloque APPHELP**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



Cuadro de diálogo de AppHelp cancelado, lo que impide que se inicie la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR \_ \_ de acceso deshabilitado \_ por \_ Directiva**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Este programa está bloqueado por la Directiva de grupo. Para obtener más información, póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR de \_ registro de NAT de reg \_ \_**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Un programa intenta utilizar un valor de registro no válido. Normalmente causado por un registro no inicializado. Este error es específico de Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR \_ CSCSHARE \_ sin conexión**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



El recurso compartido está actualmente sin conexión o no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR \_ PKINIT \_ error**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



El protocolo Kerberos encontró un error al validar el certificado KDC durante el inicio de sesión de la tarjeta inteligente. Hay más información en el registro de eventos del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR en el \_ \_ subsistema de tarjeta inteligente \_**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



El protocolo Kerberos encontró un error al intentar el uso del subsistema de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR de \_ degradación \_ detectado**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



El sistema no puede ponerse en contacto con un controlador de dominio para atender la solicitud de autenticación. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**máquina de ERROR \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



El equipo está bloqueado y no se puede apagar sin la opción Force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**la \_ devolución de llamada de error \_ proporcionó \_ datos no válidos \_**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Una devolución de llamada definida por la aplicación proporcionó datos no válidos cuando se llamó a.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR en la \_ sincronización en \_ primer plano \_ \_**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



El marco de directiva de grupo debe llamar a la extensión en la actualización sincrónica de la Directiva de primer plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**controlador de ERROR \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Se ha bloqueado la carga de este controlador.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR \_ \_ de importación no válida \_ de un \_ \_ archivo no dll**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Una biblioteca de vínculos dinámicos (DLL) hacía referencia a un módulo que no era un archivo DLL ni la imagen ejecutable del proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR de \_ acceso a \_ WebBlade deshabilitado \_**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows no puede abrir este programa porque se ha deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR de \_ acceso a la \_ manipulación de \_ WebBlade deshabilitada \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows no puede abrir este programa porque el sistema de cumplimiento de licencias se ha manipulado o dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR de recuperación de errores \_ \_**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Error en la recuperación de la transacción.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR \_ ya \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



El subproceso actual ya se ha convertido en una fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR \_ ya \_ subproceso**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



El subproceso actual ya se ha convertido a partir de una fibra.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_saturación del \_ búfer de pila de errores \_**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



El sistema detectó un desbordamiento de un búfer basado en la pila en esta aplicación. Esta saturación podría permitir que un usuario malintencionado gane el control de esta aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**cuota de parámetro de ERROR \_ \_ \_ superada**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



Los datos presentes en uno de los parámetros son más de lo que puede funcionar en la función.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**depurador de errores \_ \_ inactivo**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Error al intentar realizar una operación en un objeto de depuración porque el objeto está en proceso de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR \_ \_ al cargar el retraso de errores \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Error al tratar de cargar con retraso un archivo. dll u obtener una dirección de función en un archivo. dll de carga retrasada.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR \_ VDM no \_ permitido**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 es una aplicación de 16 bits. No tiene permisos para ejecutar aplicaciones de 16 bits. Compruebe los permisos del administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**error no \_ identificado \_**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Existe información insuficiente para identificar la causa del error.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR en el \_ \_ parámetro CRUNTIME no válido \_**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



El parámetro pasado a una función en tiempo de ejecución de C es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR \_ más allá de \_ VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



La operación se produjo más allá de la longitud de datos válida del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR de \_ tipo de SID de servicio no compatible \_ \_ \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



No se pudo iniciar el servicio porque uno o varios servicios del mismo proceso tienen una configuración de tipo de SID de servicio no compatible. Un servicio con tipo de SID de servicio restringido solo puede coexistir en el mismo proceso con otros servicios con un tipo de SID restringido. Si se acaba de configurar el tipo de SID de servicio para este servicio, el proceso de hospedaje debe reiniciarse para iniciar este servicio.

En Windows Server 2003 y Windows XP, un servicio sin restricciones no puede coexistir en el mismo proceso con otros servicios. El servicio con el tipo de SID de servicio sin restricciones debe moverse a un proceso de propiedad para poder iniciar este servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**proceso de controlador de ERROR \_ \_ \_ finalizado**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



El proceso que hospeda el controlador de este dispositivo ha finalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_límite de implementación de errores \_**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Una operación intentó superar un límite definido por la implementación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**el \_ proceso de error \_ está \_ protegido**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



El proceso de destino o el proceso que contiene el subproceso de destino es un proceso protegido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR del \_ servicio de \_ notificación de \_ cliente \_**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



El cliente de notificación de servicio se atrasa demasiado detrás del estado actual de los servicios de la máquina.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**cuota de disco de ERROR \_ \_ \_ superada**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



No se pudo realizar la operación de archivo solicitada porque se superó la cuota de almacenamiento. Para liberar espacio en disco, mueva los archivos a otra ubicación o elimine los archivos innecesarios. Para obtener más información, póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**contenido de ERROR \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



No se pudo realizar la operación de archivo solicitada porque la Directiva de almacenamiento bloquea ese tipo de archivo. Para obtener más información, póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR de privilegio de servicio no \_ compatible \_ \_**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Un privilegio que el servicio necesita para funcionar correctamente no existe en la configuración de la cuenta de servicio. Puede usar el complemento Servicios de Microsoft Management Console (MMC) (Services. msc) y el complemento MMC configuración de seguridad local (SECPOL. msc) para ver la configuración del servicio y la configuración de la cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR de la aplicación de ERROR \_ \_**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Parece que un subproceso implicado en esta operación no responde.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR \_ de \_ etiqueta no válida**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indica que un determinado identificador de seguridad no se puede asignar como etiqueta de un objeto.


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

 

 




