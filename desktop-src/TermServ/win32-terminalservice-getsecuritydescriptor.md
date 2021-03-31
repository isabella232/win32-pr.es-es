---
title: Método GetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)
description: Devuelve el descriptor de seguridad que controla el acceso al servicio.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- scripting Instrumental de administración de Windows, seguridad
- Instrumental de administración de Windows de seguridad, scripting
- Método GetSecurityDescriptor Servicios de Escritorio remoto
- Método GetSecurityDescriptor Servicios de Escritorio remoto, clase Win32_Service
- Win32_Service de clase Servicios de Escritorio remoto, método GetSecurityDescriptor
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
ms.openlocfilehash: cf8dc271d5498163352af10bcb0b9c55e2e81fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996250"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="6e964-108">Método GetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="6e964-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="6e964-109">El método **GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="6e964-110">El descriptor se devuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6e964-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e964-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e964-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="6e964-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e964-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e964-113">*Descriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e964-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e964-114">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e964-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e964-115">Return value</span></span>

<span data-ttu-id="6e964-116">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="6e964-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="6e964-117">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6e964-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6e964-118">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6e964-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6e964-119">**0**</span><span class="sxs-lookup"><span data-stu-id="6e964-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-120">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e964-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-121">**1**</span><span class="sxs-lookup"><span data-stu-id="6e964-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-122">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e964-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-123">**2**</span><span class="sxs-lookup"><span data-stu-id="6e964-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-124">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="6e964-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-125">**3**</span><span class="sxs-lookup"><span data-stu-id="6e964-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-126">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="6e964-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-127">**4**</span><span class="sxs-lookup"><span data-stu-id="6e964-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-128">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-129">**5**</span><span class="sxs-lookup"><span data-stu-id="6e964-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-130">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="6e964-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-131">**6**</span><span class="sxs-lookup"><span data-stu-id="6e964-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-132">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="6e964-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-133">**7**</span><span class="sxs-lookup"><span data-stu-id="6e964-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-134">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-135">**8**</span><span class="sxs-lookup"><span data-stu-id="6e964-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-136">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-137">**9**</span><span class="sxs-lookup"><span data-stu-id="6e964-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-138">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-139">**10**</span><span class="sxs-lookup"><span data-stu-id="6e964-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-140">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6e964-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-141">**11**</span><span class="sxs-lookup"><span data-stu-id="6e964-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-142">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e964-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-143">**12**</span><span class="sxs-lookup"><span data-stu-id="6e964-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-144">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-145">**13**</span><span class="sxs-lookup"><span data-stu-id="6e964-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-146">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="6e964-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-147">**14**</span><span class="sxs-lookup"><span data-stu-id="6e964-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-148">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-149">**15**</span><span class="sxs-lookup"><span data-stu-id="6e964-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-150">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-151">**16**</span><span class="sxs-lookup"><span data-stu-id="6e964-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-152">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-153">**17**</span><span class="sxs-lookup"><span data-stu-id="6e964-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-154">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6e964-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-155">**18**</span><span class="sxs-lookup"><span data-stu-id="6e964-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-156">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="6e964-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-157">**19**</span><span class="sxs-lookup"><span data-stu-id="6e964-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-158">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="6e964-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-159">**20**</span><span class="sxs-lookup"><span data-stu-id="6e964-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-160">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="6e964-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-161">**21**</span><span class="sxs-lookup"><span data-stu-id="6e964-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-162">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-163">**22**</span><span class="sxs-lookup"><span data-stu-id="6e964-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-164">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e964-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-165">**23**</span><span class="sxs-lookup"><span data-stu-id="6e964-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-166">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e964-167">**24**</span><span class="sxs-lookup"><span data-stu-id="6e964-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="6e964-168">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6e964-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e964-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e964-169">Remarks</span></span>

<span data-ttu-id="6e964-170">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="6e964-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="6e964-171">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="6e964-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="6e964-172">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="6e964-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="6e964-173">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="6e964-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="6e964-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6e964-174">Examples</span></span>

<span data-ttu-id="6e964-175">Al recuperar un descriptor de seguridad en VBScript, asegúrese de "seguridad" y ejecute como administrador, tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="6e964-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="6e964-176">De lo contrario, el código puede producir un error de permisos.</span><span class="sxs-lookup"><span data-stu-id="6e964-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="6e964-177">Del mismo modo, en VB.NET, asegúrese de establecer "EnablePrivileges = true" y ejecutar la aplicación como administrador.</span><span class="sxs-lookup"><span data-stu-id="6e964-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="6e964-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e964-178">Requirements</span></span>



| <span data-ttu-id="6e964-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e964-179">Requirement</span></span> | <span data-ttu-id="6e964-180">Value</span><span class="sxs-lookup"><span data-stu-id="6e964-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e964-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e964-181">Minimum supported client</span></span><br/> | <span data-ttu-id="6e964-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e964-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e964-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e964-183">Minimum supported server</span></span><br/> | <span data-ttu-id="6e964-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e964-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e964-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e964-185">Namespace</span></span><br/>                | <span data-ttu-id="6e964-186">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6e964-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6e964-187">MOF</span><span class="sxs-lookup"><span data-stu-id="6e964-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e964-188"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e964-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e964-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e964-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e964-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e964-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e964-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e964-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e964-192">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="6e964-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="6e964-193">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="6e964-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="6e964-194">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="6e964-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="6e964-195">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="6e964-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="6e964-196">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="6e964-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="6e964-197">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="6e964-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

