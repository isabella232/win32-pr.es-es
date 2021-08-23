---
description: Describe los códigos de error 1300-1699 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Códigos de error del sistema (1300-1699) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7aeb1c3642331db8ed3215d55a6d77e1e7b2a98c3859a5eb64a1d5b60350d24a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119310925"
---
# <a name="system-error-codes-1300-1699"></a>Códigos de error del sistema (1300-1699)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema para los errores 1300 a 1699. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR \_ NO \_ TODOS \_ ASIGNADOS**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



No todos los privilegios o grupos a los que se hace referencia se asignan al autor de la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR \_ ALGUNOS \_ NO \_ ASIGNADOS**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



No se ha realizado alguna asignación entre los nombres de cuenta y los ID de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR \_ NO \_ QUOTAS \_ FOR \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



No se establecen límites de cuota del sistema específicamente para esta cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR \_ CLAVE DE SESIÓN DE USUARIO \_ \_ \_ LOCAL**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



No hay ninguna clave de cifrado disponible. Se devolvió una clave de cifrado conocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR \_ NULL \_ LM \_ PASSWORD**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



La contraseña es demasiado compleja para convertirse en una contraseña de LAN Manager. La contraseña del administrador de LAN devuelta es una **cadena NULL.**


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR \_ REVISIÓN \_ DESCONOCIDA**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



Se desconoce el nivel de revisión.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR \_ REVISION \_ MISMATCH**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Indica que dos niveles de revisión no son compatibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR \_ PROPIETARIO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Es posible que este identificador de seguridad no se asigne como propietario de este objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR \_ GRUPO PRINCIPAL NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Es posible que este identificador de seguridad no se asigne como grupo principal de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR \_ NO \_ IMPERSONATION \_ TOKEN**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Se ha intentado operar en un token de suplantación mediante un subproceso que no está suplantando actualmente a un cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR \_ CANT \_ DISABLE \_ MANDATORY**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



Es posible que el grupo no esté deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR \_ NO \_ LOGON \_ SERVERS**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



Actualmente no hay servidores de inicio de sesión disponibles para dar servicio a la solicitud de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR \_ NO SE HA PRODUCIDO DICHA SESIÓN DE INICIO DE \_ \_ \_ SESIÓN**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Una sesión de inicio especificada no existe. Es posible que ya se haya terminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR \_ AL NO TENER ESTE \_ \_ PRIVILEGIO**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



No existe un privilegio especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**PRIVILEGIO DE ERROR \_ \_ NO \_ MANTENIDO**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



El cliente no dispone de un privilegio requerido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR \_ NOMBRE DE CUENTA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



El nombre proporcionado no es un nombre de cuenta con el formato correcto.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR \_ EL USUARIO \_ EXISTE**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



La cuenta especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR \_ NO \_ SUCH \_ USER**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



La cuenta especificada no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**EXISTE \_ UN GRUPO DE \_ ERRORES**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



El grupo especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR \_ NO \_ SUCH \_ GROUP**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



El grupo especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**MIEMBRO \_ DE ERROR EN \_ \_ GROUP**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



La cuenta de usuario especificada ya es miembro del grupo especificado o no se puede eliminar el grupo especificado porque contiene un miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**MIEMBRO \_ DE ERROR NO EN EL \_ \_ \_ GRUPO**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



La cuenta de usuario especificada no es miembro de la cuenta de grupo especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR \_ ÚLTIMO \_ ADMINISTRADOR**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Esta operación no está permitido, ya que podría dar lugar a que una cuenta de administración se deshabilite, elimine o no pueda iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR \_ DE CONTRASEÑA \_ INCORRECTA**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado como contraseña actual es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR \_ CONTRASEÑA CON UN MAL \_ \_ FORMADO**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado para la nueva contraseña contiene valores que no se permiten en las contraseñas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**RESTRICCIÓN DE \_ CONTRASEÑA DE \_ ERROR**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



