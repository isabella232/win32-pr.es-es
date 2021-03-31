---
description: El parámetro strPrivilege del método SWbemPrivilegeSet. AddAsString y el parámetro iPrivilege de SWbemPrivilegeSet. Add requieren cadenas de privilegios de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilegios (Wbemdisp. h)
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
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818046"
---
# <a name="privilege-constants"></a>Constantes de privilegio

El parámetro *strPrivilege* del método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) y el parámetro *iPrivilege* de [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) requieren cadenas de privilegios de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Para obtener más información sobre cómo usar las constantes de privilegios, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).

Las siguientes constantes se definen en [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). La lista siguiente incluye las constantes equivalentes para C++ y las cadenas para el scripting. Para formar el nombre corto de scripting, quite "se" y "privileged" del nombre de la constante de C++.

En el ejemplo de código de VBScript siguiente se muestra cómo habilitar el privilegio RemoteShutdown en un script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Muchos métodos WMI requieren que se habiliten uno o varios permisos. Si una cuenta no tiene un privilegio, no se puede habilitar para la llamada al método.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Constante de C++ **: \_ se \_ crea \_ el nombre del token** cadena: **SeCreateTokenPrivilege**

Nombre corto de scripting: **CreateToken**

Se requiere para crear un objeto de token principal.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Constante de C++: **SeAssignPrimaryTokenPrivilege** cadena: **SeAssignPrimaryTokenPrivilege**

Nombre corto de scripting: **AssignPrimaryToken**

Necesario para reemplazar un token de nivel de proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0X3)
</dt> <dt>



Constante de C++: **se \_ bloqueó \_ \_ el nombre de memoria** cadena: **SeLockMemoryPrivilege**

Nombre corto de scripting: **LockMemory**

Necesario para bloquear páginas en la memoria.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Constante de C++ **: \_ se \_ aumenta \_ el nombre de cuota** cadena: **SeIncreaseQuotaPrivilege**

Nombre corto de scripting: **IncreaseQuotaPrivilege**

Necesario para ajustar las cuotas de memoria de un proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0X5)
</dt> <dt>



Constante de C++: se trata de una cadena de  **nombre de \_ \_ cuenta \_ de macine** : SeMachineAccountPrivilege

Nombre corto de scripting: **MachineAccount**

Necesario para agregar estaciones de trabajo a un dominio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Constante de C++: se trata de la cadena de **\_ \_ nombre de TCB** : **SeTcbPrivilege**

Nombre corto de scripting: **TCB**

Necesario para actuar como parte del sistema operativo. El titular forma parte de la base del equipo de confianza.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0X7)
</dt> <dt>



Constante de C++: se trata de una cadena de **\_ \_ nombre de seguridad** : **SeSecurityPrivilege**

Nombre corto de scripting: **seguridad**

Necesario para administrar la auditoría y el registro de seguridad de NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Constante de C++ **: \_ se \_ toma \_ el nombre de propiedad** cadena: **SeTakeOwnershipPrivilege**

Nombre corto de scripting: **TakeOwnerShip**

Se requiere para asumir la propiedad de los archivos u otros objetos sin tener una [*entrada Access Control*](/windows/desktop/SecGloss/a-gly) (ACE) en la *lista de control de acceso discrecional* (DACL).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Constante de C++: **se \_ carga el \_ controlador** cadena: **SeLoadDriverPrivilege**

Nombre corto de scripting: **LoadDriver**

Necesario para cargar o descargar un controlador de dispositivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Constante de C++: **se trata \_ del \_ \_ nombre de Perfil de sistema** de la cadena: **SeSystemProfilePrivilege**

Nombre corto de scripting: **SystemProfile**

Necesario para recopilar información de perfil sobre el rendimiento del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Constante de C++ **: \_ se** trata de una \_ cadena de nombre SYSTEMTIME: **SeSystemtimePrivilege**

Nombre corto de scripting: **SYSTEMTIME**

Necesario para cambiar la hora del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Constante de C++: cadena de **\_ \_ \_ \_ nombre de proceso único de Profs** : **SeProfileSingleProcessPrivilege**

