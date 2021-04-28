---
title: Método GetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método GetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto): devuelve el descriptor de seguridad que controla el acceso al servicio.'
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- scripting Instrumental de administración de Windows , seguridad
- security Instrumental de administración de Windows , scripting
- Método GetSecurityDescriptor Servicios de Escritorio remoto
- Método GetSecurityDescriptor Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto , método GetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090653"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="0cd1e-108">Método GetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="0cd1e-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="0cd1e-109">El **método GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="0cd1e-110">El descriptor se devuelve como una instancia de [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)</span><span class="sxs-lookup"><span data-stu-id="0cd1e-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd1e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cd1e-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="0cd1e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cd1e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd1e-113">*Descriptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cd1e-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-114">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd1e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cd1e-115">Return value</span></span>

<span data-ttu-id="0cd1e-116">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="0cd1e-117">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0cd1e-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0cd1e-118">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0cd1e-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0cd1e-119">**0**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-120">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-121">**1**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-122">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-123">**2**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-124">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-125">**3**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-126">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-127">**4**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-128">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-129">**5**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-130">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-131">**6**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-132">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-133">**7**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-134">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-135">**8**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-136">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-137">**9**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-138">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-139">**10**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-140">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-141">**11**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-142">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-143">**12**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-144">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-145">**13**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-146">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-147">**14**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-148">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-149">**15**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-150">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-151">**16**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-152">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-153">**17**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-154">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-155">**18**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-156">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-157">**19**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-158">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-159">**20**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-160">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-161">**21**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-162">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-163">**22**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-164">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-165">**23**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-166">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1e-167">**24**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0cd1e-168">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cd1e-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cd1e-169">Remarks</span></span>

<span data-ttu-id="0cd1e-170">La [**instancia de \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos SECURITY DESCRIPTOR [**\_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="0cd1e-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="0cd1e-171">Para obtener más información, [vea Access Control lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="0cd1e-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="0cd1e-172">Si **se concede o se habilita SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="0cd1e-173">Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [Ejecución de operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="0cd1e-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="0cd1e-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0cd1e-174">Examples</span></span>

<span data-ttu-id="0cd1e-175">Al recuperar un descriptor de seguridad en VBScript, asegúrese de "Seguridad" y ejecute como administrador, como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="0cd1e-176">De lo contrario, el código puede producir un error de permisos.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="0cd1e-177">Del mismo modo, en VB.NET, asegúrese de establecer "EnablePrivileges = True" y ejecute la aplicación como administrador.</span><span class="sxs-lookup"><span data-stu-id="0cd1e-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="0cd1e-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd1e-178">Requirements</span></span>



| <span data-ttu-id="0cd1e-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd1e-179">Requirement</span></span> | <span data-ttu-id="0cd1e-180">Valor</span><span class="sxs-lookup"><span data-stu-id="0cd1e-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd1e-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd1e-181">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd1e-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cd1e-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cd1e-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd1e-183">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd1e-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cd1e-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cd1e-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0cd1e-185">Namespace</span></span><br/>                | <span data-ttu-id="0cd1e-186">\\TerminalServices de CIMv2 \\ raíz</span><span class="sxs-lookup"><span data-stu-id="0cd1e-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0cd1e-187">MOF</span><span class="sxs-lookup"><span data-stu-id="0cd1e-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cd1e-188"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cd1e-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cd1e-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0cd1e-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cd1e-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cd1e-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cd1e-191">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0cd1e-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd1e-192">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="0cd1e-193">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0cd1e-194">**Constantes de privilegios**</span><span class="sxs-lookup"><span data-stu-id="0cd1e-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="0cd1e-195">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="0cd1e-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="0cd1e-196">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="0cd1e-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="0cd1e-197">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="0cd1e-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