No se puede actualizar la contraseña. El valor proporcionado para la nueva contraseña no cumple los requisitos de longitud, complejidad o historial del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR AL \_ INICIAR SESIÓN \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



El nombre de usuario o la contraseña son incorrectos.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**RESTRICCIÓN DE \_ LA CUENTA \_ DE ERROR**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



Las restricciones de cuenta impiden que este usuario inicie sesión. Por ejemplo: no se permiten contraseñas en blanco, los tiempos de inicio de sesión son limitados o se ha aplicado una restricción de directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR \_ HORAS DE INICIO DE SESIÓN NO \_ \_ VÁLIDAS**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Su cuenta tiene restricciones de tiempo que le evitarán iniciar sesión en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR \_ ESTACIÓN DE TRABAJO NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Este usuario no puede iniciar sesión en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**CONTRASEÑA DE ERROR \_ \_ EXPIRADA**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



La contraseña de esta cuenta ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**CUENTA DE ERROR \_ \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Este usuario no puede iniciar sesión porque esta cuenta está deshabilitada actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR \_ NINGUNO \_ ASIGNADO**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



No se ha realizado ninguna asignación entre los nombres de cuenta y los ID de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR \_ \_ DEMASIADAS \_ LUID \_ SOLICITADAS**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Se solicitaron demasiados identificadores de usuario locales (LUID) al mismo tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**\_LUIDS DE ERROR \_ AGOTADOS**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



No hay más identificadores de usuario locales (LUID) disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR \_ INVALID \_ SUB \_ AUTHORITY**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



La parte de subautoridad de un identificador de seguridad no es válida para este uso en particular.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR \_ DE ACL NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



La estructura de la lista de control de acceso (ACL) no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR \_ \_ SID NO VÁLIDO**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



La estructura del identificador de seguridad no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR \_ \_ DESCR DE \_ SEGURIDAD NO VÁLIDA**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



La estructura del descriptor de seguridad no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR: \_ ACL DE HERENCIA NO \_ \_ RECIBIDA**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



No se pudo construir la lista de control de acceso (ACL) heredada o la entrada de control de acceso (ACE).


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR \_ SERVER \_ DISABLED**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



El servidor está deshabilitado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR SERVER NOT DISABLED (SERVIDOR DE ERRORES \_ NO \_ \_ DESHABILITADO)**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



El servidor está habilitado actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR \_ INVALID \_ ID \_ AUTHORITY**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



El valor proporcionado era un valor no válido para una entidad de identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**SE \_ SUPERÓ EL \_ ESPACIO ASIGNADO POR \_ ERROR**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



No hay más memoria disponible para las actualizaciones de información de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR \_ ATRIBUTOS DE GRUPO NO \_ \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Los atributos especificados no son válidos o no son compatibles con los atributos del grupo en su conjunto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR \_ NIVEL \_ DE \_ SUPLANTACIÓN DE ERROR**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



No se ha proporcionado el nivel de representación necesario o el nivel de representación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR \_ NO SE PUEDE ABRIR \_ \_ ANÓNIMO**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



No se puede abrir un token de seguridad de nivel anónimo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR \_ BAD \_ VALIDATION \_ (CLASE)**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



La clase de información de validación solicitada no era válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**TIPO \_ DE TOKEN DE ERROR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



El tipo del token no es adecuado para su intento de uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR \_ NO \_ SECURITY \_ ON \_ OBJECT**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



No se puede realizar una operación de seguridad en un objeto que no tiene ninguna seguridad asociada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR \_ NO SE PUEDE ACCEDER A LA INFORMACIÓN DE \_ \_ \_ DOMINIO**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



No se pudo leer la información de configuración del controlador de dominio, ya sea porque la máquina no está disponible o porque se ha denegado el acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR \_ ESTADO DE SERVIDOR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



