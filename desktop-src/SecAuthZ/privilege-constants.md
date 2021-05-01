---
Description: Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilegios (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327160"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilegios (autorización)

Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a cuentas de usuario y grupo. Los privilegios de cada usuario incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

Las funciones que obtienen y ajustan los privilegios de un [*token*](/windows/desktop/SecGloss/a-gly) de acceso usan el tipo de identificador único [*local*](/windows/desktop/SecGloss/l-gly) (LUID) para identificar los privilegios. Use la [**función LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para determinar el [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) en el sistema local que corresponde a una constante de privilegios. Use la [**función LookupPrivilegeName para**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) convertir **un LUID** en su constante de cadena correspondiente.

El sistema operativo representa un privilegio mediante la cadena que sigue a "Derecho de usuario" en la columna Descripción de la tabla siguiente. El sistema operativo muestra las cadenas derechas del usuario en la columna Directiva del nodo **Asignación** de derechos de usuario del complemento Configuración de seguridad Microsoft Management Console local (MMC). 

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
Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) en GitHub.

## <a name="constants"></a>Constantes


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para asignar el <a href="/windows/desktop/SecGloss/p-gly"><em>token principal</em></a> de un proceso. <br/> Derecho de usuario: reemplace un token de nivel de proceso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong>SE_AUDIT_NAME</strong></dt> <dt>TEXT( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para generar entradas de registro de auditoría. Dé este privilegio a los servidores seguros. <br/> Derecho de usuario: genere auditorías de seguridad.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong>SE_BACKUP_NAME</strong></dt> <dt>TEXT( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para realizar operaciones de copia de seguridad. Este privilegio hace que el sistema conceda todo el control de acceso de lectura a cualquier archivo, independientemente de la lista de <a href="/windows/desktop/SecGloss/a-gly"><em>control</em></a> de acceso (ACL) especificada para el archivo. Cualquier solicitud de acceso que no sea de lectura se sigue evaluando con la ACL. Este privilegio lo requieren las <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>funciones RegSaveKey</strong></a> <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>y RegSaveKeyEx.</strong></a> Si se mantiene este privilegio, se conceden los siguientes derechos de acceso:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Derecho de usuario: haga una copia de seguridad de archivos y directorios.<br/>Si el archivo se encuentra en una unidad extraíble y el "Auditar almacenamiento extraíble" está habilitado, el SE_SECURITY_NAME debe tener ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>TEXT( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para recibir notificaciones de cambios en archivos o directorios. Este privilegio también hace que el sistema omita todas las comprobaciones de acceso transversal. Está habilitada de forma predeterminada para todos los usuarios. <br/> Derecho de usuario: omitir la comprobación de recorrido.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>TEXT( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear objetos de asignación de archivos con nombre en el espacio de nombres global durante las sesiones de Terminal Services. Este privilegio está habilitado de forma predeterminada para los administradores, los servicios y la cuenta del sistema local.<br/> Derecho de usuario: cree objetos globales.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear un archivo de paginación. <br/> Derecho de usuario: cree un archivo de paginación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear un objeto permanente. <br/> Derecho de usuario: cree objetos compartidos permanentes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>TEXT( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear un vínculo simbólico.<br/> Derecho de usuario: cree vínculos simbólicos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear un token principal. <br/> Derecho de usuario: cree un objeto de token.<br/> No puede agregar este privilegio a una cuenta de usuario con la &quot; directiva Crear un objeto de &quot; token. Además, no puede agregar este privilegio a un proceso propiedad mediante las API de Windows. <strong>Windows Server 2003 y Windows XP con SP1 y versiones anteriores:</strong> Las API de Windows pueden agregar este privilegio a un proceso de propiedad.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong>SE_DEBUG_NAME</strong></dt> <dt>TEXT( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para depurar y ajustar la memoria de un proceso propiedad de otra cuenta. <br/> Derecho de usuario: depurar programas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para obtener un token de suplantación para otro usuario en la misma sesión. <br/> Derecho de usuario: suplantar a otros usuarios.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>TEXT( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para marcar las cuentas de usuario y equipo como de confianza para la delegación.<br/> Derecho de usuario: permite que las cuentas de equipo y usuario sean de confianza para la delegación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para suplantar.<br/> Derecho de usuario: suplantar un cliente después de la autenticación.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para aumentar la prioridad base de un proceso. <br/> Derecho de usuario: aumente la prioridad de programación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para aumentar la cuota asignada a un proceso. <br/> Derecho de usuario: ajuste las cuotas de memoria de un proceso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para asignar más memoria a las aplicaciones que se ejecutan en el contexto de los usuarios.<br/> Derecho de usuario: aumente un conjunto de trabajo de proceso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>TEXT( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para cargar o descargar un controlador de dispositivo. <br/> Derecho de usuario: cargue y descargue los controladores de dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>TEXT( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para bloquear páginas físicas en memoria. <br/> Derecho de usuario: bloquear páginas en memoria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>TEXT( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para crear una cuenta de equipo. <br/> Derecho de usuario: agregue estaciones de trabajo al dominio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>TEXT( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para habilitar los privilegios de administración de volúmenes. <br/> Derecho de usuario: administre los archivos de un volumen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>TEXT( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para recopilar información de generación de perfiles para un único proceso. <br/> Derecho de usuario: perfil de proceso único.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong>SE_RELABEL_NAME</strong></dt> <dt>TEXT( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar el nivel de integridad obligatorio de un objeto .<br/> Derecho de usuario: modifique una etiqueta de objeto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para apagar un sistema mediante una solicitud de red. <br/> Derecho de usuario: forzar el apagado desde un sistema remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong>SE_RESTORE_NAME</strong></dt> <dt>TEXT( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para realizar operaciones de restauración. Este privilegio hace que el sistema conceda todo el control de acceso de escritura a cualquier archivo, independientemente de la ACL especificada para el archivo. Cualquier solicitud de acceso que no sea de escritura se sigue evaluando con la ACL. Además, este privilegio le permite establecer cualquier SID de grupo o usuario válido como propietario de un archivo. La función <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> requiere este privilegio. Si se mantiene este privilegio, se conceden los siguientes derechos de acceso:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Derecho de usuario: restaure archivos y directorios.<br/>Si el archivo se encuentra en una unidad extraíble y el "Auditar almacenamiento extraíble" está habilitado, el SE_SECURITY_NAME debe tener ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong>SE_SECURITY_NAME</strong></dt> <dt>TEXT( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para realizar una serie de funciones relacionadas con la seguridad, como controlar y ver mensajes de auditoría. Este privilegio identifica a su titular como operador de seguridad. <br/> Derecho de usuario: administre el registro de auditoría y seguridad.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para apagar un sistema local. <br/> Derecho de usuario: apague el sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>TEXT( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para que un controlador de dominio use los servicios de sincronización de <a href="/windows/desktop/SecGloss/l-gly"><em>directorios</em></a> del Protocolo ligero de acceso a directorios. Este privilegio permite al titular leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y propiedades. De forma predeterminada, se asigna a las cuentas Administrador y LocalSystem en controladores de dominio. <br/> Derecho de usuario: sincronice los datos del servicio de directorio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>TEXT( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar la RAM no volátil de los sistemas que usan este tipo de memoria para almacenar información de configuración. <br/> Derecho de usuario: modifique los valores del entorno de firmware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>TEXT( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para recopilar información de generación de perfiles para todo el sistema. <br/> Derecho de usuario: rendimiento del sistema de perfiles.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>TEXT( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar la hora del sistema. <br/> Derecho de usuario: cambie la hora del sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>TEXT( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para tomar posesión de un objeto sin que se le conceda acceso discrecional. Este privilegio permite establecer el valor del propietario solo en los valores que el titular puede asignar legítimamente como propietario de un objeto. <br/> Derecho de usuario: tome posesión de archivos u otros objetos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong>SE_TCB_NAME</strong></dt> <dt>TEXT( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Este privilegio identifica su titular como parte de la base de equipos de confianza. A algunos subsistemas protegidos de confianza se les concede este privilegio. <br/> Derecho de usuario: actúa como parte del sistema operativo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>TEXT( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para ajustar la zona horaria asociada al reloj interno del equipo.<br/> Derecho de usuario: cambie la zona horaria.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>TEXT( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para acceder a Administrador de credenciales como llamador de confianza.<br/> Derecho de usuario: acceda Administrador de credenciales como llamador de confianza.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>TEXT( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para desacoplar un equipo portátil.<br/> Derecho de usuario: quite el equipo de la estación de acoplamiento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>TEXT( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para leer la entrada no solicitada desde un <a href="/windows/desktop/SecGloss/t-gly"><em>dispositivo terminal.</em></a><br/> Derecho de usuario: no aplicable.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Las constantes de privilegios se definen como cadenas en Winnt.h. Por ejemplo, la constante SE \_ AUDIT NAME se define como \_ "SeAuditPrivilege".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Privilegios](privileges.md)
</dt> </dl>

