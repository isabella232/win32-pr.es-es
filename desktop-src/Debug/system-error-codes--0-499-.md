---
description: Describe los códigos de error 0-499 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Códigos de error del sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907268"
---
# <a name="system-error-codes-0-499"></a>Códigos de error del sistema (0-499)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 0 a 499). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR \_ correcto**
</dt> <dd> <dl> <dt>

0 (0X0)
</dt> <dt>



La operación se ha completado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR \_ de \_ función no válida**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Función incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_ \_ no \_ se encontró el archivo de error**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



El sistema no encuentra el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_ \_ no \_ se encontró la ruta de error**
</dt> <dd> <dl> <dt>

3 (0X3)
</dt> <dt>



el sistema no encuentra la ruta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR \_ demasiados \_ \_ \_ archivos abiertos**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



El sistema no puede abrir el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR de \_ acceso \_ denegado**
</dt> <dd> <dl> <dt>

5 (0X5)
</dt> <dt>



Acceso denegado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



El identificador no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR de la \_ arena \_**
</dt> <dd> <dl> <dt>

7 (0X7)
</dt> <dt>



Los bloques de control de almacenamiento se han destruido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



No hay recursos de memoria suficientes disponibles para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR \_ de \_ bloque no válido**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



La dirección del bloque de control de almacenamiento no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR \_ de \_ entorno incorrecto**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



El entorno no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR \_ de \_ formato incorrecto**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Se ha intentado cargar un programa con un formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR \_ de \_ acceso no válido**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



El código de acceso no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR de \_ datos no válidos \_**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Los datos no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



No hay suficiente espacio de almacenamiento disponible para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR \_ de \_ unidad no válida**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



El sistema no encuentra la unidad especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR en el \_ \_ directorio actual**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



No se puede quitar el directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR \_ no es el \_ mismo \_ dispositivo**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



El sistema no puede trasladar el archivo a una unidad de disco diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR: \_ no hay \_ más \_ archivos**
</dt> <dd> <dl> <dt>

18 (0X12)
</dt> <dt>



No hay más archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR \_ de \_ protección contra escritura**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



El medio está protegido contra escritura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR \_ de \_ unidad incorrecta**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



El sistema no encuentra el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR \_ no \_ preparado**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



El dispositivo no está listo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR \_ de \_ comando incorrecto**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



El dispositivo no reconoce el comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**CRC de ERROR \_**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Error de datos (comprobación de redundancia cíclica).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR \_ de \_ longitud incorrecta**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



El programa emitió un comando pero la longitud del comando es incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**búsqueda de errores \_**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



La unidad no puede encontrar un área o un seguimiento específicos en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR \_ de \_ disco no dos \_**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



No se puede tener acceso al disco o disquete especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ no \_ se encontró el sector de error**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



La unidad no puede encontrar el sector solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR \_ \_ de falta de \_ papel**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



La impresora se ha quedado sin papel.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR de escritura de ERROR \_ \_**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



El sistema no puede escribir en el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR de lectura de ERROR \_ \_**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



El sistema no puede leer desde el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR de \_ gen. \_**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Un dispositivo conectado al sistema no funciona.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**infracción de \_ uso compartido de errores \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



El proceso no puede obtener acceso al archivo porque otro proceso lo está utilizando.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**infracción de bloqueo de ERROR \_ \_**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



El proceso no puede obtener acceso al archivo porque otro proceso ha bloqueado una parte de este.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR \_ de \_ disco incorrecto**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



El disco incorrecto está en la unidad. Inserte %2 (número de serie del volumen: %3) en la unidad %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**se \_ \_ superó el búfer de uso compartido de errores \_**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Demasiados archivos abiertos para compartir.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR de \_ control de \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Llegó al final del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR al \_ controlar el \_ disco \_ lleno**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



El disco está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ no \_ admitido**
</dt> <dd> <dl> <dt>

50 (bajo la letra)
</dt> <dt>



No se admite la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR \_ REM \_ no \_ lista**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows no puede encontrar la ruta de acceso de red. Compruebe que la ruta de acceso de red es correcta y que el equipo de destino no está ocupado o desactivado. Si Windows todavía no encuentra la ruta de acceso de red, póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR \_ de \_ nombre DUP**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



