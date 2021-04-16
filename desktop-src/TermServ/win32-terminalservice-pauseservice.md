---
title: Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)
description: Intenta poner el servicio en estado de pausa.
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Método PauseService Servicios de Escritorio remoto
- Método PauseService Servicios de Escritorio remoto, clase Win32_Service
- Win32_Service de clase Servicios de Escritorio remoto, método PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69951a77530b3aff89148b08e19f3a7c4da8f5b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676661"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="c4d2c-106">Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="c4d2c-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="c4d2c-107">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta poner el servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="c4d2c-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c4d2c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c4d2c-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c4d2c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d2c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4d2c-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="c4d2c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4d2c-111">Parameters</span></span>

<span data-ttu-id="c4d2c-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4d2c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4d2c-113">Return value</span></span>

<span data-ttu-id="c4d2c-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c4d2c-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c4d2c-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c4d2c-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c4d2c-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c4d2c-117">**0**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-119">**1**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-121">**2**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-123">**3**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-125">**4**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-127">**5**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-129">**6**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-131">**7**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-133">**8**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-135">**9**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-136">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-137">**10**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-139">**11**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-141">**12**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-142">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-143">**13**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-145">**14**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-147">**15**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-149">**16**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-151">**17**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-153">**18**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-154">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-155">**19**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-156">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-157">**20**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-159">**21**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-161">**22**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-162">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-163">**23**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c4d2c-165">**24**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c4d2c-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4d2c-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4d2c-167">Remarks</span></span>

<span data-ttu-id="c4d2c-168">Después de determinar qué servicios se pueden detener o pausar, puede utilizar los métodos [**StopService**](win32-terminalservice-stopservice.md) y **PauseService** para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="c4d2c-169">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4d2c-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="c4d2c-170">¿Se puede pausar el servicio?</span><span class="sxs-lookup"><span data-stu-id="c4d2c-170">Is the service capable of being paused?</span></span> <span data-ttu-id="c4d2c-171">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="c4d2c-172">¿Necesita seguir controlando las solicitudes de cliente para los usuarios que ya están conectados al servicio?</span><span class="sxs-lookup"><span data-stu-id="c4d2c-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="c4d2c-173">Si es así, al pausar un servicio normalmente se le permite administrar los clientes existentes a la vez que deniega el acceso a los clientes nuevos.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="c4d2c-174">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="c4d2c-175">¿Necesita volver a configurar un servicio y hacer que los cambios surtan efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="c4d2c-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="c4d2c-176">Aunque se pueden cambiar las propiedades del servicio mientras se pausa un servicio, la mayoría de ellos no surtirán efecto hasta que el servicio se detenga y se reinicie realmente.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="c4d2c-177">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4d2c-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="c4d2c-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c4d2c-178">Examples</span></span>

<span data-ttu-id="c4d2c-179">En el ejemplo de [aplicación pausar los servicios que se ejecutan con una cuenta específica](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) de VBScript se detienen todos los servicios que se ejecutan en la misma cuenta de servicio</span><span class="sxs-lookup"><span data-stu-id="c4d2c-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d2c-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4d2c-180">Requirements</span></span>



| <span data-ttu-id="c4d2c-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d2c-181">Requirement</span></span> | <span data-ttu-id="c4d2c-182">Value</span><span class="sxs-lookup"><span data-stu-id="c4d2c-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d2c-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4d2c-183">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d2c-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4d2c-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4d2c-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4d2c-185">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d2c-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4d2c-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4d2c-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4d2c-187">Namespace</span></span><br/>                | <span data-ttu-id="c4d2c-188">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c4d2c-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c4d2c-189">MOF</span><span class="sxs-lookup"><span data-stu-id="c4d2c-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4d2c-190"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4d2c-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4d2c-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4d2c-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d2c-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d2c-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d2c-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4d2c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d2c-194">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c4d2c-195">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c4d2c-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="c4d2c-196">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c4d2c-197">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="c4d2c-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="c4d2c-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c4d2c-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