El servidor del administrador de cuentas de seguridad (SAM) o la autoridad de seguridad local (LSA) estaba en un estado incorrecto para realizar la operación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR \_ ESTADO DE DOMINIO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



El dominio estaba en un estado incorrecto para realizar la operación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR \_ ROL DE DOMINIO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Esta operación solo se permite para el controlador de dominio principal del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR \_ NO \_ SUCH \_ DOMAIN**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



El dominio especificado no existe o no se pudo ponerse en contacto con él.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**DOMINIO \_ DE ERROR \_ EXISTE**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



El dominio especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**SE \_ SUPERÓ \_ EL LÍMITE DE DOMINIO \_ DE ERROR**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Se intentó superar el límite en el número de dominios por servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR DAÑOS \_ EN LA BASE DE DATOS \_ \_ INTERNA**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



No se puede completar la operación solicitada debido a un error grave en los medios o a daños en la estructura de datos en el disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR \_ \_ INTERNO**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR \_ GENÉRICO \_ NO \_ ASIGNADO**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Los tipos de acceso genéricos estaban contenidos en una máscara de acceso que ya se debería asignar a tipos no genéricos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**FORMATO \_ DE DESCRIPTOR DE ERROR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Un descriptor de seguridad no tiene el formato correcto (absoluto o relativo a sí mismo).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR \_ NO PROCESO DE INICIO DE \_ \_ SESIÓN**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



La acción solicitada está restringida solo para que la usen los procesos de inicio de sesión. El proceso de llamada no se ha registrado como un proceso de inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**EXISTE UNA \_ SESIÓN DE INICIO DE SESIÓN DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



No se puede iniciar una nueva sesión de inicio de sesión con un identificador que ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR \_ NO \_ SUCH \_ PACKAGE**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Se desconoce un paquete de autenticación especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR \_ ESTADO DE SESIÓN DE INICIO DE SESIÓN NO \_ \_ \_ CORRECTO**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



La sesión de inicio de sesión no está en un estado coherente con la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**COLISIÓN DE \_ SESIÓN DE INICIO DE SESIÓN DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



El identificador de sesión de inicio de sesión ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR \_ TIPO DE INICIO DE SESIÓN NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Una solicitud de inicio de sesión contenía un valor de tipo de inicio de sesión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR \_ NO SE PUEDE \_ SUPLANTAR**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



No se puede suplantar mediante una canalización con nombre hasta que se han leído datos de esa canalización.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR \_ RXACT \_ INVALID \_ STATE**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



El estado de transacción de un subárbol del Registro no es compatible con la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR \_ RXACT \_ COMMIT \_ FAILURE**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Se ha detectado un daño en una base de datos de seguridad interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**CUENTA \_ ESPECIAL DE \_ ERROR**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



No se puede realizar esta operación en cuentas integradas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**GRUPO \_ ESPECIAL DE \_ ERRORES**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



No se puede realizar esta operación en este grupo especial integrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**USUARIO \_ ESPECIAL \_ DE ERROR**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



No se puede realizar esta operación en este usuario especial integrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**GRUPO \_ PRINCIPAL DE MIEMBROS DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



El usuario no se puede quitar de un grupo porque el grupo es actualmente el grupo principal del usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**TOKEN \_ DE ERROR YA EN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



El token ya está en uso como token principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR \_ NO \_ SUCH \_ ALIAS**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



El grupo local especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**MIEMBRO \_ DE ERROR NO EN \_ \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



El nombre de cuenta especificado no es miembro del grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**MIEMBRO \_ DE ERROR EN \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



El nombre de cuenta especificado ya es miembro del grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**EL \_ ALIAS DE ERROR \_ EXISTE**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



El grupo local especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR \_ DE INICIO DE SESIÓN NO \_ \_ CONCEDIDO**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR \_ \_ DEMASIADOS \_ SECRETOS**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



Se ha superado el número máximo de secretos que se pueden almacenar en un único sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**SECRETO DE ERROR \_ \_ DEMASIADO \_ LARGO**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



