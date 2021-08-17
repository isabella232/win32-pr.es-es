---
description: Describe los códigos de error 0-499 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Códigos de error del sistema (0-499) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: a9eddec2baf098f62bb1c0ad88e632360807e7f3fd0ea045f2565587f13e93a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405654"
---
# <a name="system-error-codes-0-499"></a>Códigos de error del sistema (0-499)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se describen [los códigos de error del](system-error-codes.md) sistema (errores 0 a 499). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR \_ CORRECTO**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



La operación se ha completado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR \_ FUNCIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Función incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



El sistema no encuentra el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**RUTA DE \_ ACCESO DE ERROR NO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



el sistema no encuentra la ruta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR \_ \_ DEMASIADOS \_ ARCHIVOS ABIERTOS \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



El sistema no puede abrir el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR \_ DE ACCESO \_ DENEGADO**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Acceso denegado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



El identificador no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR \_ DE LA \_ PAPELERA**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Los bloques de control de almacenamiento se destruyeron.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



No hay recursos de memoria suficientes disponibles para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR \_ BLOQUE NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



La dirección del bloque de control de almacenamiento no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR \_ ENTORNO \_ DE ERROR**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



El entorno es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**FORMATO \_ DE ERROR NO \_ CORRECTO**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Se ha intentado cargar un programa con un formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR \_ ACCESO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



El código de acceso no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR \_ DATOS NO \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Los datos no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



No hay suficiente almacenamiento disponible para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR \_ UNIDAD NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



El sistema no puede encontrar la unidad especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR \_ DIRECTORIO \_ ACTUAL**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



No se puede quitar el directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR \_ NO ES EL MISMO \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



El sistema no puede mover el archivo a otra unidad de disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR \_ NO \_ MÁS \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



No hay más archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**PROTECCIÓN DE \_ ESCRITURA \_ DE ERROR**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



El medio está protegido por escritura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**UNIDAD \_ DE ERROR NO ESTÁ \_ BIEN**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



El sistema no puede encontrar el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR \_ NO \_ LISTO**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



El dispositivo no está listo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR \_ BAD \_ (COMANDO)**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



El dispositivo no reconoce el comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Error de datos (comprobación de redundancia cíclica).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR \_ BAD \_ LENGTH**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



El programa emitió un comando, pero la longitud del comando es incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR \_ SEEK**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



La unidad no puede encontrar un área o un seguimiento específicos en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR \_ NOT \_ DOS \_ DISK**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



No se puede acceder al disco o a la unidad de disco especificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR \_ SECTOR \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



La unidad no encuentra el sector solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR \_ FUERA \_ DE \_ PAPEL**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



La impresora se ha quedado sin papel.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR \_ AL ESCRIBIR \_ ERROR**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



El sistema no puede escribir en el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR \_ DE LECTURA DE \_ ERROR**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



El sistema no puede leer desde el dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR \_ DE GEN \_**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Un dispositivo conectado al sistema no funciona.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**INFRACCIÓN DE \_ USO COMPARTIDO \_ DE ERRORES**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



El proceso no puede obtener acceso al archivo porque otro proceso lo está utilizando.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**INFRACCIÓN \_ DE BLOQUEO \_ DE ERROR**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



El proceso no puede obtener acceso al archivo porque otro proceso ha bloqueado una parte de este.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR \_ DE DISCO \_ INCORRECTO**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



El diskette incorrecto está en la unidad. Inserte %2 (Número de serie de volumen: %3) en la unidad %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**SE HA \_ SUPERADO EL BÚFER DE USO COMPARTIDO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Demasiados archivos abiertos para compartir.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**EOF \_ DEL \_ IDENTIFICADOR DE ERROR**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Se alcanzó el final del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**DISCO \_ DE IDENTIFICADOR DE ERRORES \_ \_ LLENO**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



El disco está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ NO \_ ADMITIDO**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



No se admite la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR \_ REM \_ NOT \_ LIST**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows puede encontrar la ruta de acceso de red. Compruebe que la ruta de acceso de red es correcta y que el equipo de destino no está ocupado ni desactivado. Si Windows puede encontrar la ruta de acceso de red, póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR \_ DUP \_ NAME**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