Nombre corto de scripting: **ProfileSingleProcess**

Necesario para recopilar información de perfil para un único proceso.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Constante de C++: nombre de la **\_ \_ \_ \_ prioridad base de se Inc** . cadena: **SeIncreaseBasePriorityPrivilege**

Nombre corto de scripting: **IncreaseBasePriority**

Necesario para aumentar la prioridad de programación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Constante de C++ **: \_ se \_ crea \_ el nombre** de archivo de paginación cadena: **SeCreatePagefilePrivilege**

Nombre corto de scripting: **CreatePagefile**

Se requiere para crear un archivo de paginación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Constante de C++: se crea una cadena de **\_ \_ \_ nombre permanente** : **SeCreatePermanentPrivilege**

Nombre corto de scripting: **CreatePermanent**

Necesario para crear objetos compartidos permanentes.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Constante de C++ **: \_ \_ nombre de copia de seguridad de se** cadena: **SeBackupPrivilege**

Nombre corto de scripting: **copia de seguridad**

Necesario para realizar una copia de seguridad de archivos y directorios, independientemente de la ACL especificada para el archivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Constante de C++: **se ha restaurado la cadena de \_ \_ nombre** : **SeRestorePrivilege**

Nombre corto de scripting: **restore**

Necesario para restaurar archivos y directorios, independientemente de la ACL especificada para el archivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0X12)
</dt> <dt>



Constante de C++: **se ha \_ cerrado \_ el nombre** de la cadena: **SeShutdownPrivilege**

Nombre corto de scripting: **apagado**

Necesario para apagar el sistema local.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Constante de C++: **se ha \_ depurado \_ el nombre** cadena: **SeDebugPrivilege**

Nombre corto de scripting: **Debug**

Necesario para depurar y ajustar la memoria de un proceso que pertenece a otra cuenta.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Constante de C++: se trata de una cadena de **\_ \_ nombre de auditoría** : **SeAuditPrivilege**

Nombre corto de scripting: **Auditoría**

Necesario para generar entradas de auditoría en el registro de seguridad de NT. Solo los servidores seguros deben tener este privilegio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Constante de C++: **se trata \_ del \_ \_ nombre del entorno del sistema** de la cadena: **SeSystemEnvironmentPrivilege**

Nombre corto de scripting: **SystemEnvironment**

Necesario para modificar la RAM no volátil de los sistemas que utilizan este tipo de memoria para almacenar los datos de configuración.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Constante de C++: **se ha \_ cambiado \_ \_ el nombre de notificación** cadena: **SeChangeNotifyPrivilege**

Nombre corto de scripting: **ChangeNotify**

Requerido para recibir notificaciones de cambios en archivos o directorios y omitir las comprobaciones de acceso transversal. Este privilegio está habilitado de forma predeterminada para todos los usuarios.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Constante de C++: cadena de **\_ \_ \_ nombre de apagado remoto** : **SeRemoteShutdownPrivilege**

Nombre corto de scripting: **RemoteShutdown**

Necesario para apagar un equipo remoto.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Constante de C++: **se \_ desacopla \_ el nombre** de la cadena: **SeUndockPrivilege**

Nombre corto de scripting: **desacoplar**

Necesario para quitar un portátil de una estación de acoplamiento.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Constante de C++: **se ha sincronizado la cadena de \_ \_ \_ nombre del agente** : **SeSyncAgentPrivilege**

Nombre corto de scripting: **SyncAgent**

Necesario para sincronizar los datos del servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Constante de C++: se habilita la cadena de  **\_ \_ \_ nombre de delegación** : SeEnableDelegationPrivilege

Nombre corto de scripting: **EnableDelegation**

Se requiere para habilitar la confianza en las cuentas de equipo y de usuario para la delegación.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Constante de C++ **: \_ se \_ administra \_ el nombre de volumen** cadena: **SeManageVolumePrivilege**

Nombre corto de scripting: **ManageVolume**

Necesario para realizar tareas de mantenimiento del volumen.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de constantes de API](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Ejecutar operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

