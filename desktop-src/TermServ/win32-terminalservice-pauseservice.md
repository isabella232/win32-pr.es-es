---
title: Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método PauseService de la Win32_Service (Servicios de Escritorio remoto): intenta colocar el servicio en estado en pausa.'
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Método PauseService Servicios de Escritorio remoto
- Método PauseService Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto método , PauseService
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
ms.openlocfilehash: 1d7c9847f363d9bc6d1743da6189d2c4290c00dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090603"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="bcbdb-106">Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="bcbdb-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="bcbdb-107">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta colocar el servicio en estado en pausa.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="bcbdb-108">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="bcbdb-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bcbdb-109">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bcbdb-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbdb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcbdb-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="bcbdb-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcbdb-111">Parameters</span></span>

<span data-ttu-id="bcbdb-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcbdb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcbdb-113">Return value</span></span>

<span data-ttu-id="bcbdb-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="bcbdb-115">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bcbdb-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bcbdb-116">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bcbdb-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bcbdb-117">**0**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-119">**1**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-121">**2**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-123">**3**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-125">**4**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-127">**5**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-129">**6**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-131">**7**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-133">**8**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-135">**9**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-136">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-137">**10**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-139">**11**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-141">**12**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-142">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-143">**13**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-145">**14**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-147">**15**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-149">**16**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-151">**17**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-153">**18**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-154">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-155">**19**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-156">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-157">**20**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-159">**21**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-161">**22**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-162">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-163">**23**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bcbdb-165">**24**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="bcbdb-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcbdb-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcbdb-167">Remarks</span></span>

<span data-ttu-id="bcbdb-168">Después de determinar qué servicios se pueden detener o pausar, puede usar los métodos [**StopService**](win32-terminalservice-stopservice.md) y **PauseService** para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="bcbdb-169">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bcbdb-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="bcbdb-170">¿El servicio es capaz de pausar?</span><span class="sxs-lookup"><span data-stu-id="bcbdb-170">Is the service capable of being paused?</span></span> <span data-ttu-id="bcbdb-171">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="bcbdb-172">¿Necesita seguir controlando las solicitudes de cliente de cualquier persona que ya esté conectada al servicio?</span><span class="sxs-lookup"><span data-stu-id="bcbdb-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="bcbdb-173">Si es así, pausar un servicio normalmente le permite controlar los clientes existentes mientras se deniega el acceso a los nuevos clientes.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="bcbdb-174">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="bcbdb-175">¿Necesita volver a configurar un servicio y hacer que los cambios sumen efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="bcbdb-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="bcbdb-176">Aunque las propiedades del servicio se pueden cambiar mientras un servicio está en pausa, la mayoría de ellas no tienen efecto hasta que el servicio se detiene y reinicia realmente.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="bcbdb-177">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="bcbdb-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bcbdb-178">Examples</span></span>

<span data-ttu-id="bcbdb-179">El [ejemplo de VBScript Pausar](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) servicios que se ejecutan en una cuenta específica pausa todos los servicios que se ejecutan en la cuenta de servicio hipotética Netsvc.</span><span class="sxs-lookup"><span data-stu-id="bcbdb-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbdb-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcbdb-180">Requirements</span></span>



| <span data-ttu-id="bcbdb-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbdb-181">Requirement</span></span> | <span data-ttu-id="bcbdb-182">Valor</span><span class="sxs-lookup"><span data-stu-id="bcbdb-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbdb-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcbdb-183">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbdb-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcbdb-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcbdb-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcbdb-185">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbdb-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcbdb-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcbdb-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bcbdb-187">Namespace</span></span><br/>                | <span data-ttu-id="bcbdb-188">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bcbdb-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bcbdb-189">MOF</span><span class="sxs-lookup"><span data-stu-id="bcbdb-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcbdb-190"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcbdb-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcbdb-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bcbdb-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbdb-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbdb-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbdb-193">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcbdb-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbdb-194">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="bcbdb-195">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bcbdb-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="bcbdb-196">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="bcbdb-197">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="bcbdb-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="bcbdb-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="bcbdb-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