No estaba conectado porque existe un nombre duplicado en la red. Si se une a un dominio, vaya a Sistema en Panel de control cambiar el nombre del equipo e inténtelo de nuevo. Si se une a un grupo de trabajo, elija otro nombre de grupo de trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR \_ BAD \_ NETPATH**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



No se ha encontrado la ruta de acceso de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR \_ NETWORK \_ BUSY**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



La red está ocupada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR \_ DEV \_ NOT \_ EXIST**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



El recurso o dispositivo de red especificado ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR \_ \_ DEMASIADOS \_ CMD**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



Se ha alcanzado el límite de comandos del BIOS de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR \_ ADAP \_ HDW \_ ERR**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Error de hardware del adaptador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR \_ BAD \_ NET \_ RESP**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



El servidor especificado no puede ejecutar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR \_ UNEXP \_ NET \_ ERR**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Se produjo un error de red inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR \_ BAD \_ REM \_ ADAP**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



El adaptador remoto no es compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR \_ PRINTQ \_ FULL**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



La cola de impresora está llena.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR \_ NO HAY ESPACIO DE \_ COLA \_**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



El espacio para almacenar el archivo en espera de impresión no está disponible en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR \_ DE \_ IMPRESIÓN CANCELADA**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Se eliminó el archivo que espera a ser impreso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR \_ NETNAME \_ DELETED**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



El nombre de red especificado ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR \_ ACCESO DE RED \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Se deniega el acceso a la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR \_ TIPO \_ DEV NO ES \_ BUENO**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



El tipo de recurso de red no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR \_ NOMBRE DE RED NO ESTÁ \_ \_ BIEN**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



No se encuentra el nombre de red especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR \_ \_ DEMASIADOS \_ NOMBRES**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



Se superó el límite de nombres de la tarjeta del adaptador de red del equipo local.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR \_ \_ DEMASIADOS \_ SESS**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



Se superó el límite de sesión del BIOS de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR \_ AL COMPARTIR EN \_ PAUSA**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



El servidor remoto se ha pausado o se está iniciando.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR \_ REQ \_ NOT \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



No se pueden realizar más conexiones a este equipo remoto en este momento porque ya hay tantas conexiones como el equipo pueda aceptar.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR \_ REDIR \_ PAUSED**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



Se ha pausado la impresora o el dispositivo de disco especificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ARCHIVO DE \_ ERROR \_ EXISTE**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



El archivo ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR \_ NO SE PUEDE \_ REALIZAR**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



No se puede crear el directorio o archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR \_ FAIL \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Error en INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR \_ FUERA \_ DE \_ ESTRUCTURAS**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Storage para procesar esta solicitud no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR \_ YA \_ ASIGNADO**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



El nombre del dispositivo local ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR \_ CONTRASEÑA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



La contraseña de red especificada no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



El parámetro no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR \_ NET \_ WRITE \_ FAULT**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Se produjo un error de escritura en la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR \_ NO \_ HAY RANURAS PROC \_**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



El sistema no puede iniciar otro proceso en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR \_ \_ DEMASIADOS \_ SEMÁFOROS**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



No se puede crear otro semáforo del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR \_ EXCL \_ SEM \_ YA EN \_ PROPIEDAD**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



El semáforo exclusivo pertenece a otro proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR \_ SEM \_ IS \_ SET**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



El semáforo está establecido y no se puede cerrar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR \_ \_ DEMASIADAS \_ SOLICITUDES DE SEM \_**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



No se puede volver a establecer el semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR NO \_ VÁLIDO EN TIEMPO DE \_ \_ \_ INTERRUPCIÓN**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



No se pueden solicitar semáforos exclusivos en tiempo de interrupción.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR \_ DEL PROPIETARIO DEL SEM QUE SE \_ \_ PRODUJO**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



Ha finalizado la propiedad anterior de este semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR \_ SEM \_ USER \_ LIMIT**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Inserte el diskette de la unidad %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR \_ DE CAMBIO DE \_ DISCO**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



