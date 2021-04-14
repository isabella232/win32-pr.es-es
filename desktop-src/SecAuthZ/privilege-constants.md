---
Description: Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a las cuentas de usuario y de grupo. Cada privilegio de usuario incluye los que se conceden al usuario y a los grupos a los que pertenece el usuario.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilegio (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 801eccb2f42ccf27b45bc5628a32cee3de994bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653871"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilegio (autorización)

Los privilegios determinan el tipo de operaciones del sistema que puede realizar una cuenta de usuario. Un administrador asigna privilegios a las cuentas de usuario y de grupo. Entre los privilegios de cada usuario se incluyen los concedidos al usuario y a los grupos a los que pertenece el usuario.

Las funciones que obtienen y ajustan los privilegios de un [*token de acceso*](/windows/desktop/SecGloss/a-gly) usan el tipo de [*identificador local único*](/windows/desktop/SecGloss/l-gly) (LUID) para identificar los privilegios. Utilice la función [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para determinar el [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) en el sistema local que corresponde a una constante de privilegio. Utilice la función [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para convertir un **LUID** en su constante de cadena correspondiente.

El sistema operativo representa un privilegio mediante el uso de la cadena que sigue a "derecho de usuario" en la columna Descripción de la tabla siguiente. El sistema operativo muestra las cadenas de derecho de usuario en la columna **Directiva** del nodo **asignación de derechos de usuario** del complemento configuración de seguridad local de Microsoft Management Console (MMC).

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
Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) en github.

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
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>texto ( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obligatorio para asignar el <a href="/windows/desktop/SecGloss/p-gly"><em>token principal</em></a> de un proceso. <br/> Derecho de usuario: reemplazar un token de nivel de proceso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong>SE_AUDIT_NAME</strong></dt> <dt>texto ( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para generar entradas del registro de auditoría. Conceda este privilegio a los servidores seguros. <br/> Derecho de usuario: generar auditorías de seguridad.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong>SE_BACKUP_NAME</strong></dt> <dt>texto ( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requerido para realizar operaciones de copia de seguridad. Este privilegio hace que el sistema conceda todo el control de acceso de lectura a cualquier archivo, independientemente de la <a href="/windows/desktop/SecGloss/a-gly"><em>lista de control de acceso</em></a> (ACL) especificada para el archivo. Cualquier solicitud de acceso que no sea de lectura todavía se evalúa con la ACL. Las funciones <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> y <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>requieren este privilegio. Se conceden los siguientes derechos de acceso si se mantiene este privilegio:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Derecho de usuario: copia de seguridad de archivos y directorios.<br/>Si el archivo se encuentra en una unidad extraíble y la opción "auditar almacenamiento extraíble" está habilitada, es necesario que el SE_SECURITY_NAME tenga ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>texto ( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requerido para recibir notificaciones de cambios en archivos o directorios. Este privilegio también hace que el sistema omita todas las comprobaciones de acceso transversal. Está habilitada de forma predeterminada para todos los usuarios. <br/> Derecho de usuario: Omitir comprobación de recorrido.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>texto ( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para crear objetos de asignación de archivo con nombre en el espacio de nombres global durante Terminal Services sesiones. Este privilegio está habilitado de forma predeterminada para los administradores, los servicios y la cuenta de sistema local.<br/> Derecho de usuario: crear objetos globales.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>texto ( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para crear un archivo de paginación. <br/> Derecho de usuario: crear un archivo de paginación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>texto ( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requerido para crear un objeto permanente. <br/> Derecho de usuario: crear objetos compartidos permanentes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>texto ( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para crear un vínculo simbólico.<br/> Derecho de usuario: crear vínculos simbólicos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>texto ( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para crear un token primario. <br/> Derecho de usuario: cree un objeto de token.<br/> No se puede Agregar este privilegio a una cuenta de usuario con la &quot; Directiva crear un objeto de token &quot; . Además, no puede Agregar este privilegio a un proceso de propiedad mediante las API de Windows. <strong>Windows Server 2003 y Windows XP con SP1 y versiones anteriores:</strong> Las API de Windows pueden agregar este privilegio a un proceso de propiedad.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong>SE_DEBUG_NAME</strong></dt> <dt>texto ( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para depurar y ajustar la memoria de un proceso que pertenece a otra cuenta. <br/> Derecho de usuario: depurar programas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>texto ( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para obtener un token de suplantación para otro usuario de la misma sesión. <br/> Derecho de usuario: suplantar a otros usuarios.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>texto ( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obligatorio para marcar las cuentas de usuario y de equipo como de confianza para la delegación.<br/> Derecho de usuario: permitir que las cuentas de equipo y de usuario sean de confianza para la delegación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>texto ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Requerido para suplantar.<br/> Derecho de usuario: suplantar a un cliente tras la autenticación.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>texto ( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para aumentar la prioridad base de un proceso. <br/> Derecho de usuario: aumentar la prioridad de programación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>texto ( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para aumentar la cuota asignada a un proceso. <br/> Derecho de usuario: ajuste de las cuotas de memoria para un proceso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>texto ( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para asignar más memoria a las aplicaciones que se ejecutan en el contexto de los usuarios.<br/> Derecho de usuario: aumentar un espacio de trabajo del proceso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>texto ( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para cargar o descargar un controlador de dispositivo. <br/> Derecho de usuario: cargar y descargar controladores de dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>texto ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para bloquear páginas físicas en la memoria. <br/> Derecho de usuario: bloquear páginas en la memoria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>texto ( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para crear una cuenta de equipo. <br/> Derecho de usuario: agregar estaciones de trabajo al dominio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>texto ( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para habilitar los privilegios de administración de volúmenes. <br/> Derecho de usuario: administre los archivos de un volumen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>texto ( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para recopilar información de generación de perfiles para un único proceso. <br/> Derecho de usuario: generar perfiles de un solo proceso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong>SE_RELABEL_NAME</strong></dt> <dt>texto ( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar el nivel de integridad obligatorio de un objeto.<br/> Derecho de usuario: modifique una etiqueta de objeto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>texto ( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para apagar un sistema mediante una solicitud de red. <br/> Derecho de usuario: forzar el cierre desde un sistema remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong>SE_RESTORE_NAME</strong></dt> <dt>texto ( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para realizar operaciones de restauración. Este privilegio hace que el sistema conceda todo el control de acceso de escritura a cualquier archivo, independientemente de la ACL especificada para el archivo. Cualquier solicitud de acceso que no sea de escritura todavía se evalúa con la ACL. Además, este privilegio le permite establecer cualquier SID de usuario o grupo válido como propietario de un archivo. Este privilegio es necesario para la función <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegLoadKey</strong></a> . Se conceden los siguientes derechos de acceso si se mantiene este privilegio:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>Delete</li>
</ul>
Derecho de usuario: restaurar archivos y directorios.<br/>Si el archivo se encuentra en una unidad extraíble y la opción "auditar almacenamiento extraíble" está habilitada, es necesario que el SE_SECURITY_NAME tenga ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong></strong></dt> <dt>Texto SE_SECURITY_NAME ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para realizar una serie de funciones relacionadas con la seguridad, como el control y la visualización de los mensajes de auditoría. Este privilegio identifica su titular como operador de seguridad. <br/> Derecho de usuario: Administrar registro de seguridad y auditoría.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>texto ( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para apagar un sistema local. <br/> Derecho de usuario: Apague el sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>texto ( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para que un controlador de dominio use los servicios de sincronización de directorios del <a href="/windows/desktop/SecGloss/l-gly"><em>Protocolo ligero de acceso a directorios</em></a> . Este privilegio permite al titular leer todos los objetos y propiedades del directorio, independientemente de la protección de los objetos y las propiedades. De forma predeterminada, se asigna a las cuentas de administrador y LocalSystem en los controladores de dominio. <br/> Derecho de usuario: sincronizar los datos del servicio de directorio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>texto ( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar la memoria RAM no volátil de los sistemas que utilizan este tipo de memoria para almacenar información de configuración. <br/> Derecho de usuario: modifique los valores de entorno de firmware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>texto ( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para recopilar información de generación de perfiles para todo el sistema. <br/> Derecho de usuario: generar perfiles del rendimiento del sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>texto ( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para modificar la hora del sistema. <br/> Derecho de usuario: cambiar la hora del sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>texto ( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Se requiere para tomar posesión de un objeto sin que se le conceda acceso discrecional. Este privilegio permite que el valor de propietario se establezca únicamente en los valores que el titular puede asignar legítimamente como propietario de un objeto. <br/> Derecho de usuario: tomar posesión de archivos u otros objetos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong>SE_TCB_NAME</strong></dt> <dt>texto ( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Este privilegio identifica su titular como parte de la base del equipo de confianza. A algunos subsistemas protegidos de confianza se les concede este privilegio. <br/> Derecho de usuario: actuar como parte del sistema operativo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>texto ( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para ajustar la zona horaria asociada con el reloj interno del equipo.<br/> Derecho de usuario: cambie la zona horaria.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>texto ( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para tener acceso al administrador de credenciales como un llamador de confianza.<br/> Derecho de usuario: acceder al administrador de credenciales como un llamador de confianza.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>texto ( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para desacoplar un equipo portátil.<br/> Derecho de usuario: quitar el equipo de la estación de acoplamiento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>texto ( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necesario para leer la entrada no solicitada de un dispositivo <a href="/windows/desktop/SecGloss/t-gly"><em>terminal</em></a> .<br/> Derecho de usuario: no aplicable.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Las constantes de privilegio se definen como cadenas en Winnt. h. Por ejemplo, la \_ constante de nombre de auditoría se \_ define como "SeAuditPrivilege".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Privilegios](privileges.md)
</dt> </dl>

