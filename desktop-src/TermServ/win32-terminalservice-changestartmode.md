---
title: Método ChangeStartMode de la clase Win32_Service (Servicios de Escritorio remoto)
description: Modifica el modo de inicio de un TerminalService de Win32 \_ .
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- Método ChangeStartMode Servicios de Escritorio remoto
- Método ChangeStartMode Servicios de Escritorio remoto, clase Win32_Service
- Win32_Service de clase Servicios de Escritorio remoto, método ChangeStartMode
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685964"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="da278-106">Método ChangeStartMode de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="da278-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="da278-107">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de [**un \_ TerminalService de Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="da278-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="da278-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="da278-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da278-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da278-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da278-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da278-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="da278-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da278-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da278-112">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da278-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da278-113">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="da278-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="da278-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**</span><span class="sxs-lookup"><span data-stu-id="da278-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="da278-115">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="da278-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="da278-116">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="da278-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="da278-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Integrado**</span><span class="sxs-lookup"><span data-stu-id="da278-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="da278-118">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="da278-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="da278-119">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="da278-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="da278-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="da278-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="da278-121">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="da278-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="da278-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="da278-123">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="da278-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="da278-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**</span><span class="sxs-lookup"><span data-stu-id="da278-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="da278-125">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="da278-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da278-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da278-126">Return value</span></span>

<span data-ttu-id="da278-127">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="da278-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="da278-128">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="da278-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="da278-129">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da278-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da278-130">**0**</span><span class="sxs-lookup"><span data-stu-id="da278-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="da278-131">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da278-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="da278-132">**1**</span><span class="sxs-lookup"><span data-stu-id="da278-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="da278-133">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da278-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="da278-134">**2**</span><span class="sxs-lookup"><span data-stu-id="da278-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="da278-135">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="da278-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="da278-136">**3**</span><span class="sxs-lookup"><span data-stu-id="da278-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="da278-137">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="da278-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="da278-138">**4**</span><span class="sxs-lookup"><span data-stu-id="da278-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="da278-139">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="da278-140">**5**</span><span class="sxs-lookup"><span data-stu-id="da278-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="da278-141">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="da278-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="da278-142">**6**</span><span class="sxs-lookup"><span data-stu-id="da278-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="da278-143">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="da278-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="da278-144">**7**</span><span class="sxs-lookup"><span data-stu-id="da278-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="da278-145">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="da278-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="da278-146">**8**</span><span class="sxs-lookup"><span data-stu-id="da278-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="da278-147">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="da278-148">**9**</span><span class="sxs-lookup"><span data-stu-id="da278-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="da278-149">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="da278-150">**10**</span><span class="sxs-lookup"><span data-stu-id="da278-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="da278-151">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="da278-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="da278-152">**11**</span><span class="sxs-lookup"><span data-stu-id="da278-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="da278-153">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="da278-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="da278-154">**12**</span><span class="sxs-lookup"><span data-stu-id="da278-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="da278-155">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="da278-156">**13**</span><span class="sxs-lookup"><span data-stu-id="da278-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="da278-157">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="da278-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="da278-158">**14**</span><span class="sxs-lookup"><span data-stu-id="da278-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="da278-159">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="da278-160">**15**</span><span class="sxs-lookup"><span data-stu-id="da278-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="da278-161">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="da278-162">**16**</span><span class="sxs-lookup"><span data-stu-id="da278-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="da278-163">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="da278-164">**17**</span><span class="sxs-lookup"><span data-stu-id="da278-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="da278-165">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="da278-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="da278-166">**18**</span><span class="sxs-lookup"><span data-stu-id="da278-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="da278-167">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="da278-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="da278-168">**19**</span><span class="sxs-lookup"><span data-stu-id="da278-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="da278-169">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="da278-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="da278-170">**20**</span><span class="sxs-lookup"><span data-stu-id="da278-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="da278-171">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="da278-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="da278-172">**21**</span><span class="sxs-lookup"><span data-stu-id="da278-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="da278-173">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="da278-174">**22**</span><span class="sxs-lookup"><span data-stu-id="da278-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="da278-175">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="da278-176">**23**</span><span class="sxs-lookup"><span data-stu-id="da278-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="da278-177">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="da278-178">**24**</span><span class="sxs-lookup"><span data-stu-id="da278-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="da278-179">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="da278-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="da278-180">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="da278-180">Examples</span></span>

<span data-ttu-id="da278-181">El siguiente [cambio de StartMode de un](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) ejemplo de PowerShell de servicio, extraído de la galería de TechNet, cambia el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="da278-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="da278-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da278-182">Requirements</span></span>



| <span data-ttu-id="da278-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="da278-183">Requirement</span></span> | <span data-ttu-id="da278-184">Value</span><span class="sxs-lookup"><span data-stu-id="da278-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da278-185">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da278-185">Minimum supported client</span></span><br/> | <span data-ttu-id="da278-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da278-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da278-187">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da278-187">Minimum supported server</span></span><br/> | <span data-ttu-id="da278-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da278-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da278-189">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da278-189">Namespace</span></span><br/>                | <span data-ttu-id="da278-190">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="da278-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da278-191">MOF</span><span class="sxs-lookup"><span data-stu-id="da278-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da278-192"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da278-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da278-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da278-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da278-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da278-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da278-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="da278-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da278-196">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="da278-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="da278-197">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="da278-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="da278-198">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="da278-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="da278-199">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="da278-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