El programa se detuvo porque no se insertó un diskette alternativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**UNIDAD DE ERROR \_ \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



El disco está en uso o bloqueado por otro proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR \_ DE CANALIZACIÓN \_ ROTA**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



Se ha finalizado la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR \_ AL ABRIR \_ ERROR**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



El sistema no puede abrir el dispositivo o el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR \_ BUFFER \_ OVERFLOW**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



El nombre de archivo es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR \_ DISK \_ FULL**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



There is not enough space on the disk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR \_ NO \_ MÁS \_ IDENTIFICADORES DE \_ BÚSQUEDA**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



No hay más identificadores de archivo internos disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR \_ IDENTIFICADOR DE DESTINO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



El identificador de archivo interno de destino es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR \_ CATEGORÍA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



La llamada IOCTL realizada por el programa de aplicación no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR \_ INVALID \_ VERIFY \_ SWITCH**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



El valor del parámetro de modificador verify-on-write no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR \_ NIVEL DE CONTROLADOR NO \_ \_ ADECUADO**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



El sistema no admite el comando solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**LLAMADA \_ DE ERROR NO \_ \_ IMPLEMENTADA**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Esta función no se admite en este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR \_ SEM \_ TIMEOUT**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



El período de tiempo de espera del semáforo ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ BÚFER \_ INSUFICIENTE**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



El área de datos pasada a una llamada del sistema es demasiado pequeña.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR \_ NOMBRE NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



La sintaxis de nombre de archivo, nombre de directorio o etiqueta de volumen es incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR \_ NIVEL NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



El nivel de llamada del sistema no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR \_ NO HAY ETIQUETA DE \_ \_ VOLUMEN**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



El disco no tiene ninguna etiqueta de volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR \_ MOD \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



No se pudo encontrar el módulo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR \_ PROC \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



No se encontró el procedimiento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR \_ WAIT \_ NO \_ CHILDREN**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



No hay ningún proceso secundario que esperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR \_ SECUNDARIO \_ NO \_ COMPLETADO**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



La aplicación %1 no se puede ejecutar en modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**IDENTIFICADOR \_ DE ACCESO DIRECTO DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Intente usar un identificador de archivo en una partición de disco abierto para una operación que no sea la E/S de disco sin formato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**BÚSQUEDA \_ NEGATIVA \_ DE ERROR**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Se intentó mover el puntero de archivo antes del principio del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**BÚSQUEDA \_ DE ERRORES EN EL \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



El puntero de archivo no se puede establecer en el dispositivo o archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR \_ ES \_ JOIN \_ TARGET**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



No se puede usar un comando JOIN o SUBST para una unidad que contenga unidades previamente unidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR \_ SE \_ UNE**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Se intentó usar un comando JOIN o SUBST en una unidad que ya se ha unido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR \_ IS \_ SUBSTED**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Se intentó usar un comando JOIN o SUBST en una unidad que ya se ha sustituido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR \_ NO \_ UNIDO**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



El sistema intentó eliminar la combinación de una unidad que no está unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR \_ NO \_ SUBSTED**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



El sistema intentó eliminar la sustitución de una unidad que no se sustituye.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR \_ JOIN \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



El sistema intentó unir una unidad a un directorio en una unidad unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR \_ SUBST \_ A \_ SUBST**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



El sistema intentó sustituir una unidad a un directorio en una unidad sustituta.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR \_ JOIN \_ TO \_ SUBST**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



El sistema intentó unir una unidad a un directorio en una unidad sustituta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR \_ SUBST \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



El sistema intentó subserer una unidad a un directorio en una unidad unida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**UNIDAD \_ OCUPADA DE \_ ERROR**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



En este momento, el sistema no puede realizar una operación JOIN o SUBST.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR \_ EN LA MISMA \_ UNIDAD**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



El sistema no puede unir ni sustituir una unidad a o a un directorio de la misma unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR \_ DIR \_ NOT \_ ROOT**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



