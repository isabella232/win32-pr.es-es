---
description: 'Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32): devuelve el descriptor de seguridad que controla el acceso al servicio.'
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096993"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="9cbe5-103">Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9cbe5-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9cbe5-104">El **método GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="9cbe5-105">El descriptor se devuelve como una instancia de [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)</span><span class="sxs-lookup"><span data-stu-id="9cbe5-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cbe5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cbe5-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="9cbe5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cbe5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbe5-108">*Descriptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9cbe5-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-109">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cbe5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cbe5-110">Return value</span></span>

<span data-ttu-id="9cbe5-111">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="9cbe5-112">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9cbe5-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9cbe5-113">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9cbe5-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9cbe5-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-115">0</span><span class="sxs-lookup"><span data-stu-id="9cbe5-115">0</span></span>

<span data-ttu-id="9cbe5-116">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-117">1</span><span class="sxs-lookup"><span data-stu-id="9cbe5-117">1</span></span>

<span data-ttu-id="9cbe5-118">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9cbe5-119">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-120">2</span><span class="sxs-lookup"><span data-stu-id="9cbe5-120">2</span></span>

<span data-ttu-id="9cbe5-121">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-122">3</span><span class="sxs-lookup"><span data-stu-id="9cbe5-122">3</span></span>

<span data-ttu-id="9cbe5-123">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-124">4</span><span class="sxs-lookup"><span data-stu-id="9cbe5-124">4</span></span>

<span data-ttu-id="9cbe5-125">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-126">5</span><span class="sxs-lookup"><span data-stu-id="9cbe5-126">5</span></span>

<span data-ttu-id="9cbe5-127">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**Propiedad** State) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-128">6</span><span class="sxs-lookup"><span data-stu-id="9cbe5-128">6</span></span>

<span data-ttu-id="9cbe5-129">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-130">7</span><span class="sxs-lookup"><span data-stu-id="9cbe5-130">7</span></span>

<span data-ttu-id="9cbe5-131">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9cbe5-132">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-133">8</span><span class="sxs-lookup"><span data-stu-id="9cbe5-133">8</span></span>

<span data-ttu-id="9cbe5-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9cbe5-135">**Falta el privilegio**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-136">9</span><span class="sxs-lookup"><span data-stu-id="9cbe5-136">9</span></span>

<span data-ttu-id="9cbe5-137">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-138">10</span><span class="sxs-lookup"><span data-stu-id="9cbe5-138">10</span></span>

<span data-ttu-id="9cbe5-139">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-140">11</span><span class="sxs-lookup"><span data-stu-id="9cbe5-140">11</span></span>

<span data-ttu-id="9cbe5-141">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-142">12</span><span class="sxs-lookup"><span data-stu-id="9cbe5-142">12</span></span>

<span data-ttu-id="9cbe5-143">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-144">13</span><span class="sxs-lookup"><span data-stu-id="9cbe5-144">13</span></span>

<span data-ttu-id="9cbe5-145">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-146">14</span><span class="sxs-lookup"><span data-stu-id="9cbe5-146">14</span></span>

<span data-ttu-id="9cbe5-147">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-148">15</span><span class="sxs-lookup"><span data-stu-id="9cbe5-148">15</span></span>

<span data-ttu-id="9cbe5-149">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-150">16</span><span class="sxs-lookup"><span data-stu-id="9cbe5-150">16</span></span>

<span data-ttu-id="9cbe5-151">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-152">17</span><span class="sxs-lookup"><span data-stu-id="9cbe5-152">17</span></span>

<span data-ttu-id="9cbe5-153">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-154">18</span><span class="sxs-lookup"><span data-stu-id="9cbe5-154">18</span></span>

<span data-ttu-id="9cbe5-155">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-156">19</span><span class="sxs-lookup"><span data-stu-id="9cbe5-156">19</span></span>

<span data-ttu-id="9cbe5-157">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-158">20</span><span class="sxs-lookup"><span data-stu-id="9cbe5-158">20</span></span>

<span data-ttu-id="9cbe5-159">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="9cbe5-160">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-161">21</span><span class="sxs-lookup"><span data-stu-id="9cbe5-161">21</span></span>

<span data-ttu-id="9cbe5-162">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-163">22</span><span class="sxs-lookup"><span data-stu-id="9cbe5-163">22</span></span>

<span data-ttu-id="9cbe5-164">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-165">23</span><span class="sxs-lookup"><span data-stu-id="9cbe5-165">23</span></span>

<span data-ttu-id="9cbe5-166">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9cbe5-167">24</span><span class="sxs-lookup"><span data-stu-id="9cbe5-167">24</span></span>

<span data-ttu-id="9cbe5-168">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="9cbe5-169">**Otros**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9cbe5-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="9cbe5-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cbe5-171">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cbe5-171">Remarks</span></span>

<span data-ttu-id="9cbe5-172">La [**instancia \_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos [**SECURITY DESCRIPTOR \_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="9cbe5-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="9cbe5-173">Para obtener más información, [vea Access Control enumeraciones](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="9cbe5-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="9cbe5-174">Si no se concede o se habilita **SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="9cbe5-175">Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [Ejecución de operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)</span><span class="sxs-lookup"><span data-stu-id="9cbe5-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="9cbe5-176">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9cbe5-176">Examples</span></span>

<span data-ttu-id="9cbe5-177">Al recuperar un descriptor de seguridad en VBScript, asegúrese de "Seguridad" y ejecute como Administrador, como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="9cbe5-178">De lo contrario, el código puede producir un error de permisos.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="9cbe5-179">Del mismo modo, en VB.NET, asegúrese de establecer "EnablePrivileges = True" y ejecutar la aplicación como administrador.</span><span class="sxs-lookup"><span data-stu-id="9cbe5-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="9cbe5-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbe5-180">Requirements</span></span>



| <span data-ttu-id="9cbe5-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbe5-181">Requirement</span></span> | <span data-ttu-id="9cbe5-182">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbe5-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbe5-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cbe5-183">Minimum supported client</span></span><br/> | <span data-ttu-id="9cbe5-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cbe5-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cbe5-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cbe5-185">Minimum supported server</span></span><br/> | <span data-ttu-id="9cbe5-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cbe5-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cbe5-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9cbe5-187">Namespace</span></span><br/>                | <span data-ttu-id="9cbe5-188">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="9cbe5-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cbe5-189">MOF</span><span class="sxs-lookup"><span data-stu-id="9cbe5-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cbe5-190"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cbe5-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cbe5-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cbe5-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cbe5-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cbe5-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbe5-193">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9cbe5-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbe5-194">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="9cbe5-195">**Constantes de privilegios**</span><span class="sxs-lookup"><span data-stu-id="9cbe5-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="9cbe5-196">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="9cbe5-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="9cbe5-197">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="9cbe5-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="9cbe5-198">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="9cbe5-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

