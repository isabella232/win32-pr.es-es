---
title: Método ResumeService de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método ResumeService de la clase Win32_Service (Servicios de Escritorio remoto): intenta colocar el servicio al que se hace referencia en el estado reanudado.'
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- Método ResumeService Servicios de Escritorio remoto
- Método ResumeService Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto , método ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f8e7dcfc9b9bd5b408e36d8a909aa10c84519c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090593"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="8f945-106">Método ResumeService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="8f945-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="8f945-107">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** intenta colocar el servicio al que se hace referencia en estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="8f945-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="8f945-108">En este tema se usa Managed Object Format sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="8f945-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f945-109">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f945-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f945-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f945-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="8f945-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f945-111">Parameters</span></span>

<span data-ttu-id="8f945-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8f945-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f945-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f945-113">Return value</span></span>

<span data-ttu-id="8f945-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8f945-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8f945-115">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8f945-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8f945-116">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8f945-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8f945-117">**0**</span><span class="sxs-lookup"><span data-stu-id="8f945-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f945-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-119">**1**</span><span class="sxs-lookup"><span data-stu-id="8f945-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f945-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-121">**2**</span><span class="sxs-lookup"><span data-stu-id="8f945-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="8f945-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-123">**3**</span><span class="sxs-lookup"><span data-stu-id="8f945-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="8f945-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-125">**4**</span><span class="sxs-lookup"><span data-stu-id="8f945-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-127">**5**</span><span class="sxs-lookup"><span data-stu-id="8f945-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="8f945-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-129">**6**</span><span class="sxs-lookup"><span data-stu-id="8f945-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="8f945-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-131">**7**</span><span class="sxs-lookup"><span data-stu-id="8f945-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-133">**8**</span><span class="sxs-lookup"><span data-stu-id="8f945-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-135">**9**</span><span class="sxs-lookup"><span data-stu-id="8f945-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-136">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-137">**10**</span><span class="sxs-lookup"><span data-stu-id="8f945-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8f945-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-139">**11**</span><span class="sxs-lookup"><span data-stu-id="8f945-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="8f945-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-141">**12**</span><span class="sxs-lookup"><span data-stu-id="8f945-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-142">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-143">**13**</span><span class="sxs-lookup"><span data-stu-id="8f945-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="8f945-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-145">**14**</span><span class="sxs-lookup"><span data-stu-id="8f945-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f945-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-147">**15**</span><span class="sxs-lookup"><span data-stu-id="8f945-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8f945-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-149">**16**</span><span class="sxs-lookup"><span data-stu-id="8f945-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f945-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-151">**17**</span><span class="sxs-lookup"><span data-stu-id="8f945-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="8f945-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-153">**18**</span><span class="sxs-lookup"><span data-stu-id="8f945-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-154">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="8f945-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-155">**19**</span><span class="sxs-lookup"><span data-stu-id="8f945-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-156">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="8f945-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-157">**20**</span><span class="sxs-lookup"><span data-stu-id="8f945-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="8f945-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-159">**21**</span><span class="sxs-lookup"><span data-stu-id="8f945-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-161">**22**</span><span class="sxs-lookup"><span data-stu-id="8f945-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-162">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-163">**23**</span><span class="sxs-lookup"><span data-stu-id="8f945-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f945-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f945-165">**24**</span><span class="sxs-lookup"><span data-stu-id="8f945-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8f945-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8f945-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f945-167">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f945-167">Remarks</span></span>

<span data-ttu-id="8f945-168">Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio que se detiene y un servicio que está en pausa, los dos estados aparecen de forma diferente al SCM.</span><span class="sxs-lookup"><span data-stu-id="8f945-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="8f945-169">Un servicio detenido es un servicio que no se está ejecutando y debe pasar por todo el procedimiento de inicio del servicio.</span><span class="sxs-lookup"><span data-stu-id="8f945-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="8f945-170">Sin embargo, un servicio en pausa todavía se está ejecutando, pero se ha suspendido su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="8f945-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="8f945-171">Por este problema, un servicio en pausa no necesita pasar por todo el procedimiento de inicio del servicio, sino que necesita un procedimiento diferente para reanudar el funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="8f945-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="8f945-172">Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado.</span><span class="sxs-lookup"><span data-stu-id="8f945-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="8f945-173">Los [**métodos \_ del servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) y **ResumeService** deben usarse en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f945-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="8f945-174">Si un servicio está detenido actualmente, debe usar el [**método StartService**](win32-terminalservice-startservice.md) para reiniciarlo. **ResumeService** no puede iniciar un servicio que está detenido actualmente.</span><span class="sxs-lookup"><span data-stu-id="8f945-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="8f945-175">Si un servicio está en pausa, debe usar **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="8f945-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="8f945-176">Si usa el [**método StartService**](win32-terminalservice-startservice.md) en un servicio en pausa, recibirá el mensaje "El servicio ya se está ejecutando".</span><span class="sxs-lookup"><span data-stu-id="8f945-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="8f945-177">Sin embargo, el servicio permanece en pausa hasta que se le envía el código de control de servicio de reanudación.</span><span class="sxs-lookup"><span data-stu-id="8f945-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="8f945-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f945-178">Examples</span></span>

<span data-ttu-id="8f945-179">En [el ejemplo Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript (Reanudar servicios de inicio automático que son VBScript en pausa) se reinician los servicios de inicio automático que se han pausado.</span><span class="sxs-lookup"><span data-stu-id="8f945-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f945-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f945-180">Requirements</span></span>



| <span data-ttu-id="8f945-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f945-181">Requirement</span></span> | <span data-ttu-id="8f945-182">Valor</span><span class="sxs-lookup"><span data-stu-id="8f945-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f945-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f945-183">Minimum supported client</span></span><br/> | <span data-ttu-id="8f945-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f945-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f945-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f945-185">Minimum supported server</span></span><br/> | <span data-ttu-id="8f945-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f945-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f945-187">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f945-187">Namespace</span></span><br/>                | <span data-ttu-id="8f945-188">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f945-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f945-189">MOF</span><span class="sxs-lookup"><span data-stu-id="8f945-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f945-190"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f945-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f945-191">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f945-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f945-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f945-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f945-193">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f945-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f945-194">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="8f945-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="8f945-195">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8f945-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="8f945-196">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8f945-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="8f945-197">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="8f945-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