No estaba conectado porque existe un nombre duplicado en la red. Si se une a un dominio, vaya a sistema en el panel de control para cambiar el nombre del equipo e inténtelo de nuevo. Si se une a un grupo de trabajo, elija otro nombre de grupo de trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR \_ \_ NETPATH incorrecto**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



No se ha encontrado la ruta de acceso de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR de \_ red \_ ocupada**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



La red está ocupada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**\_ \_ no existe el desarrollador de errores \_**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



El recurso o el dispositivo de red especificado ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR \_ demasiados comandos \_ \_**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



Se ha alcanzado el límite del comando de BIOS de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR \_ ADAP \_ HDW \_ error**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Se ha producido un error de hardware en el adaptador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR \_ de \_ net \_ resp**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



El servidor especificado no puede ejecutar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR \_ UNEXP \_ net \_ Err**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Se produjo un error de red inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR \_ \_ PEND. \_**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



El adaptador remoto no es compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR \_ PRINTQ \_ completo**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



La cola de impresión está llena.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR: \_ no hay \_ espacio en cola de impresión \_**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



El espacio para almacenar el archivo en espera de ser impreso no está disponible en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR de \_ impresión \_ cancelada**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



El archivo en espera de ser impreso se ha eliminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**se \_ eliminó el error de la \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



El nombre de red especificado ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR \_ de \_ acceso a la red \_ denegado**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Se denegó el acceso a la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR \_ de \_ tipo de desarrollo incorrecto \_**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



El tipo de recurso de red no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR \_ de \_ nombre de red incorrecto \_**
</dt> <dd> <dl> <dt>

67 (0X43)
</dt> <dt>



No se encuentra el nombre de red especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR \_ demasiados \_ \_ nombres**
</dt> <dd> <dl> <dt>

68 (0X44)
</dt> <dt>



Se superó el límite de nombres para la tarjeta de adaptador de red del equipo local.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR \_ demasiados \_ \_ SESS**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



Se superó el límite de sesión de BIOS de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**uso compartido de errores en \_ \_ pausa**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



El servidor remoto se ha pausado o está en proceso de iniciarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR \_ req \_ no \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



No se pueden realizar más conexiones a este equipo remoto en este momento porque ya hay tantas conexiones como el equipo puede aceptar.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR de \_ redir en \_ pausa**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



Se pausó la impresora o el dispositivo de disco especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**\_existe un archivo de error \_**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



El archivo ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**el ERROR \_ no se puede \_ hacer**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



No se puede crear el directorio o el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR \_ \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Error en INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR \_ \_ de \_ estructuras**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



El almacenamiento para procesar esta solicitud no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR \_ ya \_ asignado**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



El nombre del dispositivo local ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR \_ de \_ contraseña no válida**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



La contraseña de red especificada no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR \_ de \_ parámetro no válido**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



El parámetro no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR de ERROR de \_ escritura de net \_ \_**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Error de escritura en la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**\_no hay \_ ranuras de procedimiento \_**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



El sistema no puede iniciar otro proceso en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR \_ demasiados \_ \_ semáforos**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



No se puede crear otro semáforo de sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR \_ excl \_ SEM \_ ya es \_ propiedad**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



El semáforo exclusivo es propiedad de otro proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR \_ SEM \_ \_ establecido**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



El semáforo se establece y no se puede cerrar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR \_ demasiadas \_ \_ solicitudes de SEM \_**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



No se puede volver a establecer el semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR \_ no \_ válido \_ en \_ el momento de la interrupción**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



No se pueden solicitar semáforos exclusivos en el momento de la interrupción.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR \_ de \_ propietario de SEM \_**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



La propiedad anterior de este semáforo ha finalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_límite de \_ usuarios de SEM de error \_**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Inserte el disco para la unidad %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR \_ al \_ cambiar el disco**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



El programa se detuvo porque no se insertó un disquete alternativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unidad de ERROR \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



El disco está en uso o bloqueado por otro proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR \_ de \_ canalización interrumpida**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



La canalización ha finalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR \_ al abrir el error \_**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



El sistema no puede abrir el dispositivo o el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_desbordamiento de búfer de error \_**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



El nombre de archivo es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR de \_ disco \_ lleno**
</dt> <dd> <dl> <dt>

112 (0X70)
</dt> <dt>



There is not enough space on the disk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR: \_ no hay \_ más \_ \_ identificadores de búsqueda**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