El directorio no es un subdirectorio del directorio raíz.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR \_ DIR \_ NOT \_ EMPTY**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



El directorio no está vacío.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR \_ IS \_ SUBST \_ PATH**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



La ruta de acceso especificada se usa en un sustituto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR ES \_ RUTA DE ACCESO DE \_ \_ COMBINACIÓN**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



No hay suficientes recursos disponibles para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**RUTA DE \_ ACCESO DE ERROR \_ OCUPADA**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



La ruta de acceso especificada no se puede usar en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR \_ ES EL DESTINO DE \_ \_ SUBST**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Se intentó unir o sustituir una unidad para la que un directorio de la unidad es el destino de un sustituto anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**SEGUIMIENTO \_ DEL SISTEMA DE \_ ERRORES**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



La información de seguimiento del sistema no se especificó en el CONFIG.SYS o no se permite el seguimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**RECUENTO DE \_ EVENTOS NO \_ VÁLIDOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



El número de eventos de semáforo especificados para DosMuxSemWait no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR \_ \_ DEMASIADOS \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait no se ejecutó; ya hay demasiados semáforos establecidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR \_ FORMATO DE LISTA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



La lista DosMuxSemWait no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ETIQUETA \_ DE ERROR DEMASIADO \_ \_ LARGA**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



La etiqueta de volumen especificada supera el límite de caracteres de etiqueta del sistema de archivos de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR \_ \_ \_ DEMASIADAS TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



No se puede crear otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**SEÑAL \_ DE ERROR \_ RECHAZADA**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



El proceso de destinatario ha rechazado la señal.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR \_ DESCARTADO**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



El segmento ya se ha descartado y no se puede bloquear.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR \_ NO \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



El segmento ya está desbloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR \_ BAD \_ THREADID \_ ADDR**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



La dirección del identificador del subproceso no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ARGUMENTOS \_ \_ DE ERROR NO VÁLIDOS**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Uno o varios argumentos no son correctos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR \_ BAD \_ PATHNAME**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



La ruta de acceso especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**SEÑAL \_ DE ERROR \_ PENDIENTE**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Ya hay una señal pendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR \_ MAX \_ THRDS \_ REACHED**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



No se pueden crear más subprocesos en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR \_ DE BLOQUEO \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



No se puede bloquear una región de un archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR \_ OCUPADO**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



El recurso solicitado está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**COMPATIBILIDAD \_ CON \_ DISPOSITIVOS DE ERROR EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



La detección de compatibilidad con comandos del dispositivo está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR \_ CANCELAR \_ INFRACCIÓN**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



No había una solicitud de bloqueo pendiente para la región de cancelación proporcionada.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**NO SE \_ \_ ADMITEN BLOQUEOS \_ ATÓMICOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



El sistema de archivos no admite cambios atómicos en el tipo de bloqueo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR \_ NÚMERO DE SEGMENTO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



El sistema detectó un número de segmento que no era correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR \_ \_ ORDINAL NO VÁLIDO**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**EL ERROR \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



No se puede crear un archivo que ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR \_ NÚMERO DE MARCA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



La marca pasada no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR \_ SEM \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



No se encontró el nombre del semáforo del sistema especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR \_ CÓDIGOS DE INICIO NO \_ \_ VÁLIDOSEG**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR \_ \_ STACKSEG NO VÁLIDO**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR \_ \_ MODULETYPE NO VÁLIDO**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR \_ FIRMA EXE NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



No se puede ejecutar %1 en modo Win32.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR \_ EXE MARCADO COMO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**FORMATO \_ EXE \_ CON ERRORES \_**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 no es una aplicación Win32 válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**LOS \_ DATOS \_ ITERADOS DE ERROR SUPERAN LOS \_ \_ 64 000**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR \_ \_ LOCLOCSIZE NO VÁLIDO**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR \_ DYNLINK \_ DESDE UN ANILLO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



El sistema operativo no puede ejecutar este programa de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR \_ IOPL \_ NO \_ HABILITADO**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