La longitud de un secreto supera la longitud máxima permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR INTERNO \_ \_ DE BASE DE \_ DATOS**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



La base de datos de la autoridad de seguridad local contiene una incoherencia interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR \_ \_ DEMASIADOS \_ \_ IDENTIFICADORES DE CONTEXTO**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Durante un intento de inicio de sesión, el contexto de seguridad del usuario acumuló demasiados id. de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**TIPO \_ DE INICIO DE SESIÓN DE ERROR NO \_ \_ \_ CONCEDIDO**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR \_ NT \_ CROSS \_ ENCRYPTION \_ REQUIRED**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Se necesita una contraseña cifrada cruzada para cambiar una contraseña de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR \_ NO \_ SUCH \_ MEMBER**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



No se pudo agregar ni quitar un miembro del grupo local porque el miembro no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR \_ MIEMBRO \_ NO VÁLIDO**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



No se pudo agregar un nuevo miembro a un grupo local porque el miembro tiene el tipo de cuenta incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR \_ \_ DEMASIADOS \_ SID**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Se han especificado demasiados iD de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR \_ LM \_ CROSS \_ ENCRYPTION \_ REQUIRED**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Se necesita una contraseña cifrada cruzada para cambiar esta contraseña de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR \_ SIN \_ HERENCIA**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Indica que una ACL no contiene componentes heredables.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ARCHIVO DE ERROR \_ \_ DAÑADO**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



El archivo o directorio está dañado e ilegible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**DISCO DE \_ ERROR \_ DAÑADO**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



La estructura del disco está dañada e ilegible.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR \_ SIN CLAVE DE SESIÓN DE \_ \_ \_ USUARIO**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



No hay ninguna clave de sesión de usuario para la sesión de inicio de sesión especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**CUOTA DE \_ LICENCIA \_ DE ERROR \_ SUPERADA**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



El servicio al que se está accediendo tiene una licencia para un número determinado de conexiones. No se pueden realizar más conexiones al servicio en este momento porque ya hay tantas conexiones como el servicio pueda aceptar.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR \_ NOMBRE DE DESTINO \_ \_ INCORRECTO**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



El nombre de la cuenta de destino es incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR \_ DE \_ AUTENTICACIÓN MUTUA CON \_ ERROR**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Error de autenticación mutua. La contraseña del servidor no está actualizada en el controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_SESGO DE TIEMPO DE \_ ERROR**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Hay una diferencia de fecha y hora entre el cliente y el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR \_ DOMINIO ACTUAL NO \_ \_ \_ PERMITIDO**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Esta operación no se puede realizar en el dominio actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR \_ IDENTIFICADOR DE VENTANA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Identificador de ventana no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR \_ IDENTIFICADOR DE MENÚ NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Identificador de menú no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR \_ IDENTIFICADOR DE CURSOR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Identificador de cursor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR \_ IDENTIFICADOR DE ACL NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Identificador de tabla de aceleradores no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR \_ IDENTIFICADOR DE ENLACE NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Identificador de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR \_ IDENTIFICADOR \_ DE DWP NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Identificador no válido para una estructura de posición de varias ventanas.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR \_ TLW \_ CON \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



No se puede crear una ventana secundaria de nivel superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR \_ NO SE ENCUENTRA LA CLASE \_ \_ \_ WND**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



No se encuentra la clase window.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**VENTANA \_ DE ERROR DE OTRO \_ \_ \_ SUBPROCESO**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Ventana no válida; pertenece a otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR \_ HOTKEY \_ ALREADY \_ REGISTERED**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



Ya se ha registrado la tecla de acceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**LA \_ CLASE DE ERROR YA \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



La clase ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**LA \_ CLASE ERROR NO \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



La clase no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**LA \_ CLASE DE ERROR TIENE \_ \_ WINDOWS**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