No hay más identificadores de archivo internos disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR \_ de \_ identificador de destino no válido \_**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



El identificador de archivo interno de destino es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR \_ de \_ categoría no válida**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



La llamada IOCTL realizada por el programa de la aplicación no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR \_ al \_ \_ cambiar el modificador de comprobación**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



El valor del parámetro de modificador de comprobación en escritura no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR \_ de \_ nivel de controlador incorrecto \_**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



El sistema no admite el comando solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**llamada de ERROR \_ \_ no \_ implementada**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Esta función no es compatible con este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR \_ de \_ tiempo de espera de SEM**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Expiró el tiempo de espera del semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ de \_ búfer insuficiente**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



El área de datos que se pasa a una llamada del sistema es demasiado pequeña.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR \_ de \_ nombre no válido**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



El nombre de archivo, el nombre de directorio o la sintaxis de la etiqueta de volumen son incorrectos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR \_ de \_ nivel no válido**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



El nivel de llamada del sistema no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR: \_ no hay \_ etiqueta de volumen \_**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



El disco no tiene etiqueta de volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR \_ mod \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



No se pudo encontrar el módulo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**\_ \_ no \_ se encontró el procedimiento de error**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



No se pudo encontrar el procedimiento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR de \_ espera \_ sin \_ elementos secundarios**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



No hay ningún proceso secundario que esperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR \_ secundario \_ no \_ completado**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



La aplicación %1 no se puede ejecutar en modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_identificador de \_ acceso \_ directo de error**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Intento de usar un identificador de archivo para una partición de disco abierta para una operación distinta de e/s de disco sin procesar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR \_ de \_ búsqueda negativa**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Se intentó trasladar el puntero de archivo antes del principio del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR \_ \_ de búsqueda en el \_ dispositivo**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



No se puede establecer el puntero de archivo en el dispositivo o archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**el ERROR es el destino de la \_ \_ Unión \_**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



No se puede usar un comando JOIN o SUBSt para una unidad que contenga unidades Unidas previamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**el ERROR \_ está \_ Unido**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Se intentó usar un comando JOIN o SUBSt en una unidad que ya se ha unido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**el ERROR \_ es \_ SUBSTED**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Se intentó usar un comando JOIN o SUBSt en una unidad que ya se ha sustituido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR \_ no \_ Unido**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



El sistema intentó eliminar la combinación de una unidad que no está unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR \_ no \_ SUBSTED**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



El sistema intentó eliminar la sustitución de una unidad que no se sustituye.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**\_combinación \_ de errores para \_ unirse**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



El sistema intentó unir una unidad a un directorio en una unidad unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR \_ de SUBST \_ en \_ subst**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



El sistema intentó sustituir una unidad por un directorio en una unidad sustituida.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR \_ \_ al combinar con \_ subst**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



El sistema intentó unir una unidad a un directorio en una unidad sustituida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR \_ subst \_ a \_ join**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



El sistema intentó sustituir una unidad a un directorio en una unidad unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR \_ de \_ unidad ocupada**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



El sistema no puede realizar una combinación o SUBSt en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR en la \_ misma \_ unidad**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



El sistema no puede unir ni sustituir una unidad a o para un directorio de la misma unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR de \_ directorio \_ no \_ raíz**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



El directorio no es un subdirectorio del directorio raíz.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR de \_ dir \_ no \_ vacío**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



El directorio no está vacío.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**el ERROR \_ es \_ subst \_ path**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



La ruta de acceso especificada se usa en un sustituto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR en la \_ \_ ruta de acceso de combinación \_**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



No hay suficientes recursos disponibles para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**Ruta de acceso de ERROR \_ \_ ocupada**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



La ruta de acceso especificada no se puede usar en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**el ERROR \_ es el \_ destino de SUBST \_**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Se intentó unir o sustituir una unidad para la que un directorio de la unidad es el destino de un sustituto anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_seguimiento del sistema de errores \_**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



No se especificó la información de seguimiento del sistema en el archivo de CONFIG.SYS o no se permite el seguimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR \_ al \_ recuento de eventos no válidos \_**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



El número de eventos de semáforo especificados para DosMuxSemWait no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR \_ demasiados \_ \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



No se ejecutó DosMuxSemWait; ya se han establecido demasiados semáforos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR \_ de \_ formato de lista no válido \_**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