El sistema operativo no está configurado actualmente para ejecutar esta aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR \_ \_ SEGDPL NO VÁLIDO**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**EL \_ ERROR AUTODATASEG \_ SUPERA LOS \_ 64 000**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



El sistema operativo no puede ejecutar este programa de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**EL \_ ERROR RING2SEG \_ DEBE SER \_ \_ MOVABLE**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



El segmento de código no puede ser mayor o igual que 64 K.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR \_ RELOC \_ CHAIN \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR \_ INFLOOP \_ EN LA CADENA \_ RELOC \_**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



El sistema operativo no puede ejecutar %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR \_ ENVVAR \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



El sistema no encontró la opción de entorno especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR \_ SIN \_ SEÑAL \_ ENVIADA**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Ningún proceso del subárbol de comandos tiene un controlador de señal.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**INTERVALO \_ \_ EXCED DE NOMBRE DE \_ ARCHIVO DE ERROR**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



El nombre de archivo o la extensión es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**PILA \_ RING2 \_ DE ERROR EN \_ \_ USO**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



La pila de anillo 2 está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR \_ META \_ EXPANSION \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Los caracteres globales del nombre de archivo, o ?, se especifican incorrectamente o se especifican demasiados caracteres de nombre \* de archivo globales.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR \_ NÚMERO DE SEÑAL NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



La señal que se está publicndo no es correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**SUBPROCESO DE ERROR \_ \_ 1 \_ INACTIVO**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



No se puede establecer el controlador de señal.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



El segmento está bloqueado y no se puede reasignar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR \_ \_ DEMASIADOS \_ MÓDULOS**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Hay demasiados módulos de vínculo dinámico asociados a este programa o módulo de vínculo dinámico.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR \_ DE ANIDAMIENTO \_ NO \_ PERMITIDO**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



No se pueden anidar llamadas a LoadModule.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR: \_ ERROR DE COINCIDENCIA DEL TIPO DE MÁQUINA \_ \_ \_ EXE**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Esta versión de %1 no es compatible con la versión de Windows está ejecutando. Compruebe la información del sistema del equipo y, a continuación, póngase en contacto con el publicador de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR \_ EXE \_ CANNOT \_ MODIFY \_ SIGNED \_ BINARY**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



El archivo de imagen %1 está firmado, no se puede modificar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR \_ EXE \_ CANNOT \_ MODIFY \_ STRONG \_ SIGNED \_ BINARY**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



El archivo de imagen %1 es fuertemente firmado, no se puede modificar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ARCHIVO \_ DE ERROR \_ DESPROTEGIENDO \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Otro usuario desprotegía o bloquea este archivo para su edición.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR \_ CHECKOUT \_ REQUIRED**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



El archivo debe desprotegrse antes de guardar los cambios.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**TIPO \_ DE ARCHIVO CON \_ ERROR \_**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



El tipo de archivo que se guarda o recupera se ha bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ARCHIVO \_ DE ERROR DEMASIADO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



El tamaño del archivo supera el límite permitido y no se puede guardar.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**SE REQUIERE \_ \_ AUTENTICACIÓN DE FORMULARIOS \_ DE ERROR**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Acceso denegado. Antes de abrir los archivos en esta ubicación, primero debe agregar el sitio web a la lista de sitios de confianza, ir al sitio web y seleccionar la opción para iniciar sesión automáticamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS \_ DE ERROR \_ INFECTADO**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



La operación no se ha completado correctamente porque el archivo contiene un virus o software potencialmente no deseado.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR \_ VIRUS \_ ELIMINADO**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Este archivo contiene un virus o software potencialmente no deseado y no se puede abrir. Debido a la naturaleza de este virus o software potencialmente no deseado, el archivo se ha quitado de esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**CANALIZACIÓN DE \_ \_ ERROR LOCAL**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



La canalización es local.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**CANALIZACIÓN \_ DE ERROR \_**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



El estado de canalización no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**CANALIZACIÓN DE \_ ERRORES \_ OCUPADA**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Todas las instancias de canalización están ocupadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR \_ SIN \_ DATOS**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



La canalización se está cierrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**CANALIZACIÓN DE \_ ERROR \_ NO \_ CONECTADA**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



