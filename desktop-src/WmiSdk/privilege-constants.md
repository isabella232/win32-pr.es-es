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
# <a name="privilege-constants"></a><span data-ttu-id="79a17-103">Constantes de privilegio</span><span class="sxs-lookup"><span data-stu-id="79a17-103">Privilege Constants</span></span>

<span data-ttu-id="79a17-104">El parámetro *strPrivilege* del método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) y el parámetro *iPrivilege* de [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) requieren cadenas de privilegios de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="79a17-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="79a17-105">Para obtener más información sobre cómo usar las constantes de privilegios, vea [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="79a17-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="79a17-106">Las siguientes constantes se definen en [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="79a17-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="79a17-107">La lista siguiente incluye las constantes equivalentes para C++ y las cadenas para el scripting.</span><span class="sxs-lookup"><span data-stu-id="79a17-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="79a17-108">Para formar el nombre corto de scripting, quite "se" y "privileged" del nombre de la constante de C++.</span><span class="sxs-lookup"><span data-stu-id="79a17-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="79a17-109">En el ejemplo de código de VBScript siguiente se muestra cómo habilitar el privilegio RemoteShutdown en un script.</span><span class="sxs-lookup"><span data-stu-id="79a17-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="79a17-110">Muchos métodos WMI requieren que se habiliten uno o varios permisos.</span><span class="sxs-lookup"><span data-stu-id="79a17-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="79a17-111">Si una cuenta no tiene un privilegio, no se puede habilitar para la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="79a17-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="79a17-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span><span class="sxs-lookup"><span data-stu-id="79a17-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="79a17-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-114">Constante de C++ **: \_ se \_ crea \_ el nombre del token** cadena: **SeCreateTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="79a17-115">Nombre corto de scripting: **CreateToken**</span><span class="sxs-lookup"><span data-stu-id="79a17-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="79a17-116">Se requiere para crear un objeto de token principal.</span><span class="sxs-lookup"><span data-stu-id="79a17-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="79a17-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-118">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="79a17-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-119">Constante de C++: **SeAssignPrimaryTokenPrivilege** cadena: **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="79a17-120">Nombre corto de scripting: **AssignPrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="79a17-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="79a17-121">Necesario para reemplazar un token de nivel de proceso.</span><span class="sxs-lookup"><span data-stu-id="79a17-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span><span class="sxs-lookup"><span data-stu-id="79a17-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-123">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="79a17-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-124">Constante de C++: **se \_ bloqueó \_ \_ el nombre de memoria** cadena: **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="79a17-125">Nombre corto de scripting: **LockMemory**</span><span class="sxs-lookup"><span data-stu-id="79a17-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="79a17-126">Necesario para bloquear páginas en la memoria.</span><span class="sxs-lookup"><span data-stu-id="79a17-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span><span class="sxs-lookup"><span data-stu-id="79a17-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="79a17-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-129">Constante de C++ **: \_ se \_ aumenta \_ el nombre de cuota** cadena: **SeIncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="79a17-130">Nombre corto de scripting: **IncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="79a17-131">Necesario para ajustar las cuotas de memoria de un proceso.</span><span class="sxs-lookup"><span data-stu-id="79a17-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span><span class="sxs-lookup"><span data-stu-id="79a17-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-133">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="79a17-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-134">Constante de C++: se trata de una cadena de  **nombre de \_ \_ cuenta \_ de macine** : SeMachineAccountPrivilege</span><span class="sxs-lookup"><span data-stu-id="79a17-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="79a17-135">Nombre corto de scripting: **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="79a17-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="79a17-136">Necesario para agregar estaciones de trabajo a un dominio.</span><span class="sxs-lookup"><span data-stu-id="79a17-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span><span class="sxs-lookup"><span data-stu-id="79a17-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="79a17-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-139">Constante de C++: se trata de la cadena de **\_ \_ nombre de TCB** : **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="79a17-140">Nombre corto de scripting: **TCB**</span><span class="sxs-lookup"><span data-stu-id="79a17-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="79a17-141">Necesario para actuar como parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="79a17-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="79a17-142">El titular forma parte de la base del equipo de confianza.</span><span class="sxs-lookup"><span data-stu-id="79a17-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span><span class="sxs-lookup"><span data-stu-id="79a17-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-144">7 (0X7)</span><span class="sxs-lookup"><span data-stu-id="79a17-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-145">Constante de C++: se trata de una cadena de **\_ \_ nombre de seguridad** : **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="79a17-146">Nombre corto de scripting: **seguridad**</span><span class="sxs-lookup"><span data-stu-id="79a17-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="79a17-147">Necesario para administrar la auditoría y el registro de seguridad de NT.</span><span class="sxs-lookup"><span data-stu-id="79a17-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="79a17-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="79a17-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-150">Constante de C++ **: \_ se \_ toma \_ el nombre de propiedad** cadena: **SeTakeOwnershipPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="79a17-151">Nombre corto de scripting: **TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="79a17-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="79a17-152">Se requiere para asumir la propiedad de los archivos u otros objetos sin tener una [*entrada Access Control*](/windows/desktop/SecGloss/a-gly) (ACE) en la *lista de control de acceso discrecional* (DACL).</span><span class="sxs-lookup"><span data-stu-id="79a17-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span><span class="sxs-lookup"><span data-stu-id="79a17-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="79a17-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-155">Constante de C++: **se \_ carga el \_ controlador** cadena: **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="79a17-156">Nombre corto de scripting: **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="79a17-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="79a17-157">Necesario para cargar o descargar un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a17-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="79a17-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-159">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="79a17-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-160">Constante de C++: **se trata \_ del \_ \_ nombre de Perfil de sistema** de la cadena: **SeSystemProfilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="79a17-161">Nombre corto de scripting: **SystemProfile**</span><span class="sxs-lookup"><span data-stu-id="79a17-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="79a17-162">Necesario para recopilar información de perfil sobre el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="79a17-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span><span class="sxs-lookup"><span data-stu-id="79a17-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="79a17-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-165">Constante de C++ **: \_ se** trata de una \_ cadena de nombre SYSTEMTIME: **SeSystemtimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="79a17-166">Nombre corto de scripting: **SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="79a17-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="79a17-167">Necesario para cambiar la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="79a17-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="79a17-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-169">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="79a17-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-170">Constante de C++: cadena de **\_ \_ \_ \_ nombre de proceso único de Profs** : **SeProfileSingleProcessPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="79a17-171">Nombre corto de scripting: **ProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="79a17-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="79a17-172">Necesario para recopilar información de perfil para un único proceso.</span><span class="sxs-lookup"><span data-stu-id="79a17-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="79a17-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="79a17-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-175">Constante de C++: nombre de la **\_ \_ \_ \_ prioridad base de se Inc** . cadena: **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="79a17-176">Nombre corto de scripting: **IncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="79a17-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="79a17-177">Necesario para aumentar la prioridad de programación.</span><span class="sxs-lookup"><span data-stu-id="79a17-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="79a17-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-179">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="79a17-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-180">Constante de C++ **: \_ se \_ crea \_ el nombre** de archivo de paginación cadena: **SeCreatePagefilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="79a17-181">Nombre corto de scripting: **CreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="79a17-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="79a17-182">Se requiere para crear un archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="79a17-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="79a17-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="79a17-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-185">Constante de C++: se crea una cadena de **\_ \_ \_ nombre permanente** : **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="79a17-186">Nombre corto de scripting: **CreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="79a17-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="79a17-187">Necesario para crear objetos compartidos permanentes.</span><span class="sxs-lookup"><span data-stu-id="79a17-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span><span class="sxs-lookup"><span data-stu-id="79a17-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="79a17-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-190">Constante de C++ **: \_ \_ nombre de copia de seguridad de se** cadena: **SeBackupPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="79a17-191">Nombre corto de scripting: **copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="79a17-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="79a17-192">Necesario para realizar una copia de seguridad de archivos y directorios, independientemente de la ACL especificada para el archivo.</span><span class="sxs-lookup"><span data-stu-id="79a17-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span><span class="sxs-lookup"><span data-stu-id="79a17-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="79a17-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-195">Constante de C++: **se ha restaurado la cadena de \_ \_ nombre** : **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="79a17-196">Nombre corto de scripting: **restore**</span><span class="sxs-lookup"><span data-stu-id="79a17-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="79a17-197">Necesario para restaurar archivos y directorios, independientemente de la ACL especificada para el archivo.</span><span class="sxs-lookup"><span data-stu-id="79a17-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span><span class="sxs-lookup"><span data-stu-id="79a17-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-199">18 (0X12)</span><span class="sxs-lookup"><span data-stu-id="79a17-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-200">Constante de C++: **se ha \_ cerrado \_ el nombre** de la cadena: **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="79a17-201">Nombre corto de scripting: **apagado**</span><span class="sxs-lookup"><span data-stu-id="79a17-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="79a17-202">Necesario para apagar el sistema local.</span><span class="sxs-lookup"><span data-stu-id="79a17-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span><span class="sxs-lookup"><span data-stu-id="79a17-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="79a17-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-205">Constante de C++: **se ha \_ depurado \_ el nombre** cadena: **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="79a17-206">Nombre corto de scripting: **Debug**</span><span class="sxs-lookup"><span data-stu-id="79a17-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="79a17-207">Necesario para depurar y ajustar la memoria de un proceso que pertenece a otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="79a17-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span><span class="sxs-lookup"><span data-stu-id="79a17-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="79a17-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-210">Constante de C++: se trata de una cadena de **\_ \_ nombre de auditoría** : **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="79a17-211">Nombre corto de scripting: **Auditoría**</span><span class="sxs-lookup"><span data-stu-id="79a17-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="79a17-212">Necesario para generar entradas de auditoría en el registro de seguridad de NT.</span><span class="sxs-lookup"><span data-stu-id="79a17-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="79a17-213">Solo los servidores seguros deben tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="79a17-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="79a17-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="79a17-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-216">Constante de C++: **se trata \_ del \_ \_ nombre del entorno del sistema** de la cadena: **SeSystemEnvironmentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="79a17-217">Nombre corto de scripting: **SystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="79a17-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="79a17-218">Necesario para modificar la RAM no volátil de los sistemas que utilizan este tipo de memoria para almacenar los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="79a17-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="79a17-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="79a17-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-221">Constante de C++: **se ha \_ cambiado \_ \_ el nombre de notificación** cadena: **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="79a17-222">Nombre corto de scripting: **ChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="79a17-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="79a17-223">Requerido para recibir notificaciones de cambios en archivos o directorios y omitir las comprobaciones de acceso transversal.</span><span class="sxs-lookup"><span data-stu-id="79a17-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="79a17-224">Este privilegio está habilitado de forma predeterminada para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="79a17-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="79a17-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="79a17-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-227">Constante de C++: cadena de **\_ \_ \_ nombre de apagado remoto** : **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="79a17-228">Nombre corto de scripting: **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="79a17-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="79a17-229">Necesario para apagar un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="79a17-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span><span class="sxs-lookup"><span data-stu-id="79a17-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="79a17-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-232">Constante de C++: **se \_ desacopla \_ el nombre** de la cadena: **SeUndockPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="79a17-233">Nombre corto de scripting: **desacoplar**</span><span class="sxs-lookup"><span data-stu-id="79a17-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="79a17-234">Necesario para quitar un portátil de una estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="79a17-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span><span class="sxs-lookup"><span data-stu-id="79a17-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="79a17-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-237">Constante de C++: **se ha sincronizado la cadena de \_ \_ \_ nombre del agente** : **SeSyncAgentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="79a17-238">Nombre corto de scripting: **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="79a17-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="79a17-239">Necesario para sincronizar los datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="79a17-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="79a17-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="79a17-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-242">Constante de C++: se habilita la cadena de  **\_ \_ \_ nombre de delegación** : SeEnableDelegationPrivilege</span><span class="sxs-lookup"><span data-stu-id="79a17-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="79a17-243">Nombre corto de scripting: **EnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="79a17-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="79a17-244">Se requiere para habilitar la confianza en las cuentas de equipo y de usuario para la delegación.</span><span class="sxs-lookup"><span data-stu-id="79a17-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79a17-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span><span class="sxs-lookup"><span data-stu-id="79a17-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a17-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="79a17-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="79a17-247">Constante de C++ **: \_ se \_ administra \_ el nombre de volumen** cadena: **SeManageVolumePrivilege**</span><span class="sxs-lookup"><span data-stu-id="79a17-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="79a17-248">Nombre corto de scripting: **ManageVolume**</span><span class="sxs-lookup"><span data-stu-id="79a17-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="79a17-249">Necesario para realizar tareas de mantenimiento del volumen.</span><span class="sxs-lookup"><span data-stu-id="79a17-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79a17-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79a17-250">Requirements</span></span>



| <span data-ttu-id="79a17-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="79a17-251">Requirement</span></span> | <span data-ttu-id="79a17-252">Value</span><span class="sxs-lookup"><span data-stu-id="79a17-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79a17-253">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79a17-253">Minimum supported client</span></span><br/> | <span data-ttu-id="79a17-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79a17-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79a17-255">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79a17-255">Minimum supported server</span></span><br/> | <span data-ttu-id="79a17-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79a17-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79a17-257">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79a17-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="79a17-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79a17-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79a17-259">IDL</span><span class="sxs-lookup"><span data-stu-id="79a17-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79a17-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79a17-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79a17-261">Vea también</span><span class="sxs-lookup"><span data-stu-id="79a17-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a17-262">Scripting de constantes de API</span><span class="sxs-lookup"><span data-stu-id="79a17-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="79a17-263">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="79a17-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="79a17-264">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="79a17-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="79a17-265">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="79a17-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="79a17-266">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="79a17-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

