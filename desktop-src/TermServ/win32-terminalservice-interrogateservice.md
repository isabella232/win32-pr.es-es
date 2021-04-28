---
title: Método InterrogateService de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método InterrogateService de la clase Win32_Service (Servicios de Escritorio remoto): solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.'
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Método InterrogateService Servicios de Escritorio remoto
- Método InterrogateService Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto método , InterrogateService
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090663"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="6e3f2-106">Método InterrogateService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="6e3f2-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="6e3f2-107">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="6e3f2-108">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="6e3f2-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6e3f2-109">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6e3f2-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3f2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e3f2-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="6e3f2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e3f2-111">Parameters</span></span>

<span data-ttu-id="6e3f2-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e3f2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e3f2-113">Return value</span></span>

<span data-ttu-id="6e3f2-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="6e3f2-115">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6e3f2-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6e3f2-116">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6e3f2-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6e3f2-117">**0**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-119">**1**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-121">**2**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-123">**3**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-125">**4**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-127">**5**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-129">**6**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-131">**7**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-133">**8**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-135">**9**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-136">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-137">**10**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-139">**11**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-141">**12**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-142">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-143">**13**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-145">**14**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-147">**15**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-149">**16**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-151">**17**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-153">**18**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-154">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-155">**19**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-156">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-157">**20**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-159">**21**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-161">**22**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-162">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-163">**23**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6e3f2-165">**24**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="6e3f2-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3f2-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e3f2-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e3f2-167">Requirements</span></span>



| <span data-ttu-id="6e3f2-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e3f2-168">Requirement</span></span> | <span data-ttu-id="6e3f2-169">Valor</span><span class="sxs-lookup"><span data-stu-id="6e3f2-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3f2-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e3f2-170">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3f2-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e3f2-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e3f2-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e3f2-172">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3f2-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e3f2-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e3f2-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e3f2-174">Namespace</span></span><br/>                | <span data-ttu-id="6e3f2-175">\\TerminalServices de CIMv2 \\ raíz</span><span class="sxs-lookup"><span data-stu-id="6e3f2-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6e3f2-176">MOF</span><span class="sxs-lookup"><span data-stu-id="6e3f2-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e3f2-177"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e3f2-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e3f2-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e3f2-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e3f2-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e3f2-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e3f2-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e3f2-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3f2-181">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="6e3f2-182">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6e3f2-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="6e3f2-183">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="6e3f2-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="6e3f2-184">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="6e3f2-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