No hay ningún proceso en el otro extremo de la canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ MÁS \_ DATOS**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR \_ VC \_ DISCONNECTED**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



Se canceló la sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR \_ NOMBRE DE EA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



El nombre de atributo extendido especificado no era válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR \_ EA \_ LIST \_ INCONSISTENT**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Los atributos extendidos son incoherentes.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**TIEMPO DE \_ ESPERA AGOTADO**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Se agotó el tiempo de espera de la operación de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR \_ NO \_ MÁS \_ ELEMENTOS**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



No más datos disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR \_ NO SE PUEDE \_ COPIAR**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



No se pueden usar las funciones de copia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**DIRECTORIO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



El nombre del directorio no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR \_ EAS \_ DIDNT \_ FIT**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Los atributos extendidos no caben en el búfer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR \_ EA \_ FILE \_ CORRUPT**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



El archivo de atributo extendido en el sistema de archivos montado está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR \_ DE TABLA DE EA \_ \_ COMPLETA**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



El archivo de tabla de atributos extendidos está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR \_ IDENTIFICADOR DE EA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



El identificador de atributo extendido especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR \_ NO COMPATIBLE CON EAS \_ \_**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



El sistema de archivos montado no admite atributos extendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR \_ NOT \_ OWNER**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Intente liberar la exclusión mutua que no es propiedad del autor de la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR \_ \_ DEMASIADAS \_ PUBLICACIONES**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Se han realizado demasiadas publicaciones en un semáforo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR \_ COPIA \_ PARCIAL**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Solo se completó una parte de una solicitud ReadProcessMemory o WriteProcessMemory.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR \_ OPLOCK \_ NO \_ CONCEDIDO**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Se deniega la solicitud oplock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR \_ PROTOCOLO \_ OPLOCK NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



El sistema recibió una confirmación de bloqueo de operación no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**DISCO \_ DE ERROR DEMASIADO \_ \_ FRAGMENTADO**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



El volumen está demasiado fragmentado para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ELIMINACIÓN \_ DE ERRORES \_ PENDIENTE**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



No se puede abrir el archivo porque está en proceso de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR INCOMPATIBLE \_ CON LA CONFIGURACIÓN GLOBAL DEL REGISTRO DE NOMBRES \_ \_ \_ \_ \_ \_ CORTOS**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



La configuración de nombre corto no se puede cambiar en este volumen debido a la configuración del Registro global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**NOMBRES \_ CORTOS DE ERROR NO \_ \_ \_ \_ HABILITADOS EN EL \_ VOLUMEN**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Los nombres cortos no están habilitados en este volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**EL FLUJO \_ DE SEGURIDAD DE ERROR ES \_ \_ \_ INCOHERENTE**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



El flujo de seguridad para el volumen dado está en un estado incoherente. Ejecute CHKDSK en el volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR \_ INTERVALO DE BLOQUEO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



No se puede procesar una operación de bloqueo de archivo solicitada debido a un intervalo de bytes no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**SUBSISTEMA DE \_ IMAGEN DE ERROR NO \_ \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



El subsistema necesario para admitir el tipo de imagen no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID \_ DE NOTIFICACIÓN DE ERRORES YA \_ \_ \_ DEFINIDO**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



El archivo especificado ya tiene asociado un GUID de notificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR \_ CONTROLADOR DE \_ EXCEPCIONES NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Se ha detectado una rutina de controlador de excepciones no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**PRIVILEGIOS \_ \_ DUPLICADOS DE ERROR**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Se especificaron privilegios duplicados para el token.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR \_ SIN \_ INTERVALOS \_ PROCESADOS**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



No se pudo procesar ningún intervalo para la operación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR \_ NO PERMITIDO EN EL ARCHIVO DEL \_ \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



No se permite la operación en un archivo interno del sistema de archivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**RECURSOS DE \_ DISCO \_ DE ERROR \_ AGOTADOS**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Se han agotado los recursos físicos de este disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR \_ TOKEN NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



