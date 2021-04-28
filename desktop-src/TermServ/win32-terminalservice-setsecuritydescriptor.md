---
title: Método SetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método SetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto): escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.'
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- scripting Instrumental de administración de Windows , security
- security Instrumental de administración de Windows , scripting
- Método SetSecurityDescriptor Servicios de Escritorio remoto
- Método SetSecurityDescriptor Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto , método SetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2dd7e43041c05b1c294181f8bd01548ed76d87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114502"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="f3363-108">Método SetSecurityDescriptor de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="f3363-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="f3363-109">El **método SetSecurityDescriptor** escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3363-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3363-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="f3363-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3363-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3363-112">*Descriptor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f3363-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3363-113">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3363-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3363-114">Return value</span></span>

<span data-ttu-id="f3363-115">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f3363-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="f3363-116">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f3363-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f3363-117">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f3363-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f3363-118">**0**</span><span class="sxs-lookup"><span data-stu-id="f3363-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-119">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3363-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-120">**1**</span><span class="sxs-lookup"><span data-stu-id="f3363-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-121">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3363-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-122">**2**</span><span class="sxs-lookup"><span data-stu-id="f3363-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-123">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="f3363-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-124">**3**</span><span class="sxs-lookup"><span data-stu-id="f3363-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-125">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="f3363-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-126">**4**</span><span class="sxs-lookup"><span data-stu-id="f3363-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-127">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-128">**5**</span><span class="sxs-lookup"><span data-stu-id="f3363-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-129">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="f3363-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-130">**6**</span><span class="sxs-lookup"><span data-stu-id="f3363-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-131">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="f3363-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-132">**7**</span><span class="sxs-lookup"><span data-stu-id="f3363-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-133">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-134">**8**</span><span class="sxs-lookup"><span data-stu-id="f3363-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-135">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-136">**9**</span><span class="sxs-lookup"><span data-stu-id="f3363-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-137">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-138">**10**</span><span class="sxs-lookup"><span data-stu-id="f3363-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-139">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f3363-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-140">**11**</span><span class="sxs-lookup"><span data-stu-id="f3363-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-141">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f3363-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-142">**12**</span><span class="sxs-lookup"><span data-stu-id="f3363-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-143">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-144">**13**</span><span class="sxs-lookup"><span data-stu-id="f3363-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-145">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="f3363-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-146">**14**</span><span class="sxs-lookup"><span data-stu-id="f3363-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-147">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="f3363-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-148">**15**</span><span class="sxs-lookup"><span data-stu-id="f3363-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-149">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f3363-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-150">**16**</span><span class="sxs-lookup"><span data-stu-id="f3363-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-151">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="f3363-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-152">**17**</span><span class="sxs-lookup"><span data-stu-id="f3363-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-153">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f3363-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-154">**18**</span><span class="sxs-lookup"><span data-stu-id="f3363-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-155">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="f3363-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-156">**19**</span><span class="sxs-lookup"><span data-stu-id="f3363-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-157">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="f3363-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-158">**20**</span><span class="sxs-lookup"><span data-stu-id="f3363-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-159">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="f3363-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-160">**21**</span><span class="sxs-lookup"><span data-stu-id="f3363-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-161">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-162">**22**</span><span class="sxs-lookup"><span data-stu-id="f3363-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-163">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f3363-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-164">**23**</span><span class="sxs-lookup"><span data-stu-id="f3363-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-165">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="f3363-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f3363-166">**24**</span><span class="sxs-lookup"><span data-stu-id="f3363-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f3363-167">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f3363-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3363-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3363-168">Remarks</span></span>

<span data-ttu-id="f3363-169">La [**instancia \_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos [**SECURITY DESCRIPTOR \_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="f3363-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="f3363-170">Para obtener más información, [vea Access Control enumeraciones](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="f3363-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="f3363-171">Si no se concede o se habilita **SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="f3363-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="f3363-172">Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [Ejecución de operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="f3363-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="f3363-173">Puede actualizar la DACL y la SACL en la instancia [**\_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o solo la SACL.</span><span class="sxs-lookup"><span data-stu-id="f3363-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="f3363-174">Los valores siguientes de [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan dacl, sacl o ambos.</span><span class="sxs-lookup"><span data-stu-id="f3363-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="f3363-175">**SE \_ DACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="f3363-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="f3363-176">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="f3363-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="f3363-177">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="f3363-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="f3363-178">**SE \_ SACL \_ PRESENT**</span><span class="sxs-lookup"><span data-stu-id="f3363-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="f3363-179">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="f3363-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="f3363-180">Si no se establece, WMI conserva el valor original de sacl.</span><span class="sxs-lookup"><span data-stu-id="f3363-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="f3363-181">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege.**</span><span class="sxs-lookup"><span data-stu-id="f3363-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="f3363-182">Para el scripting, el nombre de privilegio **es SeSecurityPrivilege.**</span><span class="sxs-lookup"><span data-stu-id="f3363-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="f3363-183">Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="f3363-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="f3363-184">Si las propiedades Administrador de grupo y Administrador de propietarios no son **NULL,** se actualizan.</span><span class="sxs-lookup"><span data-stu-id="f3363-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="f3363-185">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="f3363-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="f3363-186">Para obtener más información, vea [Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="f3363-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="f3363-187">Cuando una sacl nueva es **NULL en** una llamada a este método, el descriptor de seguridad SACL del objeto protegible de destino se deja sin modificar.</span><span class="sxs-lookup"><span data-stu-id="f3363-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3363-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3363-188">Requirements</span></span>



| <span data-ttu-id="f3363-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3363-189">Requirement</span></span> | <span data-ttu-id="f3363-190">Valor</span><span class="sxs-lookup"><span data-stu-id="f3363-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3363-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3363-191">Minimum supported client</span></span><br/> | <span data-ttu-id="f3363-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3363-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3363-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3363-193">Minimum supported server</span></span><br/> | <span data-ttu-id="f3363-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3363-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3363-195">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3363-195">Namespace</span></span><br/>                | <span data-ttu-id="f3363-196">\\TerminalServices de CIMv2 \\ raíz</span><span class="sxs-lookup"><span data-stu-id="f3363-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f3363-197">MOF</span><span class="sxs-lookup"><span data-stu-id="f3363-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3363-198"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3363-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3363-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3363-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3363-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3363-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3363-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f3363-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3363-202">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="f3363-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="f3363-203">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f3363-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f3363-204">**Constantes de privilegios**</span><span class="sxs-lookup"><span data-stu-id="f3363-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="f3363-205">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="f3363-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="f3363-206">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="f3363-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="f3363-207">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="f3363-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

