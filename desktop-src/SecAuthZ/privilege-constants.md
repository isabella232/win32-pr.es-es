---
Description: Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilegios (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168949"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilegios (autorización)

Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

Las funciones que obtienen y ajustan los privilegios en un [*token*](/windows/desktop/SecGloss/a-gly) de acceso usan el tipo de identificador único [*local*](/windows/desktop/SecGloss/l-gly) (LUID) para identificar privilegios. Use la [**función LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para determinar el [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) en el sistema local que corresponde a una constante de privilegios. Use la [**función LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para convertir **un LUID** en su constante de cadena correspondiente.

El sistema operativo representa un privilegio mediante la cadena que sigue a "Derecho de usuario" en la columna Descripción de la tabla siguiente. El sistema operativo muestra las cadenas derechas  del usuario en la columna **Directiva** del nodo Asignación de derechos de usuario del complemento Configuración Microsoft Management Console seguridad local (MMC).

## <a name="example"></a>Ejemplo

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) en GitHub.

## <a name="constants"></a>Constantes



| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>TEXT("SeAssignPrimaryTokenPrivilege")</dt></dl> | Necesario para asignar el <a href="/windows/desktop/SecGloss/p-gly"><em>token principal</em></a> de un proceso. <br /> Derecho de usuario: reemplace un token de nivel de proceso.<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl><dt><strong>SE_AUDIT_NAME</strong></dt><dt>TEXT("SeAuditPrivilege")</dt></dl> | Necesario para generar entradas de registro de auditoría. Dé este privilegio a los servidores seguros. <br /> Derecho de usuario: genere auditorías de seguridad.<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl><dt><strong>SE_BACKUP_NAME</strong></dt><dt>TEXT("SeBackupPrivilege")</dt></dl> | Necesario para realizar operaciones de copia de seguridad. Este privilegio hace que el sistema conceda todo el control de acceso de lectura a cualquier archivo, independientemente de la lista de <a href="/windows/desktop/SecGloss/a-gly"><em>control</em></a> de acceso (ACL) especificada para el archivo. Cualquier solicitud de acceso que no sea de lectura se sigue evaluando con la ACL. Este privilegio lo requieren las <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>funciones RegSaveKey</strong></a> <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>y RegSaveKeyEx.</strong></a> Si se mantiene este privilegio, se conceden los siguientes derechos de acceso:<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>Derecho de usuario: haga una copia de seguridad de archivos y directorios.<br />Si el archivo se encuentra en una unidad extraíble y la opción "Auditar Storage extraíble" está habilitada, el SE_SECURITY_NAME debe tener ACCESS_SYSTEM_SECURITY. | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>TEXT("SeChangeNotifyPrivilege")</dt></dl> | Necesario para recibir notificaciones de cambios en archivos o directorios. Este privilegio también hace que el sistema omita todas las comprobaciones de acceso transversal. Está habilitada de forma predeterminada para todos los usuarios. <br /> Derecho de usuario: omitir la comprobación de recorrido.<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>TEXT("SeCreateGlobalPrivilege")</dt></dl> | Necesario para crear objetos de asignación de archivos con nombre en el espacio de nombres global durante las sesiones de Terminal Services. Este privilegio está habilitado de forma predeterminada para administradores, servicios y la cuenta del sistema local.<br /> Derecho de usuario: cree objetos globales.<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>TEXT("SeCreatePagefilePrivilege")</dt></dl> | Necesario para crear un archivo de paginación. <br /> Derecho de usuario: cree un archivo de paginación.<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>TEXT("SeCreatePermanentPrivilege")</dt></dl> | Necesario para crear un objeto permanente. <br /> Derecho de usuario: cree objetos compartidos permanentes.<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>TEXT("SeCreateSymbolicLinkPrivilege")</dt></dl> | Necesario para crear un vínculo simbólico.<br /> Derecho de usuario: cree vínculos simbólicos.<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>TEXT("SeCreateTokenPrivilege")</dt></dl> | Necesario para crear un token principal. <br /> Derecho de usuario: cree un objeto de token.<br /> No puede agregar este privilegio a una cuenta de usuario con la directiva "Crear un objeto de token". Además, no puede agregar este privilegio a un proceso de propiedad mediante Windows API. <strong>Windows Server 2003 y Windows XP</strong> con SP1 y versiones anteriores: Windows API pueden agregar este privilegio a un proceso de propiedad.<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl><dt><strong>SE_DEBUG_NAME</strong></dt><dt>TEXT("SeDebugPrivilege")</dt></dl> | Necesario para depurar y ajustar la memoria de un proceso propiedad de otra cuenta. <br /> Derecho de usuario: depurar programas.<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeDelegateSessionUserImpersonatePrivilege")</dt></dl> | Necesario para obtener un token de suplantación para otro usuario en la misma sesión. <br /> Derecho de usuario: suplantar a otros usuarios.<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>TEXT("SeEnableDelegationPrivilege")</dt></dl> | Se requiere para marcar las cuentas de usuario y equipo como de confianza para la delegación.<br /> Derecho de usuario: permite que las cuentas de equipo y usuario sean de confianza para la delegación.<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl><dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeImpersonatePrivilege")</dt></dl> | Necesario para suplantar.<br /> Derecho de usuario: suplantar un cliente después de la autenticación.<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>TEXT("SeIncreaseBasePriorityPrivilege")</dt></dl> | Necesario para aumentar la prioridad base de un proceso. <br /> Derecho de usuario: aumente la prioridad de programación.<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>TEXT("SeIncreaseQuotaPrivilege")</dt></dl> | Necesario para aumentar la cuota asignada a un proceso. <br /> Derecho de usuario: ajuste las cuotas de memoria de un proceso.<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>TEXT("SeIncreaseWorkingSetPrivilege")</dt></dl> | Necesario para asignar más memoria a las aplicaciones que se ejecutan en el contexto de los usuarios.<br /> Derecho de usuario: aumente un conjunto de trabajo de proceso.<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>TEXT("SeLoadDriverPrivilege")</dt></dl> | Necesario para cargar o descargar un controlador de dispositivo. <br /> Derecho de usuario: cargue y descargue los controladores de dispositivo.<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>TEXT("SeLockMemoryPrivilege")</dt></dl> | Necesario para bloquear páginas físicas en memoria. <br /> Derecho de usuario: bloquear páginas en memoria.<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>TEXT("SeMachineAccountPrivilege")</dt></dl> | Necesario para crear una cuenta de equipo. <br /> Derecho de usuario: agregue estaciones de trabajo al dominio.<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>TEXT("SeManageVolumePrivilege")</dt></dl> | Necesario para habilitar los privilegios de administración de volúmenes. <br /> Derecho de usuario: administre los archivos de un volumen.<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>TEXT("SeProfileSingleProcessPrivilege")</dt></dl> | Necesario para recopilar información de generación de perfiles para un único proceso. <br /> Derecho de usuario: perfil de proceso único.<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl><dt><strong>SE_RELABEL_NAME</strong></dt><dt>TEXT("SeRelabelPrivilege")</dt></dl> | Necesario para modificar el nivel de integridad obligatorio de un objeto .<br /> Derecho de usuario: modifique una etiqueta de objeto.<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>TEXT("SeRemoteShutdownPrivilege")</dt></dl> | Necesario para apagar un sistema mediante una solicitud de red. <br /> Derecho de usuario: forzar el apagado desde un sistema remoto.<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl><dt><strong>SE_RESTORE_NAME</strong></dt><dt>TEXT("SeRestorePrivilege")</dt></dl> | Necesario para realizar operaciones de restauración. Este privilegio hace que el sistema conceda todo el control de acceso de escritura a cualquier archivo, independientemente de la ACL especificada para el archivo. Cualquier solicitud de acceso que no sea de escritura se sigue evaluando con la ACL. Además, este privilegio le permite establecer cualquier SID de grupo o usuario válido como propietario de un archivo. La función <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> requiere este privilegio. Si se mantiene este privilegio, se conceden los siguientes derechos de acceso:<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>DELETE</li></ul>Derecho de usuario: restaurar archivos y directorios.<br />Si el archivo se encuentra en una unidad extraíble y la opción "Auditar Storage extraíble" está habilitada, el SE_SECURITY_NAME debe tener ACCESS_SYSTEM_SECURITY.<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl><dt><strong>SE_SECURITY_NAME</strong></dt><dt>TEXT("SeSecurityPrivilege")</dt></dl> | Necesario para realizar una serie de funciones relacionadas con la seguridad, como controlar y ver mensajes de auditoría. Este privilegio identifica a su titular como operador de seguridad. <br /> Derecho de usuario: administre el registro de auditoría y seguridad.<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl><dt><strong>SE_SHUTDOWN_NAME</strong></dt><dt>TEXT("SeShutdownPrivilege")</dt></dl> | Necesario para apagar un sistema local. <br /> Derecho de usuario: apague el sistema.<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl><dt><strong>SE_SYNC_AGENT_NAME</strong></dt><dt>TEXT("SeSyncAgentPrivilege")</dt></dl> | Necesario para que un controlador de dominio use los <a href="/windows/desktop/SecGloss/l-gly"><em>servicios ligeros de sincronización de directorios del Protocolo</em></a> ligero de acceso a directorios. Este privilegio permite que el titular lea todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y propiedades. De forma predeterminada, se asigna a las cuentas Administrador y LocalSystem en controladores de dominio. <br /> Derecho de usuario: sincronice los datos del servicio de directorio.<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl><dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt><dt>TEXT("SeSystemEnvironmentPrivilege")</dt></dl> | Necesario para modificar la RAM no volátil de los sistemas que usan este tipo de memoria para almacenar información de configuración. <br /> Derecho de usuario: modifique los valores del entorno de firmware.<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl><dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt><dt>TEXT("SeSystemProfilePrivilege")</dt></dl> | Necesario para recopilar información de generación de perfiles para todo el sistema. <br /> Derecho de usuario: rendimiento del sistema de perfiles.<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl><dt><strong>SE_SYSTEMTIME_NAME</strong></dt><dt>TEXT("SeSystemtimePrivilege")</dt></dl> | Necesario para modificar la hora del sistema. <br /> Derecho de usuario: cambie la hora del sistema.<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl><dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt><dt>TEXT("SeTakeOwnershipPrivilege")</dt></dl> | Necesario para tomar posesión de un objeto sin que se le conceda acceso discrecional. Este privilegio permite establecer el valor del propietario solo en los valores que el titular puede asignar legítimamente como propietario de un objeto. <br /> Derecho de usuario: tome posesión de archivos u otros objetos.<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl><dt><strong>SE_TCB_NAME</strong></dt><dt>TEXT("SeTcbPrivilege")</dt></dl> | Este privilegio identifica a su titular como parte de la base de equipos de confianza. A algunos subsistemas protegidos de confianza se les concede este privilegio. <br /> Derecho de usuario: actúa como parte del sistema operativo.<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl><dt><strong>SE_TIME_ZONE_NAME</strong></dt><dt>TEXT("SeTimeZonePrivilege")</dt></dl> | Necesario para ajustar la zona horaria asociada al reloj interno del equipo.<br /> Derecho de usuario: cambie la zona horaria.<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl><dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt><dt>TEXT("SeTrustedCredManAccessPrivilege")</dt></dl> | Necesario para acceder a Administrador de credenciales como llamador de confianza.<br /> Derecho de usuario: acceda Administrador de credenciales como llamador de confianza.<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl><dt><strong>SE_UNDOCK_NAME</strong></dt><dt>TEXT("SeUndockPrivilege")</dt></dl> | Necesario para desacoplar un equipo portátil.<br /> Derecho de usuario: quite el equipo de la estación de acoplamiento.<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl><dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt><dt>TEXT("SeUnsolicitedInputPrivilege")</dt></dl> | Necesario para leer la entrada no solicitada desde un <a href="/windows/desktop/SecGloss/t-gly"><em>dispositivo terminal.</em></a><br /> Derecho de usuario: no aplicable.<br /> | 




## <a name="remarks"></a>Observaciones

Las constantes de privilegios se definen como cadenas en Winnt.h. Por ejemplo, la SE \_ AUDIT NAME se define como \_ "SeAuditPrivilege".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Privilegios](privileges.md)
</dt> </dl>

