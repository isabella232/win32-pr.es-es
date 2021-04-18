---
title: Método InterrogateService de la clase Win32_Service (Servicios de Escritorio remoto)
description: Solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Método InterrogateService Servicios de Escritorio remoto
- Método InterrogateService Servicios de Escritorio remoto, clase Win32_Service
- Win32_Service Servicios de Escritorio remoto de clase, método InterrogateService
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
ms.openlocfilehash: 6f53b3d5e1cced6b6820f9b7334551de47f333be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685974"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="5d7fe-106">Método InterrogateService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="5d7fe-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="5d7fe-107">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio al que se hace referencia actualice su estado con el administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="5d7fe-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5d7fe-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5d7fe-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5d7fe-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7fe-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d7fe-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="5d7fe-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d7fe-111">Parameters</span></span>

<span data-ttu-id="5d7fe-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d7fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d7fe-113">Return value</span></span>

<span data-ttu-id="5d7fe-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="5d7fe-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5d7fe-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5d7fe-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5d7fe-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5d7fe-117">**0**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-119">**1**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-121">**2**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-123">**3**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-125">**4**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-127">**5**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-129">**6**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-131">**7**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-133">**8**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-135">**9**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-136">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-137">**10**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-139">**11**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-141">**12**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-142">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-143">**13**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-145">**14**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-147">**15**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-149">**16**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-151">**17**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-153">**18**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-154">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-155">**19**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-156">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-157">**20**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-159">**21**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-161">**22**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-162">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-163">**23**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-165">**24**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d7fe-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7fe-167">Requirements</span></span>



| <span data-ttu-id="5d7fe-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7fe-168">Requirement</span></span> | <span data-ttu-id="5d7fe-169">Value</span><span class="sxs-lookup"><span data-stu-id="5d7fe-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7fe-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7fe-170">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7fe-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d7fe-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d7fe-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7fe-172">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7fe-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d7fe-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d7fe-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d7fe-174">Namespace</span></span><br/>                | <span data-ttu-id="5d7fe-175">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5d7fe-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5d7fe-176">MOF</span><span class="sxs-lookup"><span data-stu-id="5d7fe-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d7fe-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d7fe-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d7fe-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d7fe-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d7fe-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d7fe-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7fe-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d7fe-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7fe-181">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="5d7fe-182">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5d7fe-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="5d7fe-183">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5d7fe-184">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="5d7fe-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

