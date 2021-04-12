---
description: Describe los códigos de error 1300-1699 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Códigos de error del sistema (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496241"
---
# <a name="system-error-codes-1300-1699"></a>Códigos de error del sistema (1300-1699)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 1300 a 1699. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**\_no se \_ \_ ha asignado ningún error**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



No todos los privilegios o grupos a los que se hace referencia se asignan al autor de la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR \_ algunos \_ no \_ asignados**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



No se ha realizado ninguna asignación entre los nombres de cuenta y los ID. de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR: \_ no hay \_ cuotas \_ para la \_ cuenta**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



No se ha establecido específicamente ningún límite de cuota del sistema para esta cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR en la \_ \_ clave de sesión de usuario local \_ \_**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



No hay ninguna clave de cifrado disponible. Se devolvió una clave de cifrado conocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR \_ : \_ contraseña de LM nula \_**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



La contraseña es demasiado compleja para convertirse en una contraseña de administrador de LAN. La contraseña del administrador de LAN devuelta es una cadena **nula** .


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR \_ de \_ revisión desconocida**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Se desconoce el nivel de revisión.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR \_ de \_ coincidencia de revisión**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Indica que dos niveles de revisión son incompatibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR \_ de \_ propietario no válido**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



No se puede asignar este identificador de seguridad como propietario de este objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR \_ de \_ grupo principal no válido \_**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Este identificador de seguridad no se puede asignar como el grupo principal de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR: \_ no hay \_ token de suplantación \_**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Se ha intentado realizar una operación en un token de suplantación por parte de un subproceso que actualmente no suplanta a un cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR no se pudo \_ \_ deshabilitar \_ obligatorio**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Es posible que el grupo no esté deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR: \_ no hay \_ servidores de inicio de sesión \_**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Actualmente no hay ningún servidor de inicio de sesión disponible para atender la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR no se ha podido \_ \_ \_ iniciar \_ sesión**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Una sesión de inicio especificada no existe. Es posible que ya se haya terminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**NO se ha podido obtener \_ \_ dicho \_ privilegio**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



No existe un privilegio especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**\_no se \_ \_ mantiene el privilegio de error**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



El cliente no dispone de un privilegio requerido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR \_ de \_ nombre de cuenta no válido \_**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



El nombre proporcionado no es un nombre de cuenta formado correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**existe un ERROR de \_ usuario \_**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



La cuenta especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**NO se ha podido \_ \_ este \_ usuario**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



La cuenta especificada no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**\_existe un grupo de errores \_**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



El grupo especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**NO se ha podido \_ \_ este \_ Grupo**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



El grupo especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_miembro \_ de error en \_ Grupo**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



O bien la cuenta de usuario especificada ya es miembro del grupo especificado o el grupo especificado no se puede eliminar porque contiene un miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**el \_ miembro \_ de error no está \_ en el \_ Grupo**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



La cuenta de usuario especificada no es miembro de la cuenta de grupo especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**último ERROR de \_ \_ Administrador**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Esta operación no está permitida, ya que podría dar lugar a que se deshabilitara, eliminara o no se pudiera iniciar sesión en una cuenta de administración.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR \_ de \_ contraseña incorrecta**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado como contraseña actual no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR \_ de \_ contraseña con formato incorrecto \_**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado para la nueva contraseña contiene valores que no se permiten en las contraseñas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restricción de contraseña de error \_**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado para la nueva contraseña no cumple los requisitos de longitud, complejidad o historial del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR de \_ Inicio de sesión \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



El nombre de usuario o la contraseña son incorrectos.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restricción de cuenta de error \_**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Las restricciones de cuenta impiden que este usuario inicie sesión. Por ejemplo: no se permiten contraseñas en blanco, las horas de inicio de sesión están limitadas o se ha aplicado una restricción de directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR de \_ horas de inicio de sesión no válidas \_ \_**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Su cuenta tiene restricciones de tiempo que le evitan iniciar sesión en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR \_ de \_ estación de trabajo no válida**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Este usuario no tiene permiso para iniciar sesión en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**contraseña de ERROR \_ \_ expirada**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



La contraseña de esta cuenta ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**cuenta de ERROR \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Este usuario no puede iniciar sesión porque esta cuenta está deshabilitada actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR \_ ninguno \_ asignado**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



No se realizó ninguna asignación entre los nombres de cuenta y los ID. de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR \_ demasiados de \_ \_ LUID \_ solicitadas**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Se solicitaron demasiados identificadores de usuario local (LUID) al mismo tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR de \_ LUID \_ agotado**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



No hay más identificadores de usuario locales (LUID) disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR \_ de \_ \_ subentidad no válida**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



La parte del subautor de un identificador de seguridad no es válida para este uso concreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR \_ de \_ ACL no válida**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



La estructura de la lista de control de acceso (ACL) no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR \_ de \_ SID no válido**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



La estructura de ID. de seguridad no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR \_ de \_ Descripción de seguridad no válido \_**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



La estructura del descriptor de seguridad no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR \_ en \_ ACL de herencia incorrecta \_**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



No se pudo crear la lista de control de acceso (ACL) o la entrada de control de acceso (ACE) heredada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR de \_ servidor \_ deshabilitado**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



El servidor está deshabilitado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**servidor de errores \_ \_ no \_ deshabilitado**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



El servidor está habilitado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR \_ de \_ autoridad de ID. no válido \_**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



El valor proporcionado era un valor no válido para una autoridad de identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**se \_ \_ \_ ha superado el espacio asignado**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



No hay más memoria disponible para las actualizaciones de información de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR \_ de \_ atributos de grupo no válidos \_**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Los atributos especificados no son válidos o no son compatibles con los atributos del grupo en su conjunto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR \_ de \_ nivel de suplantación incorrecto \_**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



No se ha proporcionado el nivel de representación necesario o el nivel de representación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR no se pudo \_ \_ abrir \_ anónimo**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



No se puede abrir un token de seguridad de nivel anónimo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR \_ de \_ clase de validación incorrecta \_**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



La clase de información de validación solicitada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR \_ de \_ tipo de token incorrecto \_**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



El tipo del token no es apropiado para su intento de uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR: \_ no hay \_ seguridad \_ en el \_ objeto**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



No se puede realizar una operación de seguridad en un objeto que no tiene ninguna seguridad asociada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR: no se \_ \_ puede obtener acceso a la \_ información del dominio \_**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



No se pudo leer la información de configuración del controlador de dominio, ya sea porque la máquina no está disponible o porque se ha denegado el acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR \_ de \_ Estado de servidor no válido \_**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



El servidor de administración de cuentas de seguridad (SAM) o la autoridad de seguridad local (LSA) se encontraba en un estado incorrecto para realizar la operación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR \_ de \_ Estado de dominio no válido \_**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



El estado del dominio era incorrecto para realizar la operación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR \_ de \_ rol de dominio no válido \_**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Esta operación solo se permite para el controlador de dominio principal del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**NO se ha podido \_ \_ este \_ dominio**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



El dominio especificado no existe o no se pudo establecer contacto con él.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**\_existe un dominio de error \_**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



El dominio especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**límite de dominio de ERROR \_ \_ \_ superado**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Se intentó superar el límite en el número de dominios por servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR \_ de \_ base de BD interna \_ dañado**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



No se puede completar la operación solicitada debido a un error grave del medio o a una estructura de datos dañada en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**error \_ interno de error \_**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR \_ genérico \_ no \_ asignado**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Los tipos de acceso genéricos estaban contenidos en una máscara de acceso que ya debe estar asignada a tipos no genéricos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR \_ de \_ formato de descriptor incorrecto \_**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Un descriptor de seguridad no tiene el formato correcto (absoluto o autorelativo).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR en el \_ \_ proceso de inicio de sesión \_**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



La acción solicitada está restringida para su uso por parte de los procesos de inicio de sesión. El proceso de llamada no se ha registrado como un proceso de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**la sesión de inicio de sesión de ERROR \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



No se puede iniciar una nueva sesión de inicio de sesión con un identificador que ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**NO se ha podido \_ \_ este \_ paquete**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Se desconoce un paquete de autenticación especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR \_ de \_ \_ Estado de sesión de inicio de sesión incorrecto \_**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



La sesión de inicio de sesión no se encuentra en un estado coherente con la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**\_colisión de \_ sesión de inicio de sesión con error \_**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



El identificador de la sesión de inicio de sesión ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR \_ de \_ tipo de inicio de sesión no válido \_**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Una solicitud de inicio de sesión contenía un valor de tipo de inicio de sesión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR \_ no se puede \_ Suplantar**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



No se puede suplantar con una canalización con nombre hasta que se hayan leído los datos de esa canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR \_ RXACT \_ Estado no válido \_**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



El estado de la transacción de un subárbol del registro no es compatible con la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR \_ de \_ confirmación \_ RXACT**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Se ha producido un daño interno en la base de datos de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_cuenta especial de error \_**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



No se puede realizar esta operación en cuentas integradas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_grupo especial de error \_**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



No se puede realizar esta operación en este grupo especial integrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR \_ de \_ usuario especial**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



No se puede realizar esta operación en este usuario especial integrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**miembro de ERROR: \_ \_ \_ grupo principal**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



No se puede quitar el usuario de un grupo porque es actualmente el grupo principal del usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**el \_ token \_ de error ya está \_ en \_ uso**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



El token ya se está usando como un token principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**\_no existe \_ este \_ alias**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



El grupo local especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**el \_ miembro \_ de error no está \_ en el \_ alias**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



El nombre de cuenta especificado no es un miembro del grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_miembro \_ de error en \_ alias**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



El nombre de cuenta especificado ya es miembro del grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_existe un alias de error \_**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



El grupo local especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR de \_ Inicio de sesión \_ no \_ concedido**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR \_ demasiados \_ \_ secretos**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Se ha superado el número máximo de secretos que se pueden almacenar en un solo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR de \_ secreto \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



La longitud de un secreto supera la longitud máxima permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**error \_ interno de \_ base de BD \_**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



La base de datos de autoridad de seguridad local contiene una incoherencia interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR \_ demasiados \_ \_ \_ identificadores de contexto**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Durante un intento de inicio de sesión, el contexto de seguridad del usuario ha acumulado demasiados identificadores de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_no se \_ \_ \_ concedió el tipo de inicio de sesión de error**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR \_ de \_ cifrado cruzado de NT \_ \_ requerido**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Es necesaria una contraseña con cifrado cruzado para cambiar la contraseña de un usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**NO se ha podido \_ \_ este \_ miembro**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



No se pudo agregar o quitar un miembro del grupo local porque el miembro no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR \_ de \_ miembro no válido**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



No se pudo agregar un nuevo miembro a un grupo local porque el miembro tiene un tipo de cuenta incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR \_ demasiados \_ \_ SID**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Se han especificado demasiados identificadores de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR \_ de \_ \_ cifrado cruzado LM \_ requerido**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Se necesita una contraseña con cifrado cruzado para cambiar esta contraseña de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR \_ sin \_ herencia**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Indica que una ACL no contiene componentes heredables.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**archivo de ERROR \_ \_ dañado**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



El archivo o directorio está dañado y no se pudo leer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR de \_ disco \_ dañado**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



La estructura del disco está dañada y es ilegible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR \_ sin \_ \_ clave de sesión de usuario \_**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



No hay ninguna clave de sesión de usuario para la sesión de inicio de sesión especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**cuota de licencia de ERROR \_ \_ \_ superada**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



El servicio al que se está accediendo tiene una licencia para un número determinado de conexiones. No se pueden realizar más conexiones al servicio en este momento porque ya hay tantas conexiones como el servicio puede aceptar.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR \_ de \_ nombre de destino incorrecto \_**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



El nombre de la cuenta de destino no es correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR \_ de \_ autenticación mutua \_ errónea**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Error de autenticación mutua. La contraseña del servidor no está actualizada en el controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_sesgo de tiempo de error \_**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Hay una diferencia de hora y/o fecha entre el cliente y el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR \_ \_ dominio actual \_ no \_ permitido**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Esta operación no se puede realizar en el dominio actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR \_ de \_ identificador de ventana no válido \_**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Identificador de ventana no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR \_ de \_ identificador de menú no válido \_**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Identificador de menú no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR \_ de \_ identificador de cursor no válido \_**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Identificador de cursor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR \_ de \_ controlador de aceleración no válido \_**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Identificador de tabla de aceleradores no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR \_ de \_ identificador de enlace no válido \_**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Identificador de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR \_ de \_ identificador DWP no válido \_**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Identificador no válido para una estructura de posición de varias ventanas.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR \_ TLW \_ con \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



No se puede crear una ventana secundaria de nivel superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR \_ no se \_ encuentra la \_ \_ clase WND**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



No se encuentra la clase de ventana.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_ventana \_ de error de \_ otro \_ subproceso**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Ventana no válida; pertenece a otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**la \_ tecla de error \_ ya está \_ registrada**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



La tecla de acceso rápido ya está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**la \_ clase de error \_ ya \_ existe**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



La clase ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**la clase de ERROR no \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



La clase no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**la \_ clase de error \_ tiene \_ Windows**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



La clase todavía tiene ventanas abiertas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR \_ de \_ índice no válido**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Índice no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR \_ de \_ identificador de icono no válido \_**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Identificador de icono no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR \_ de \_ Índice de cuadro de diálogo privado \_**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Usar palabras privadas de la ventana de cuadro de diálogo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador del cuadro de lista de errores**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



No se encontró el identificador del cuadro de lista.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR: \_ no hay \_ \_ caracteres comodín**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



No se encontraron caracteres comodín.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR de \_ portapapeles \_ \_ abierto**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



El subproceso no tiene abierto un portapapeles.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**la \_ tecla de error \_ no está \_ registrada**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



La tecla de acceso rápido no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**\_cuadro de \_ \_ diálogo ventana de error**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



La ventana no es una ventana de cuadro de diálogo válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador de control de errores**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



No se encontró el identificador de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR \_ de \_ mensaje de cuadro combinado no válido \_**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Mensaje no válido para un cuadro combinado porque no tiene un control de edición.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ventana de ERROR \_ \_ no \_ ComboBox**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



La ventana no es un cuadro combinado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR \_ de \_ edición de alto no válido \_**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



El alto debe ser inferior a 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_ \_ no \_ se encontró el DC de error**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Identificador de contexto de dispositivo (DC) no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR \_ de \_ filtro de enlace no válido \_**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Tipo de procedimiento de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR \_ de \_ filtro no válido \_**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Procedimiento de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**el \_ enlace de errores \_ necesita \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



No se puede establecer un enlace no local sin un identificador de módulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR \_ de \_ enlace solo global \_**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Este procedimiento de enlace solo se puede establecer globalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_conjunto de \_ enlaces del diario de errores \_**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



El procedimiento de enlace del diario ya está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR de \_ enlace \_ no \_ instalado**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



El procedimiento de enlace no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR \_ de \_ mensaje lb no válido \_**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Mensaje no válido para el cuadro de lista de selección única.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR \_ SETCOUNT \_ en \_ \_ lb**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



LB \_ SETCOUNT enviado a un cuadro de lista no diferido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR \_ lb \_ sin \_ TABSTOPS**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Este cuadro de lista no admite tabulaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR al \_ destruir el \_ objeto \_ de \_ otro \_ subproceso**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



No se puede destruir el objeto creado por otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menú de \_ ventana \_ secundaria de error**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Las ventanas secundarias no pueden tener menús.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR: \_ no hay \_ menú del sistema \_**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



La ventana no tiene un menú del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR \_ de \_ estilo de MsgBox no válido \_**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Estilo de cuadro de mensaje no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR \_ de \_ valor SPI no válido \_**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Parámetro de todo el sistema (SPI) no válido \_ \* .


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**pantalla de ERROR \_ \_ ya \_ bloqueada**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



La pantalla ya está bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR \_ hWnd \_ tener \_ diff \_ Parent**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Todos los identificadores de Windows en una estructura de posición de varias ventanas deben tener el mismo elemento primario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR en la \_ \_ \_ ventana secundaria**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



La ventana no es una ventana secundaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR \_ de \_ comando GW no válido \_**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Comando de GW no válido \_ \* .


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR \_ de \_ ID. de subproceso no válido \_**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Identificador de subproceso no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR en la \_ \_ ventana no MDICHILD \_**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



No se puede procesar un mensaje desde una ventana que no sea una ventana de interfaz de múltiples documentos (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR \_ emergente \_ ya \_ activo**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



El menú emergente ya está activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR: \_ no hay \_ barras de desplazamiento**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



La ventana no tiene barras de desplazamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR \_ de \_ intervalo de ScrollBar no válido \_**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



El intervalo de la barra de desplazamiento no puede ser mayor que MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR \_ de \_ comando SHOWWIN no válido \_**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



No se puede mostrar o quitar la ventana de la manera especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR: \_ no hay \_ recursos del sistema \_**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



No hay suficientes recursos del sistema para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR de \_ \_ recursos del sistema no paginados \_**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



No hay suficientes recursos del sistema para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERRORES de \_ \_ recursos del sistema paginados \_**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



No hay suficientes recursos del sistema para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**cuota de espacio de trabajo de ERROR \_ \_ \_**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Cuota insuficiente para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**cuota del archivo de \_ paginación de errores \_**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Cuota insuficiente para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_límite de compromiso de error \_**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



El archivo de paginación es demasiado pequeño para que se complete esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ \_ no \_ se encontró el elemento de menú de error**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



No se encontró un elemento de menú.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR \_ de \_ identificador de teclado no válido \_**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Controlador de distribución de teclado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**tipo de enlace de ERROR \_ \_ \_ no \_ permitido**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Tipo de enlace no permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**el ERROR \_ requiere \_ WINDOWSTATION interactivos \_**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Esta operación requiere una estación de ventana interactiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**tiempo de espera de ERROR \_**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Esta operación devolvió porque expiró el período de tiempo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR \_ de \_ identificador de monitor no válido \_**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Identificador de monitor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR \_ de \_ tamaño incorrecto**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Argumento de tamaño incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**\_clase SYMLINK de error \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



No se puede seguir el vínculo simbólico porque su tipo está deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR \_ SYMLINK \_ no \_ admitido**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Esta aplicación no admite la operación actual en vínculos simbólicos.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**error de \_ análisis de XML de error \_ \_**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows no pudo analizar los datos XML solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**error \_ XMLDSIG de error \_**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Se encontró un error al procesar una firma digital XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR al \_ reiniciar la \_ aplicación**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Esta aplicación debe reiniciarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**\_compartimiento incorrecto \_**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



El autor de la llamada realizó la solicitud de conexión en el compartimiento de enrutamiento equivocado.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR de \_ AUTHIP \_**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Error de AuthIP al intentar conectarse al host remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR: \_ no hay \_ \_ recursos NVRAM**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



No existen recursos NVRAM suficientes para completar el servicio solicitado. Es posible que se necesite un reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR \_ de \_ proceso de GUI \_**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



No se puede finalizar la operación solicitada porque el proceso especificado no es un proceso de GUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**el \_ archivo EVENTLOG de error \_ \_ está dañado**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



El archivo de registro de eventos está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR \_ al \_ \_ iniciar EVENTLOG**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



No se pudo abrir ningún archivo de registro de eventos, por lo que no se inició el servicio de registro de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**archivo de registro de errores \_ \_ \_ completo**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



El archivo de registro de eventos está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**el \_ archivo EVENTLOG de error \_ \_ cambió**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



El archivo de registro de eventos ha cambiado entre las operaciones de lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR \_ de \_ nombre de tarea no válido \_**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



El nombre de tarea especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR \_ de \_ Índice de tarea no válido \_**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



El índice de tarea especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**el \_ subproceso \_ de error ya está \_ en la \_ tarea**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



El subproceso especificado ya está uniendo una tarea.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR al \_ instalar el \_ servicio \_**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



No se pudo obtener acceso al servicio Windows Installer. Esto puede ocurrir si el Windows Installer no está correctamente instalado. Póngase en contacto con el personal de soporte técnico para obtener ayuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR al \_ instalar \_ USEREXIT**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



El usuario canceló la instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR de instalación de ERROR \_ \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Error irrecuperable durante la instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR de \_ instalación de \_ suspensión**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Instalación suspendida, incompleta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR \_ desconocido del \_ producto**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Esta acción solo es válida para los productos que están instalados actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR \_ de \_ característica desconocida**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



IDENTIFICADOR de característica no registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR \_ de \_ componente desconocido**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



IDENTIFICADOR de componente no registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR \_ desconocido \_ (propiedad)**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Propiedad desconocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR \_ de \_ Estado de identificador no válido \_**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



El identificador está en un estado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR \_ de \_ Configuración incorrecta**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Los datos de configuración de este producto están dañados. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**Índice de ERROR \_ \_ ausente**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



El calificador de componente no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**origen de instalación de ERROR \_ \_ \_ ausente**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



El origen de instalación de este producto no está disponible. Compruebe que el origen existe y que puede acceder a él.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR al \_ instalar la \_ versión del paquete \_**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



El servicio Windows Installer no puede instalar este paquete de instalación. Debe instalar un Service Pack de Windows que contenga una versión más reciente del servicio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**producto de ERROR \_ \_ desinstalado**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



El producto se desinstala.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR \_ de \_ Sintaxis de consulta incorrecta \_**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



Sintaxis de consulta SQL no válida o no admitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR \_ de \_ campo no válido**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



El campo de registro no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**dispositivo de ERROR \_ \_ quitado**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Se ha quitado el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**la \_ instalación de error \_ ya se \_ está ejecutando**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Ya hay otra instalación en curso. Complete esa instalación antes de continuar con la instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR \_ \_ al abrir el paquete de instalación \_ \_**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



No se pudo abrir este paquete de instalación. Compruebe que el paquete existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR al \_ instalar el \_ paquete \_ no válido**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



No se pudo abrir este paquete de instalación. Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR de instalación de ERROR de \_ \_ UI \_**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Error al iniciar la interfaz de usuario del servicio de Windows Installer. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR de \_ registro de instalación de errores \_ \_**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Error al abrir el archivo de registro de instalación. Compruebe que la ubicación del archivo de registro especificada existe y que puede escribir en ella.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**\_no se \_ admite el idioma de instalación de errores \_**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



El idioma de este paquete de instalación no es compatible con el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR al \_ instalar la \_ transformación \_**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Error al aplicar transformaciones. Compruebe que las rutas de acceso de transformación especificadas son válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR de \_ instalación de \_ paquete \_ rechazado**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Esta instalación está prohibida por la Directiva del sistema. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**función de ERROR \_ \_ no \_ llamada**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



No se pudo ejecutar la función.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR en la \_ función error \_**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Error de la función durante la ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR \_ de \_ tabla no válida**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Se especificó una tabla no válida o desconocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR de \_ coincidencia de tipo de mensaje \_**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Los datos proporcionados son de un tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR de \_ tipo no compatible \_**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



No se admiten los datos de este tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR \_ al crear error \_**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



No se pudo iniciar el servicio Windows Installer. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR al \_ instalar \_ temp no \_ interescribible**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



La carpeta Temp está en una unidad que está llena o es inaccesible. Libere espacio en la unidad o Compruebe que tiene permiso de escritura en la carpeta Temp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR al \_ instalar la \_ plataforma \_ no compatible**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Este paquete de instalación no es compatible con este tipo de procesador. Póngase en contacto con el fabricante del producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR al \_ instalar \_ NOTUSED**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Componente no usado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR \_ \_ al abrir el paquete de revisión de \_ errores \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



No se pudo abrir este paquete de actualización. Compruebe que el paquete de actualización existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**paquete de revisión de ERROR \_ \_ \_ no válido**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



No se pudo abrir este paquete de actualización. Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**paquete de revisión de ERROR \_ \_ \_ no compatible**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



El servicio Windows Installer no puede procesar este paquete de actualización. Debe instalar un Service Pack de Windows que contenga una versión más reciente del servicio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_versión del producto de error \_**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Ya está instalada otra versión de este producto. La instalación de esta versión no puede continuar. Para configurar o quitar la versión existente de este producto, use agregar o quitar programas en el panel de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR \_ de \_ línea de comandos no válida \_**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Argumento de línea de comandos no válido. Consulte el SDK de Windows Installer para obtener ayuda detallada sobre la línea de comandos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR de \_ instalación \_ remota no \_ permitida**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Solo los administradores tienen permiso para agregar, quitar o configurar el software de servidor durante una sesión remota de Terminal Services. Si desea instalar o configurar el software en el servidor, póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR \_ de \_ reinicio \_ iniciado correctamente**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



La operación solicitada se completó correctamente. El sistema se reiniciará para que los cambios surtan efecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_ \_ \_ no \_ se encontró el destino de revisión de error**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



El servicio Windows Installer no puede instalar la actualización porque es posible que falte el programa que se va a actualizar o que la actualización pueda actualizar una versión diferente del programa. Compruebe que el programa que se va a actualizar existe en el equipo y que tiene la actualización correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**paquete de revisión de errores \_ \_ \_ rechazado**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



La Directiva de restricción de software no permite el paquete de actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR \_ de \_ transformación de instalación \_ rechazada**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Una o más personalizaciones no están permitidas por la Directiva de restricción de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR al \_ instalar el \_ remoto \_ prohibido**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



El Windows Installer no permite la instalación desde un Conexión a Escritorio remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_no se \_ admite la eliminación de la revisión de errores \_**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



No se admite la desinstalación del paquete de actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR \_ de \_ revisión desconocida**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



La actualización no se aplica a este producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR de \_ revisión \_ sin \_ secuencia**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



No se encontró ninguna secuencia válida para el conjunto de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**no \_ se \_ permite la eliminación de la revisión de errores \_**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



No se ha permitido la eliminación de la actualización por la Directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR \_ de \_ revisión \_ XML no válida**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Los datos de actualización XML no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**producto de revisión de errores \_ \_ administrado \_ anunciada \_**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Installer no permite la actualización de productos anunciados administrados. Debe instalar al menos una característica del producto antes de aplicar la actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR al \_ instalar el \_ servicio \_ SafeBoot**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



No se puede obtener acceso al servicio Windows Installer en modo seguro. Vuelva a intentarlo cuando el equipo no esté en modo seguro o use Restaurar sistema para devolver el equipo a un estado bueno anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**excepción de ERROR de ERROR \_ \_ rápido \_**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Se produjo una excepción de error rápido. No se invocarán los controladores de excepciones y el proceso se terminará inmediatamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**instalación de ERROR \_ \_ rechazada**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



La aplicación que está intentando ejecutar no es compatible con esta versión de Windows.


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

 

 




