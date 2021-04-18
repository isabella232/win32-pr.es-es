---
title: Método StopService de la clase Win32_Service (Sdoias. h) (Terminal Services)
description: Coloca el servicio, representado por el \_ objeto TerminalService de Win32, en estado detenido.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- StopService (método) Servicios de Escritorio remoto
- Método StopService Servicios de Escritorio remoto, clase Win32_Service
- Clase Win32_Service Servicios de Escritorio remoto, método StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105681318"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="eaa63-106">Método StopService de la clase Win32_Service (Sdoias. h) para el servicio de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="eaa63-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="eaa63-107">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio, representado por el objeto [**\_ TerminalService de Win32**](win32-terminalservice.md) , en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="eaa63-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="eaa63-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="eaa63-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eaa63-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eaa63-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa63-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eaa63-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="eaa63-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eaa63-111">Parameters</span></span>

<span data-ttu-id="eaa63-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="eaa63-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eaa63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eaa63-113">Return value</span></span>

<span data-ttu-id="eaa63-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="eaa63-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="eaa63-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="eaa63-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="eaa63-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="eaa63-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="eaa63-117">**0**</span><span class="sxs-lookup"><span data-stu-id="eaa63-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaa63-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-119">**1**</span><span class="sxs-lookup"><span data-stu-id="eaa63-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaa63-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-121">**2**</span><span class="sxs-lookup"><span data-stu-id="eaa63-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="eaa63-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-123">**3**</span><span class="sxs-lookup"><span data-stu-id="eaa63-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="eaa63-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-125">**4**</span><span class="sxs-lookup"><span data-stu-id="eaa63-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-127">**5**</span><span class="sxs-lookup"><span data-stu-id="eaa63-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="eaa63-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-129">**6**</span><span class="sxs-lookup"><span data-stu-id="eaa63-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="eaa63-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-131">**7**</span><span class="sxs-lookup"><span data-stu-id="eaa63-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-133">**8**</span><span class="sxs-lookup"><span data-stu-id="eaa63-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-135">**9**</span><span class="sxs-lookup"><span data-stu-id="eaa63-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-136">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-137">**10**</span><span class="sxs-lookup"><span data-stu-id="eaa63-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="eaa63-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-139">**11**</span><span class="sxs-lookup"><span data-stu-id="eaa63-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="eaa63-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-141">**12**</span><span class="sxs-lookup"><span data-stu-id="eaa63-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-142">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-143">**13**</span><span class="sxs-lookup"><span data-stu-id="eaa63-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="eaa63-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-145">**14**</span><span class="sxs-lookup"><span data-stu-id="eaa63-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-147">**15**</span><span class="sxs-lookup"><span data-stu-id="eaa63-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-149">**16**</span><span class="sxs-lookup"><span data-stu-id="eaa63-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-151">**17**</span><span class="sxs-lookup"><span data-stu-id="eaa63-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eaa63-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-153">**18**</span><span class="sxs-lookup"><span data-stu-id="eaa63-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-154">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="eaa63-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-155">**19**</span><span class="sxs-lookup"><span data-stu-id="eaa63-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-156">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="eaa63-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-157">**20**</span><span class="sxs-lookup"><span data-stu-id="eaa63-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="eaa63-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-159">**21**</span><span class="sxs-lookup"><span data-stu-id="eaa63-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-161">**22**</span><span class="sxs-lookup"><span data-stu-id="eaa63-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-162">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-163">**23**</span><span class="sxs-lookup"><span data-stu-id="eaa63-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eaa63-165">**24**</span><span class="sxs-lookup"><span data-stu-id="eaa63-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="eaa63-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eaa63-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaa63-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaa63-167">Remarks</span></span>

<span data-ttu-id="eaa63-168">Después de determinar qué servicios se pueden detener o pausar, puede utilizar los métodos **StopService** y [**PauseService**](win32-terminalservice-pauseservice.md) para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="eaa63-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="eaa63-169">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="eaa63-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="eaa63-170">¿Se puede pausar el servicio?</span><span class="sxs-lookup"><span data-stu-id="eaa63-170">Is the service capable of being paused?</span></span> <span data-ttu-id="eaa63-171">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="eaa63-172">¿Necesita seguir controlando las solicitudes de cliente para los usuarios que ya están conectados al servicio?</span><span class="sxs-lookup"><span data-stu-id="eaa63-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="eaa63-173">Si es así, al pausar un servicio normalmente se le permite administrar los clientes existentes a la vez que deniega el acceso a los clientes nuevos.</span><span class="sxs-lookup"><span data-stu-id="eaa63-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="eaa63-174">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="eaa63-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="eaa63-175">¿Necesita volver a configurar un servicio y hacer que los cambios surtan efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="eaa63-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="eaa63-176">Aunque se pueden cambiar las propiedades del servicio mientras se pausa un servicio, la mayoría de ellos no surtirán efecto hasta que el servicio se detenga y se reinicie realmente.</span><span class="sxs-lookup"><span data-stu-id="eaa63-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="eaa63-177">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="eaa63-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="eaa63-178">Si intenta detener un servicio que tiene servicios dependientes en ejecución, se produce un error en el método **StopService** con un valor devuelto de 3.</span><span class="sxs-lookup"><span data-stu-id="eaa63-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="eaa63-179">Los servicios dependientes deben detenerse en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="eaa63-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="eaa63-180">Si detiene un servicio, compruebe inmediatamente el TerminalService de [**Win32 \_**](win32-terminalservice.md).**Propiedad State** , ya que el valor puede seguir mostrando el servicio como en ejecución.</span><span class="sxs-lookup"><span data-stu-id="eaa63-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="eaa63-181">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eaa63-181">Examples</span></span>

<span data-ttu-id="eaa63-182">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) El ejemplo de PowerShell establece el estado del servicio para los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="eaa63-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="eaa63-183">En el ejemplo de VBScript [detener un servicio y su dependientes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) se detiene un servicio y todos los servicios dependientes.</span><span class="sxs-lookup"><span data-stu-id="eaa63-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa63-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaa63-184">Requirements</span></span>



| <span data-ttu-id="eaa63-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaa63-185">Requirement</span></span> | <span data-ttu-id="eaa63-186">Value</span><span class="sxs-lookup"><span data-stu-id="eaa63-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa63-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaa63-187">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa63-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaa63-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eaa63-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaa63-189">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa63-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaa63-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaa63-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eaa63-191">Namespace</span></span><br/>                | <span data-ttu-id="eaa63-192">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="eaa63-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="eaa63-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eaa63-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa63-194"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa63-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="eaa63-195">MOF</span><span class="sxs-lookup"><span data-stu-id="eaa63-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaa63-196"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaa63-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaa63-197">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eaa63-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaa63-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaa63-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaa63-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="eaa63-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa63-200">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="eaa63-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="eaa63-201">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="eaa63-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="eaa63-202">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="eaa63-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="eaa63-203">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="eaa63-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="eaa63-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="eaa63-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