La lista de DosMuxSemWait no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**etiqueta de ERROR \_ \_ demasiado \_ larga**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



La etiqueta de volumen especificada supera el límite de caracteres de etiqueta del sistema de archivos de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR \_ demasiados \_ \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



No se puede crear otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**señal de ERROR \_ \_ rechazada**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



El proceso del destinatario ha rechazado la señal.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR \_ DEScartado**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



El segmento ya se ha descartado y no se puede bloquear.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR \_ no \_ bloqueado**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



El segmento ya está desbloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR \_ de \_ THREADID erróneo \_ addr**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



La dirección para el ID. de subproceso no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR de \_ argumentos no válidos \_**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Uno o varios argumentos no son correctos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR \_ de \_ ruta de nombres incorrecta**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



La ruta de acceso especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**señal de ERROR \_ \_ pendiente**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Ya hay una señal pendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR \_ máximo \_ THRDS \_ alcanzado**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



No se pueden crear más subprocesos en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**error de bloqueo de errores \_ \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



No se puede bloquear una región de un archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR \_ ocupado**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



El recurso solicitado está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR \_ \_ de compatibilidad \_ del dispositivo en \_ curso**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



La detección de la compatibilidad del comando del dispositivo está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR de \_ cancelación de \_ infracción**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



No había una solicitud de bloqueo pendiente para la región de cancelación proporcionada.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR \_ de \_ bloqueos atómicos \_ no \_ admitidos**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



El sistema de archivos no admite cambios atómicos en el tipo de bloqueo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR \_ de \_ número de segmento no válido \_**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



El sistema detectó un número de segmento que no era correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR \_ ordinal no válido \_**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**el ERROR \_ ya \_ existe**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



No se puede crear un archivo que ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR \_ de \_ número de marca no válido \_**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



La marca pasada no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR \_ SEM \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



No se encontró el nombre del semáforo del sistema especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR \_ de \_ Inicio de CODESEG no válido \_**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR \_ STACKSEG no válido \_**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR \_ de \_ MODULETYPE no válido**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR \_ de \_ firma exe no válida \_**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



No se puede ejecutar %1 en modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR \_ exe \_ marcado como \_ no válido**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR \_ de \_ formato exe incorrecto \_**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 no es una aplicación Win32 válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Los \_ datos iterados de error \_ \_ superan \_ 64k**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR \_ MINALLOCSIZE no válido \_**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR \_ DYNLINK \_ del \_ anillo no válido \_**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



El sistema operativo no puede ejecutar este programa de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR \_ IOPL \_ no \_ habilitado**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



El sistema operativo no está configurado actualmente para ejecutar esta aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR \_ SEGDPL no válido \_**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**El ERROR \_ AUTODATASEG \_ supera \_ 64k**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



El sistema operativo no puede ejecutar este programa de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**El ERROR \_ RING2SEG \_ debe \_ ser \_ movible**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



El segmento de código no puede ser mayor o igual que 64K.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR \_ reloc \_ cadena \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR \_ INFLOOP \_ en \_ la \_ cadena reloc**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR \_ ENVVAR \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



El sistema no encontró la opción de entorno que se especificó.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR \_ sin \_ señal \_ enviada**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Ningún proceso en el subárbol de comandos tiene un controlador de señales.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR \_ filename \_ EXCED \_ intervalo**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



El nombre de archivo o la extensión es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR \_ \_ en la pila RING2 \_ en \_ uso**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



La pila de anillo 2 está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR de \_ expansión de metadatos \_ \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Los caracteres de nombre de archivo globales, \* o?, se escriben incorrectamente o se han especificado demasiados caracteres de nombre de archivo globales.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR \_ de \_ número de señal no válida \_**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



La señal que se está enviando no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR de \_ subproceso \_ 1 \_ inactivo**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



No se puede establecer el controlador de señal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR \_ bloqueado**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



El segmento está bloqueado y no se puede reasignar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR \_ demasiados \_ \_ módulos**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Hay demasiados módulos de vínculos dinámicos asociados a este programa o módulo de vínculo dinámico.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_ \_ no se permite el ANIDAMIENTO de errores \_**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



No se pueden anidar llamadas a LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR \_ \_ \_ no coincide el tipo de máquina exe \_**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Esta versión de %1 no es compatible con la versión de Windows que se está ejecutando. Compruebe la información del sistema del equipo y, a continuación, póngase en contacto con el editor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR \_ exe \_ no se puede \_ modificar el \_ \_ binario firmado**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