La clase todavía tiene ventanas abiertas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR \_ ÍNDICE NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Índice no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR \_ IDENTIFICADOR DE ICONO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Identificador de icono no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR \_ PRIVATE \_ DIALOG \_ INDEX**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Uso de palabras de ventana DIALOG privadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR \_ LISTBOX \_ ID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



No se encontró el identificador del cuadro de lista.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR \_ SIN CARACTERES \_ \_ COMODÍN**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



No se encontraron caracteres comodín.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR \_ EL PORTAPAPELES \_ NO ESTÁ \_ ABIERTO**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



El subproceso no tiene un Portapapeles abierto.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR \_ HOTKEY \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



La clave de acceso no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**VENTANA DE ERROR \_ \_ NO \_ DIÁLOGO**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



La ventana no es una ventana de diálogo válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**IDENTIFICADOR \_ DE CONTROL DE ERROR NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



No se encontró el identificador de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR \_ MENSAJE DE CUADRO COMBINADO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Mensaje no válido para un cuadro combinado porque no tiene un control de edición.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**VENTANA DE \_ ERROR \_ NO \_ COMBOBOX**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



La ventana no es un cuadro combinado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR \_ EDITAR ALTO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



El alto debe ser menor que 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR \_ DC \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Identificador de contexto de dispositivo (DC) no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR \_ FILTRO DE ENLACE NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Tipo de procedimiento de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR \_ INVALID \_ FILTER \_ PROC**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Procedimiento de enlace no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**EL \_ ENLACE DE ERROR NECESITA \_ \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



No se puede establecer un enlace no local sin un identificador de módulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ENLACE \_ DE SOLO GLOBAL DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Este procedimiento de enlace solo se puede establecer globalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**CONJUNTO \_ DE ENLACES DE DIARIO DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



El procedimiento de enlace de diario ya está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ENLACE \_ DE ERROR NO \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



El procedimiento de enlace no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR \_ MENSAJE DE LB NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Mensaje no válido para el cuadro de lista de selección única.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR \_ SETCOUNT \_ ON \_ BAD \_ LB**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



LB \_ SETCOUNT enviado al cuadro de lista no diferido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR \_ LB \_ SIN \_ TABSTOPS**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Este cuadro de lista no admite tabulaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR \_ AL DESTRUIR EL OBJETO DE OTRO \_ \_ \_ \_ SUBPROCESO**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



No se puede destruir el objeto creado por otro subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**MENÚ DE \_ VENTANA \_ SECUNDARIA DE \_ ERROR**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Las ventanas secundarias no pueden tener menús.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR \_ EN EL MENÚ DEL \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



La ventana no tiene un menú del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR \_ ESTILO \_ MSGBOX NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Estilo de cuadro de mensaje no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR: \_ VALOR \_ SPI NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Parámetro de todo el sistema \_ \* (SPI) no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**PANTALLA DE \_ ERROR \_ YA \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



La pantalla ya está bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**LOS \_ HWND DE ERROR \_ TIENEN UN ELEMENTO PRIMARIO DE \_ \_ DIFERENCIAS**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Todos los identificadores de las ventanas de una estructura de posición de varias ventanas deben tener el mismo elemento primario.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR \_ NO \_ VENTANA \_ SECUNDARIA**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



La ventana no es una ventana secundaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR \_ COMANDO GW NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Comando GW \_ \* no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR \_ IDENTIFICADOR DE SUBPROCESO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Identificador de subproceso no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR \_ NO \_ VENTANA MDICHILD \_**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