El token que representa los datos no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**NO SE \_ ADMITE LA CARACTERÍSTICA DE DISPOSITIVO DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



El dispositivo no admite la característica de comandos.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR \_ MR \_ MID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



El sistema no encuentra el texto del mensaje para el número de mensaje 0x%1 en el archivo de mensaje para %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**NO SE \_ ENCONTRÓ EL ÁMBITO DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



No se encontró el ámbito especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ÁMBITO \_ SIN DEFINIR DE \_ ERROR**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



La directiva de acceso central especificada no está definida en la máquina de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR \_ LÍMITE NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



La directiva de acceso central obtenida de Active Directory no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**DISPOSITIVO DE ERROR \_ \_ INACCESIBLE**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



El dispositivo está inaccesible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR \_ DISPOSITIVO \_ SIN \_ RECURSOS**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



El dispositivo de destino no tiene recursos suficientes para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR \_ DE SUMA DE COMPROBACIÓN DE DATOS DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Error de suma de comprobación de integridad de datos. Los datos del flujo de archivos están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR \_ INTERMIXED \_ KERNEL \_ EA \_ OPERATION**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Se intentó modificar un kernel y un atributo extendido normal (EA) en la misma operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR \_ FILE \_ LEVEL \_ TRIM \_ NOT \_ SUPPORTED**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



El dispositivo no admite TRIM en el nivel de archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**INFRACCIÓN DE \_ \_ ALINEACIÓN DE DESPLAZAMIENTO \_ DE ERROR**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



El comando especificó un desplazamiento de datos que no se alinea con la granularidad o alineación del dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR \_ CAMPO NO VÁLIDO EN LA LISTA DE \_ \_ \_ \_ PARÁMETROS**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



El comando especificó un campo no válido en su lista de parámetros.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**OPERACIÓN \_ DE ERROR EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Una operación está actualmente en curso con el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**RUTA DE \_ ACCESO DEL DISPOSITIVO CON \_ \_ ERROR**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Se intentó enviar el comando a través de una ruta de acceso no válida al dispositivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR \_ \_ DEMASIADOS \_ DESCRIPTORES**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



El comando especificó una serie de descriptores que superaron el máximo admitido por el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR \_ AL LIMPIAR LOS DATOS \_ \_ DESHABILITADOS**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



La limpieza está deshabilitada en el archivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR \_ ALMACENAMIENTO \_ NO \_ REDUNDANTE**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



El dispositivo de almacenamiento no proporciona redundancia.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**NO \_ SE ADMITE EL ARCHIVO DE RESIDENTES DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



No se admite una operación en un archivo residentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ARCHIVO \_ COMPRIMIDO DE ERROR NO \_ \_ \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



No se admite una operación en un archivo comprimido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**NO \_ SE ADMITE EL DIRECTORIO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



No se admite una operación en un directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR \_ NO LEÍDO DE LA \_ \_ \_ COPIA**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



No se pudo leer la copia especificada de los datos solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR \_ AL \_ REINICIAR NOACTION \_**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



No se ha realizado ninguna acción porque se requiere un reinicio del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR \_ AL CERRAR \_**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



Error en la operación de apagado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR \_ AL REINICIAR \_**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Error en la operación de reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**SE \_ ALCANZÓ EL NÚMERO \_ MÁXIMO DE SESIONES DE \_ ERROR**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Se ha alcanzado el número máximo de sesiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**MODO DE \_ SUBPROCESO DE ERROR YA EN SEGUNDO \_ \_ \_ PLANO**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



El subproceso ya está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**MODO DE \_ SUBPROCESO DE ERROR NO EN SEGUNDO \_ \_ \_ PLANO**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



El subproceso no está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**MODO DE \_ PROCESO DE ERROR YA EN SEGUNDO \_ \_ \_ PLANO**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



El proceso ya está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**MODO DE \_ PROCESO DE ERROR NO EN SEGUNDO \_ \_ \_ PLANO**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



El proceso no está en modo de procesamiento en segundo plano.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR \_ DIRECCIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Intente acceder a una dirección no válida.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>WinError.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