El archivo de imagen %1 está firmado, no se puede modificar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR \_ exe \_ no se puede \_ modificar el \_ \_ binario con firma segura \_**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



El archivo de imagen %1 está firmado de forma segura, no se puede modificar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**archivo de ERROR \_ \_ desprotegido \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Este archivo está desprotegido o bloqueado para su edición por otro usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR de \_ desprotección \_ necesario**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



El archivo debe desprotegerse antes de guardar los cambios.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR \_ de \_ tipo de archivo incorrecto \_**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Se bloqueó el tipo de archivo que se va a guardar o recuperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**archivo de ERROR \_ \_ demasiado \_ grande**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



El tamaño del archivo supera el límite permitido y no se puede guardar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**formularios de ERROR \_ \_ auth \_ obligatorio**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Acceso denegado. Antes de abrir archivos en esta ubicación, primero debe agregar el sitio web a la lista de sitios de confianza, buscar el sitio web y seleccionar la opción de inicio de sesión automático.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS de ERROR \_ \_ infectado**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



La operación no se completó correctamente porque el archivo contiene un virus o software potencialmente no deseado.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR \_ de \_ eliminación de virus**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Este archivo contiene un virus o software potencialmente no deseado y no se puede abrir. Debido a la naturaleza de este virus o software potencialmente no deseado, el archivo se ha quitado de esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_canalización de errores \_ local**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



La canalización es local.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR \_ de \_ Canalización incorrecta**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



El estado de la canalización no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**\_canalización de errores \_ ocupada**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Todas las instancias de canalización están ocupadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR \_ sin \_ datos**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



La canalización se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**\_canalización de errores \_ no \_ conectada**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



No hay ningún proceso en el otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ más \_ datos**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR de \_ VC \_ desconectado**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



Se canceló la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR \_ de \_ nombre EA no válido \_**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



El nombre del atributo extendido especificado no era válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**lista de errores de \_ EA \_ \_ incoherente**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Los atributos extendidos son incoherentes.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_tiempo de espera agotado**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Se agotó el tiempo de espera de la operación de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_no hay \_ más \_ elementos de error**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



No más datos disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_no se puede copiar el error \_**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



No se pueden usar las funciones de copia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**directorio de errores \_**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



El nombre del directorio no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR \_ de \_ echará de EAS \_**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Los atributos extendidos no caben en el búfer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**el \_ archivo EA de error \_ \_ está dañado**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



El archivo de atributo extendido del sistema de archivos montado está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR \_ de \_ tabla EA \_ completa**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



El archivo de tabla de atributos extendidos está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR \_ de \_ identificador EA no válido \_**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



El identificador de atributo extendido especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR \_ EAS \_ no \_ compatible**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



El sistema de archivos montado no admite atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**no se pudo tener el \_ \_ propietario**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Intento de liberar la exclusión mutua que no es propiedad del autor de la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR \_ demasiadas \_ \_ publicaciones**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Se han realizado demasiadas publicaciones en un semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR \_ de \_ copia parcial**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Solo parte de una solicitud de ReadProcessMemory o WriteProcessMemory se ha completado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR de \_ bloqueo oportunista \_ no \_ concedido**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Se denegó la solicitud de bloqueo oportunista.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR \_ de \_ Protocolo de bloqueo oportunista no válido \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



El sistema recibió una confirmación de bloqueo oportunista no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**el disco de ERROR está \_ \_ demasiado \_ fragmentado**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



El volumen está demasiado fragmentado para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR de \_ eliminación \_ pendiente**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



No se puede abrir el archivo porque está en proceso de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR \_ incompatible \_ con \_ la \_ \_ configuración de \_ registro de nombre corto global \_**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



No se puede cambiar la configuración de nombre corto en este volumen debido a la configuración del registro global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nombres cortos \_ \_ de error no \_ habilitados \_ en el \_ volumen**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Los nombres cortos no están habilitados en este volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**el \_ flujo de seguridad de error \_ \_ no es \_ coherente**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



El flujo de seguridad para el volumen especificado se encuentra en un estado incoherente. Ejecute CHKDSK en el volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR \_ de \_ intervalo de bloqueo no válido \_**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



