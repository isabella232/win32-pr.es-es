---
description: El parámetro strPrivilege del método SWbemPrivilegeSet.AddAsString y el parámetro iPrivilege para SWbemPrivilegeSet.Add requieren cadenas de privilegios de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilegios (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 38d104c99885d4328ce8b12413e91607655ab1e260a61b511e3ea4a600b80b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131027"
---
# <a name="privilege-constants"></a>Constantes de privilegios

El parámetro *strPrivilege* del método [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) y el parámetro *iPrivilege* para [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) requieren cadenas de privilegios [de WbemPrivilegeEnum.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Para obtener más información sobre cómo usar constantes de privilegios, vea [Ejecutar operaciones con privilegios.](executing-privileged-operations.md)

Las siguientes constantes se definen en [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). En la lista siguiente se incluyen las constantes equivalentes para C++ y cadenas para scripting. Para formar el nombre corto de scripting, quite "Se" y "Privilege" del nombre de constante de C++.

En el siguiente ejemplo de código de VBScript se muestra cómo habilitar el privilegio RemoteShutdown en un script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Muchos métodos WMI requieren que se habilite uno o varios permisos. Si no se ha concedido un privilegio a una cuenta, no se puede habilitar para la llamada al método .

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Constante de C++: **SE cadena CREATE TOKEN \_ \_ \_ NAME:** **SeCreateTokenPrivilege**

Nombre corto de scripting: **CreateToken**

Necesario para crear un objeto de token principal.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Constante de C++: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**

Nombre corto de scripting: **AssignPrimaryToken**

Necesario para reemplazar un token de nivel de proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Constante de C++: **SE \_ LOCK MEMORY \_ \_ NAME** string: **SeLockMemoryPrivilege**

Nombre corto de scripting: **LockMemory**

Necesario para bloquear páginas en memoria.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Constante de C++: **SE cadena INCREASE QUOTA \_ \_ \_ NAME:** **SeIncreaseQuotaPrivilege**

Nombre corto de scripting: **IncreaseQuotaPrivilege**

Necesario para ajustar las cuotas de memoria de un proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Constante de C++: **SE cadena DE NOMBRE DE CUENTA \_ \_ \_ DE MACINE:** **SeMachineAccountPrivilege**

Nombre corto de scripting: **MachineAccount**

Necesario para agregar estaciones de trabajo a un dominio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Constante de C++: **SE \_ cadena TCB \_ NAME:** **SeTcbPrivilege**

Nombre corto de scripting: **Tcb**

Necesario para actuar como parte del sistema operativo. El titular forma parte de la base de equipos de confianza.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Constante de C++: **SE \_ cadena SECURITY \_ NAME:** **SeSecurityPrivilege**

Nombre corto de scripting: **Seguridad**

Necesario para administrar la auditoría y el registro de seguridad de NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Constante de C++: **SE \_ TAKE OWNERSHIP \_ \_ NAME** string: **SeTakeOwnershipPrivilege**

Nombre corto de scripting: **TakeOwnership**

Se requiere para asumir la propiedad de archivos u otros objetos sin tener una Access Control [*Entry*](/windows/desktop/SecGloss/a-gly) (ACE) en la lista *de control* de acceso discrecional (DACL).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Constante de C++: **SE \_ load \_ driver** string: **SeLoadDriverPrivilege**

Nombre corto de scripting: **LoadDriver**

Necesario para cargar o descargar un controlador de dispositivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Constante de C++: **SE \_ system profile \_ \_ name** string: **SeSystemProfilePrivilege**

Nombre corto de scripting: **SystemProfile**

Necesario para recopilar información de perfil sobre el rendimiento del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Constante de C++: **SE \_ cadena SYSTEMTIME** \_ NAME: **SeSystemtimePrivilege**

Nombre corto de scripting: **Systemtime**

Necesario para cambiar la hora del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Constante de C++: **SE DE PROF SINGLE PROCESS \_ \_ \_ \_ NAME** string: **SeProfileSingleProcessPrivilege**

Nombre corto de scripting: **ProfileSingleProcess**

Necesario para recopilar información de perfil para un único proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Constante de C++: **SE INC BASE PRIORITY \_ \_ \_ \_ NAME** string: **SeIncreaseBasePriorityPrivilege**

Nombre corto de scripting: **IncreaseBasePriority**

Necesario para aumentar la prioridad de programación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Constante de C++: **SE \_ cadena CREATE \_ PAGEFILE \_ NAME:** **SeCreatePagefilePrivilege**

Nombre corto de scripting: **CreatePagefile**

Necesario para crear un archivo de paginación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Constante de C++: **SE cadena CREATE PERMANENT \_ \_ \_ NAME:** **SeCreatePermanentPrivilege**

Nombre corto de scripting: **CreatePermanent**

Necesario para crear objetos compartidos permanentes.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Constante de C++: **SE \_ BACKUP \_ NAME** string: **SeBackupPrivilege**

Nombre corto de scripting: Copia de **seguridad**

Necesario para realizar copias de seguridad de archivos y directorios, independientemente de la ACL especificada para el archivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Constante de C++: **SE \_ cadena RESTORE \_ NAME:** **SeRestorePrivilege**

Nombre corto de scripting: **Restaurar**

Necesario para restaurar archivos y directorios, independientemente de la ACL especificada para el archivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Constante de C++: **SE \_ cadena SHUTDOWN \_ NAME:** **SeShutdownPrivilege**

Nombre corto de scripting: **Shutdown**

Necesario para apagar el sistema local.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Constante de C++: **SE \_ debug \_ name** string: **SeDebugPrivilege**

Nombre corto de scripting: **Depurar**

Necesario para depurar y ajustar la memoria de un proceso propiedad de otra cuenta.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Constante de C++: **SE \_ AUDIT \_ NAME** string: **SeAuditPrivilege**

Nombre corto de scripting: **Audit**

Necesario para generar entradas de auditoría en el registro de seguridad de NT. Solo los servidores seguros deben tener este privilegio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Constante de C++: **SE cadena SYSTEM ENVIRONMENT \_ \_ \_ NAME:** **SeSystemEnvironmentPrivilege**

Nombre corto de scripting: **SystemEnvironment**

Necesario para modificar la RAM no volátil de los sistemas que usan este tipo de memoria para almacenar los datos de configuración.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Constante de C++: **SE cadena CHANGE NOTIFY \_ \_ \_ NAME:** **SeChangeNotifyPrivilege**

Nombre corto de scripting: **ChangeNotify**

Se requiere para recibir notificaciones de cambios en archivos o directorios y omitir las comprobaciones de acceso transversal. Este privilegio está habilitado de forma predeterminada para todos los usuarios.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Constante de C++: **SE \_ REMOTE SHUTDOWN \_ \_ NAME** string: **SeRemoteShutdownPrivilege**

Nombre corto de scripting: **RemoteShutdown**

Necesario para apagar un equipo remoto.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Constante de C++: **SE \_ cadena UNDOCK \_ NAME:** **SeUndockPrivilege**

Nombre corto de scripting: **Desacoplar**

Necesario para quitar un portátil de una estación de acoplamiento.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Constante de C++: **SE SYNC AGENT NAME \_ \_ \_ string:** **SeSyncAgentPrivilege**

Nombre corto de scripting: **SyncAgent**

Necesario para sincronizar los datos del servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Constante de C++: **SE cadena ENABLE DELEGATION \_ \_ \_ NAME:** **SeEnableDelegationPrivilege**

Nombre corto de scripting: **EnableDelegation**

Necesario para permitir que las cuentas de equipo y usuario sean de confianza para la delegación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Constante de C++: **SE cadena MANAGE VOLUME \_ \_ \_ NAME:** **SeManageVolumePrivilege**

Nombre corto de scripting: **ManageVolume**

Necesario para realizar tareas de mantenimiento del volumen.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de API de scripting](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Ejecución de operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