No se puede procesar un mensaje desde una ventana que no es una ventana de interfaz de múltiples documentos (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**VENTANA \_ EMERGENTE DE ERROR YA \_ \_ ACTIVA**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



Menú emergente ya activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR \_ NO \_ SCROLLBARS**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



La ventana no tiene barras de desplazamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR \_ INTERVALO DE BARRA DE DESPLAZAMIENTO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



El intervalo de la barra de desplazamiento no puede ser mayor que MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR \_ COMANDO \_ SHOWWIN NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



No se puede mostrar ni quitar la ventana de la manera especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Existen recursos del sistema insuficientes para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR \_ RECURSOS DEL SISTEMA SIN \_ \_ PÁGINA**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Existen recursos del sistema insuficientes para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**RECURSOS \_ DEL SISTEMA \_ PAGINADOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Existen recursos del sistema insuficientes para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR \_ DE CUOTA DE ESPACIO DE \_ \_ TRABAJO**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Cuota insuficiente para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR \_ PAGEFILE \_ QUOTA**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Cuota insuficiente para completar el servicio solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**LÍMITE \_ DE COMPROMISO DE \_ ERROR**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



El archivo de paginación es demasiado pequeño para que se complete esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR \_ ELEMENTO DE MENÚ NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



No se encontró un elemento de menú.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR \_ IDENTIFICADOR DE TECLADO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Identificador de diseño de teclado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**TIPO \_ DE ENLACE DE ERROR NO \_ \_ \_ PERMITIDO**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Tipo de enlace no permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR \_ REQUIERE \_ \_ WINDOWSTATION INTERACTIVA**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Esta operación requiere una estación de ventana interactiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**TIEMPO DE ESPERA \_ DE ERROR**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Esta operación se devolvió porque expiró el período de tiempo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR \_ IDENTIFICADOR DE MONITOR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Identificador de monitor no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR \_ TAMAÑO \_ INCORRECTO**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Argumento de tamaño incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR \_ SYMLINK \_ (CLASE \_ DESHABILITADA)**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



No se puede seguir el vínculo simbólico porque su tipo está deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR \_ SYMLINK \_ NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Esta aplicación no admite la operación actual en vínculos simbólicos.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR \_ XML \_ PARSE \_ ERROR**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



Windows no pudo analizar los datos XML solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR \_ XMLDSIG \_ ERROR**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Se encontró un error al procesar una firma digital XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR \_ AL REINICIAR LA \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Esta aplicación debe reiniciarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR \_ EN EL COMPARTIMIENTO \_ INCORRECTO**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



El autor de la llamada realizó la solicitud de conexión en el compartimiento de enrutamiento incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR \_ AUTHIP \_ FAILURE**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Se ha produce un error de AuthIP al intentar conectarse al host remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR \_ NO HAY RECURSOS DE \_ \_ NVRAM**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Existen recursos de NVRAM insuficientes para completar el servicio solicitado. Es posible que se necesite un reinicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR \_ NO PROCESO DE \_ GUI \_**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



No se puede finalizar la operación solicitada porque el proceso especificado no es un proceso gui.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR \_ EVENTLOG \_ FILE \_ CORRUPT**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



El archivo de registro de eventos está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR \_ EVENTLOG \_ CANT \_ START**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



No se pudo abrir ningún archivo de registro de eventos, por lo que el servicio de registro de eventos no se inició.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ARCHIVO \_ DE REGISTRO DE ERRORES \_ \_ LLENO**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



El archivo de registro de eventos está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR \_ EVENTLOG \_ FILE \_ CHANGED**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



El archivo de registro de eventos ha cambiado entre las operaciones de lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR \_ NOMBRE DE TAREA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



El nombre de tarea especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR \_ ÍNDICE DE TAREAS NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



El índice de tareas especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**SUBPROCESO DE \_ ERROR YA EN LA \_ \_ \_ TAREA**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



El subproceso especificado ya se está uniendo a una tarea.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR \_ AL INSTALAR EL \_ \_ SERVICIO**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



No Windows se pudo acceder al servicio del instalador de archivos. Esto puede ocurrir si el Windows instalador no está instalado correctamente. Póngase en contacto con el personal de soporte técnico para obtener ayuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR \_ AL \_ INSTALAR USEREXIT**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



Instalación cancelada por el usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR \_ DE INSTALACIÓN \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Error irrecuperable durante la instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR \_ INSTALL \_ SUSPEND**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Instalación suspendida, incompleta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR \_ PRODUCTO \_ DESCONOCIDO**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Esta acción solo es válida para los productos que están instalados actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**CARACTERÍSTICA DESCONOCIDA \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



Id. de característica no registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**COMPONENTE DESCONOCIDO \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



Id. de componente no registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR \_ UNKNOWN \_ PROPERTY**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Propiedad desconocida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR \_ ESTADO DE IDENTIFICADOR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



El identificador está en un estado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR \_ DE CONFIGURACIÓN NO \_ ACTIVA**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Los datos de configuración de este producto están dañados. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR \_ INDEX \_ ABSENT**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Calificador de componente no presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR \_ AL INSTALAR EL ORIGEN \_ \_ AUSENTE**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



El origen de instalación de este producto no está disponible. Compruebe que el origen existe y que puede acceder a él.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR \_ INSTALAR LA VERSIÓN DEL \_ \_ PAQUETE**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



Este paquete de instalación no se puede instalar mediante el servicio Windows Installer. Debe instalar un service pack Windows que contenga una versión más reciente del servicio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR \_ PRODUCTO \_ DESINSTALADO**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



El producto se desinstala.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**SINTAXIS \_ DE CONSULTA INCORRECTA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



SQL sintaxis de consulta no válida o no compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**CAMPO ERROR \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



El campo de registro no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**SE \_ QUITÓ EL \_ DISPOSITIVO DE ERROR**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



Se ha quitado el dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR \_ AL INSTALAR YA EN \_ \_ EJECUCIÓN**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Ya hay otra instalación en curso. Complete esa instalación antes de continuar con esta instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR AL \_ ABRIR EL PAQUETE DE INSTALACIÓN CON \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



No se pudo abrir este paquete de instalación. Compruebe que el paquete existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de Windows instalador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR \_ AL INSTALAR EL PAQUETE NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



No se pudo abrir este paquete de instalación. Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete Windows instalador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR AL \_ INSTALAR LA INTERFAZ DE \_ \_ USUARIO**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Se produjo un error al iniciar la interfaz Windows de usuario del servicio Installer. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR AL \_ INSTALAR \_ EL \_ REGISTRO**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Error al abrir el archivo de registro de instalación. Compruebe que existe la ubicación del archivo de registro especificada y que puede escribir en ella.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR \_ AL INSTALAR EL IDIOMA NO \_ \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



El sistema no admite el idioma de este paquete de instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR AL \_ INSTALAR EL ERROR DE \_ \_ TRANSFORMACIÓN**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Error al aplicar transformaciones. Compruebe que las rutas de acceso de transformación especificadas son válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR \_ AL INSTALAR EL PAQUETE \_ \_ RECHAZADO**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Esta instalación está prohibida por la directiva del sistema. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**FUNCIÓN DE \_ ERROR \_ NO \_ LLAMADA**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



No se pudo ejecutar la función.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR EN \_ LA FUNCIÓN \_**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



Error de función durante la ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR \_ TABLA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Tabla no válida o desconocida especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR \_ DATATYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Los datos proporcionados son de tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**TIPO \_ NO ADMITIDO DE \_ ERROR**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



No se admiten datos de este tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR \_ AL CREAR \_ ERROR**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



No se Windows el servicio instalador de archivos. Póngase en contacto con el personal de soporte técnico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR \_ AL INSTALAR TEMP \_ \_ UNWRITABLE**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



La carpeta Temp está en una unidad que está llena o no es accesible. Liberar espacio en la unidad o comprobar que tiene permiso de escritura en la carpeta Temp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR \_ AL INSTALAR LA PLATAFORMA NO \_ \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Este tipo de procesador no admite este paquete de instalación. Póngase en contacto con el proveedor del producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR \_ INSTALL \_ NOTUSED**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Componente no utilizado en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR AL \_ ABRIR EL PAQUETE DE \_ \_ REVISIÓN \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



No se pudo abrir este paquete de actualización. Compruebe que el paquete de actualización existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización Windows instalador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**PAQUETE DE \_ REVISIÓN \_ DE ERROR NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



No se pudo abrir este paquete de actualización. Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización Windows instalador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**PAQUETE \_ DE \_ REVISIÓN DE ERRORES NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



El servicio instalador de Windows no puede procesar este paquete de actualización. Debe instalar un service pack Windows que contenga una versión más reciente del servicio Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR \_ VERSIÓN DEL \_ PRODUCTO**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Ya está instalada otra versión de este producto. La instalación de esta versión no puede continuar. Para configurar o quitar la versión existente de este producto, use Agregar o quitar programas en el Panel de control.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR \_ LÍNEA DE COMANDOS NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Argumento de línea de comandos no válido. Consulte el SDK Windows Installer para obtener ayuda detallada de la línea de comandos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR \_ DE INSTALACIÓN REMOTA NO \_ \_ PERMITIDO**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Solo los administradores tienen permiso para agregar, quitar o configurar software de servidor durante una sesión remota de Terminal Services. Si desea instalar o configurar software en el servidor, póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR \_ AL REINICIAR \_ \_ CORRECTAMENTE INICIADO**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



La operación solicitada se completó correctamente. El sistema se reiniciará para que los cambios puedan tener efecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**NO SE \_ ENCONTRÓ EL DESTINO DE \_ \_ \_ REVISIÓN DE ERROR**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



El servicio instalador de Windows no puede instalar la actualización porque es posible que falte el programa que se va a actualizar o que la actualización actualice una versión diferente del programa. Compruebe que el programa que se va a actualizar existe en el equipo y que tiene la actualización correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**PAQUETE \_ DE \_ REVISIÓN DE ERROR \_ RECHAZADO**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



La directiva de restricción de software no permite el paquete de actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR \_ AL INSTALAR LA TRANSFORMACIÓN \_ \_ RECHAZADA**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Una o varias personalizaciones no están permitidas por la directiva de restricción de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR \_ DE INSTALACIÓN REMOTA \_ \_ PROHIBIDA**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



El Windows no permite la instalación desde un Conexión a Escritorio remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ELIMINACIÓN \_ DE \_ REVISIÓN \_ DE ERRORES NO ADMITIDA**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



No se admite la desinstalación del paquete de actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**REVISIÓN \_ DESCONOCIDA DE \_ ERROR**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



La actualización no se aplica a este producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**REVISIÓN \_ \_ DE ERRORES SIN \_ SECUENCIA**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



No se encontró ninguna secuencia válida para el conjunto de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**NO \_ SE PUEDE ELIMINAR LA \_ \_ REVISIÓN DE ERRORES**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



La directiva no ha permitido la eliminación de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR \_ XML DE \_ REVISIÓN NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Los datos de actualización XML no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**PRODUCTO \_ ANUNCIADO ADMINISTRADO POR \_ REVISIÓN DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows El instalador no permite la actualización de productos anunciados administrados. Debe instalarse al menos una característica del producto antes de aplicar la actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR \_ AL INSTALAR \_ \_ SAFEBOOT DEL SERVICIO**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



El Windows installer no es accesible en Caja fuerte modo. Inténtelo de nuevo cuando el equipo no esté en modo Caja fuerte o puede usar Restaurar sistema para devolver el equipo a un estado anterior bueno.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR \_ AL FAST \_ \_ EXCEPCIÓN**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Se produjo una excepción rápida de error. No se invocarán controladores de excepciones y el proceso finalizará inmediatamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR \_ DE \_ INSTALACIÓN RECHAZADA**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



La aplicación que intenta ejecutar no se admite en esta versión de Windows.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