No se puede procesar una operación de bloqueo de archivo solicitada debido a un intervalo de bytes no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**subsistema de imagen de ERROR \_ \_ \_ no \_ presente**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



El subsistema necesario para admitir el tipo de imagen no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notificación de ERROR \_ \_ \_ ya \_ definido**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



El archivo especificado ya tiene asociado un GUID de notificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR \_ de \_ controlador de excepciones no válido \_**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Se ha detectado una rutina del controlador de excepciones no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR \_ de \_ privilegios duplicados**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Se especificaron privilegios duplicados para el token.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR: \_ no se \_ \_ procesaron intervalos**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



No se pudo procesar ningún intervalo para la operación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR \_ no \_ permitido \_ en \_ el \_ archivo del sistema**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



No se permite la operación en un archivo interno del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR \_ de \_ recursos de disco \_ agotados**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Se han agotado los recursos físicos de este disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR \_ de \_ token no válido**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



El token que representa los datos no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**\_no se \_ admite la característica de dispositivo de error \_ \_**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



El dispositivo no admite la característica de comandos.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**\_ \_ \_ no \_ se encontró el error Mr MID**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



El sistema no encuentra el texto del mensaje para el número de mensaje 0x %1 en el archivo de mensaje de %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ \_ no \_ se encontró el ámbito de error**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



No se encontró el ámbito especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR \_ sin definir \_ ámbito**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



La Directiva de acceso central especificada no está definida en el equipo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR \_ de \_ Cap no válido**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



La Directiva de acceso central obtenida de Active Directory no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR de \_ dispositivo \_ inaccesible**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



El dispositivo está inaccesible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR de \_ dispositivo \_ sin \_ recursos**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



El dispositivo de destino no tiene suficientes recursos para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**error \_ de \_ suma de comprobación de datos de error \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Se produjo un error de suma de comprobación de integridad de datos. Los datos de la secuencia de archivo están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR de la \_ \_ \_ operación EA \_ de kernel intermezclado**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Se intentó modificar un KERNEL y un atributo extendido normal (EA) en la misma operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_no se \_ admite el \_ recorte de nivel de \_ archivo \_ de errores**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



El dispositivo no admite el recorte en el nivel de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**infracción de alineación de desplazamiento de ERROR \_ \_ \_**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



El comando especificó un desplazamiento de datos que no se alinea con la granularidad o alineación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR \_ \_ de campo no válido \_ en la \_ lista de parámetros \_**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



El comando especificó un campo no válido en su lista de parámetros.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operación \_ de error en \_ curso**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Una operación está actualmente en curso con el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR \_ de \_ ruta de acceso de dispositivo incorrecta \_**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Se intentó enviar el comando a través de una ruta de acceso no válida al dispositivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR \_ demasiados \_ \_ descriptores**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



El comando especificó un número de descriptores que superó el máximo admitido por el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR al \_ limpiar los \_ datos \_ deshabilitados**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



La limpieza está deshabilitada en el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**no se pudo \_ \_ almacenar el almacenamiento redundante \_**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



El dispositivo de almacenamiento no proporciona redundancia.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_no se \_ admite el archivo residente de \_ errores \_**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



No se admite una operación en un archivo residente.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**\_no se \_ admite el archivo comprimido de \_ errores \_**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



No se admite una operación en un archivo comprimido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_no se \_ \_ admite el directorio de errores**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



No se admite una operación en un directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR \_ al \_ leer \_ la \_ copia**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



No se pudo leer la copia especificada de los datos solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR de ERROR de \_ \_ reinicio de no acción \_**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



No se realizó ninguna acción ya que es necesario reiniciar el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR \_ de \_ apagado**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



No se pudo realizar la operación de cierre.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR \_ de \_ reinicio**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Error en la operación de reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**se \_ alcanzó el número máximo de sesiones de error \_ \_**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Se ha alcanzado el número máximo de sesiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**el \_ modo de subproceso de error \_ \_ ya está \_ en segundo plano**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



El subproceso ya está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_modo de subproceso de error \_ \_ no \_ en segundo plano**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



El subproceso no está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**el \_ modo de proceso de error \_ \_ ya está \_ en segundo plano**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



El proceso ya está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**modo de proceso de ERROR \_ \_ \_ no \_ fondo**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



El proceso no está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR \_ de \_ dirección no válida**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Intento de obtener acceso a una dirección no válida.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>WinError. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




