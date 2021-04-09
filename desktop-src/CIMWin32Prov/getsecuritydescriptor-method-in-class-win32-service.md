---
description: Devuelve el descriptor de seguridad que controla el acceso al servicio.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)
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
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080159"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="27d9b-103">Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="27d9b-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="27d9b-104">El método **GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="27d9b-105">El descriptor se devuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="27d9b-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="27d9b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d9b-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="27d9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27d9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d9b-108">*Descriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="27d9b-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-109">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d9b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27d9b-110">Return value</span></span>

<span data-ttu-id="27d9b-111">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="27d9b-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="27d9b-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="27d9b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="27d9b-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="27d9b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="27d9b-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="27d9b-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-115">0</span><span class="sxs-lookup"><span data-stu-id="27d9b-115">0</span></span>

<span data-ttu-id="27d9b-116">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27d9b-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-117">1</span><span class="sxs-lookup"><span data-stu-id="27d9b-117">1</span></span>

<span data-ttu-id="27d9b-118">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27d9b-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="27d9b-119">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="27d9b-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-120">2</span><span class="sxs-lookup"><span data-stu-id="27d9b-120">2</span></span>

<span data-ttu-id="27d9b-121">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="27d9b-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-122">3</span><span class="sxs-lookup"><span data-stu-id="27d9b-122">3</span></span>

<span data-ttu-id="27d9b-123">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="27d9b-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-124">4</span><span class="sxs-lookup"><span data-stu-id="27d9b-124">4</span></span>

<span data-ttu-id="27d9b-125">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-126">5</span><span class="sxs-lookup"><span data-stu-id="27d9b-126">5</span></span>

<span data-ttu-id="27d9b-127">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="27d9b-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-128">6</span><span class="sxs-lookup"><span data-stu-id="27d9b-128">6</span></span>

<span data-ttu-id="27d9b-129">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="27d9b-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-130">7</span><span class="sxs-lookup"><span data-stu-id="27d9b-130">7</span></span>

<span data-ttu-id="27d9b-131">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="27d9b-132">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="27d9b-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-133">8</span><span class="sxs-lookup"><span data-stu-id="27d9b-133">8</span></span>

<span data-ttu-id="27d9b-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="27d9b-135">**Falta el privilegio**</span><span class="sxs-lookup"><span data-stu-id="27d9b-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-136">9</span><span class="sxs-lookup"><span data-stu-id="27d9b-136">9</span></span>

<span data-ttu-id="27d9b-137">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-138">10</span><span class="sxs-lookup"><span data-stu-id="27d9b-138">10</span></span>

<span data-ttu-id="27d9b-139">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="27d9b-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-140">11</span><span class="sxs-lookup"><span data-stu-id="27d9b-140">11</span></span>

<span data-ttu-id="27d9b-141">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="27d9b-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-142">12</span><span class="sxs-lookup"><span data-stu-id="27d9b-142">12</span></span>

<span data-ttu-id="27d9b-143">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-144">13</span><span class="sxs-lookup"><span data-stu-id="27d9b-144">13</span></span>

<span data-ttu-id="27d9b-145">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="27d9b-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-146">14</span><span class="sxs-lookup"><span data-stu-id="27d9b-146">14</span></span>

<span data-ttu-id="27d9b-147">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-148">15</span><span class="sxs-lookup"><span data-stu-id="27d9b-148">15</span></span>

<span data-ttu-id="27d9b-149">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-150">16</span><span class="sxs-lookup"><span data-stu-id="27d9b-150">16</span></span>

<span data-ttu-id="27d9b-151">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-152">17</span><span class="sxs-lookup"><span data-stu-id="27d9b-152">17</span></span>

<span data-ttu-id="27d9b-153">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="27d9b-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-154">18</span><span class="sxs-lookup"><span data-stu-id="27d9b-154">18</span></span>

<span data-ttu-id="27d9b-155">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="27d9b-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-156">19</span><span class="sxs-lookup"><span data-stu-id="27d9b-156">19</span></span>

<span data-ttu-id="27d9b-157">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="27d9b-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-158">20</span><span class="sxs-lookup"><span data-stu-id="27d9b-158">20</span></span>

<span data-ttu-id="27d9b-159">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="27d9b-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="27d9b-160">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="27d9b-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-161">21</span><span class="sxs-lookup"><span data-stu-id="27d9b-161">21</span></span>

<span data-ttu-id="27d9b-162">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-163">22</span><span class="sxs-lookup"><span data-stu-id="27d9b-163">22</span></span>

<span data-ttu-id="27d9b-164">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="27d9b-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-165">23</span><span class="sxs-lookup"><span data-stu-id="27d9b-165">23</span></span>

<span data-ttu-id="27d9b-166">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="27d9b-167">24</span><span class="sxs-lookup"><span data-stu-id="27d9b-167">24</span></span>

<span data-ttu-id="27d9b-168">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="27d9b-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="27d9b-169">**Otros**</span><span class="sxs-lookup"><span data-stu-id="27d9b-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="27d9b-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="27d9b-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27d9b-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27d9b-171">Remarks</span></span>

<span data-ttu-id="27d9b-172">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="27d9b-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="27d9b-173">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="27d9b-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="27d9b-174">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="27d9b-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="27d9b-175">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="27d9b-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="27d9b-176">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="27d9b-176">Examples</span></span>

<span data-ttu-id="27d9b-177">Al recuperar un descriptor de seguridad en VBScript, asegúrese de "seguridad" y ejecute como administrador, tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="27d9b-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="27d9b-178">De lo contrario, el código puede producir un error de permisos.</span><span class="sxs-lookup"><span data-stu-id="27d9b-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="27d9b-179">Del mismo modo, en VB.NET, asegúrese de establecer "EnablePrivileges = true" y ejecutar la aplicación como administrador.</span><span class="sxs-lookup"><span data-stu-id="27d9b-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="27d9b-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d9b-180">Requirements</span></span>



| <span data-ttu-id="27d9b-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d9b-181">Requirement</span></span> | <span data-ttu-id="27d9b-182">Value</span><span class="sxs-lookup"><span data-stu-id="27d9b-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27d9b-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d9b-183">Minimum supported client</span></span><br/> | <span data-ttu-id="27d9b-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27d9b-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27d9b-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d9b-185">Minimum supported server</span></span><br/> | <span data-ttu-id="27d9b-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27d9b-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27d9b-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27d9b-187">Namespace</span></span><br/>                | <span data-ttu-id="27d9b-188">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="27d9b-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27d9b-189">MOF</span><span class="sxs-lookup"><span data-stu-id="27d9b-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27d9b-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27d9b-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27d9b-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27d9b-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d9b-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27d9b-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d9b-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="27d9b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d9b-194">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="27d9b-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="27d9b-195">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="27d9b-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="27d9b-196">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="27d9b-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="27d9b-197">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="27d9b-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="27d9b-198">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="27d9b-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

