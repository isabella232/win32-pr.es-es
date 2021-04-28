---
description: 'Método InterrogateService de la clase Win32_Service (proveedores WMI CIMWin32): solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.'
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Método InterrogateService de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9702bc3fbd0a9969db20a8f1326c31b9ea7d925d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096983"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="92c84-103">Método InterrogateService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="92c84-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="92c84-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="92c84-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="92c84-105">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="92c84-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="92c84-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="92c84-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="92c84-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92c84-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="92c84-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92c84-108">Parameters</span></span>

<span data-ttu-id="92c84-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="92c84-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92c84-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92c84-110">Return value</span></span>

<span data-ttu-id="92c84-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="92c84-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="92c84-112">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="92c84-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="92c84-113">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="92c84-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="92c84-114">**0**</span><span class="sxs-lookup"><span data-stu-id="92c84-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="92c84-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-116">**1**</span><span class="sxs-lookup"><span data-stu-id="92c84-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="92c84-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-118">**2**</span><span class="sxs-lookup"><span data-stu-id="92c84-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="92c84-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-120">**3**</span><span class="sxs-lookup"><span data-stu-id="92c84-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="92c84-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-122">**4**</span><span class="sxs-lookup"><span data-stu-id="92c84-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-124">**5**</span><span class="sxs-lookup"><span data-stu-id="92c84-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**Propiedad** State) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="92c84-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-126">**6**</span><span class="sxs-lookup"><span data-stu-id="92c84-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="92c84-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-128">**7**</span><span class="sxs-lookup"><span data-stu-id="92c84-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-130">**8**</span><span class="sxs-lookup"><span data-stu-id="92c84-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-132">**9**</span><span class="sxs-lookup"><span data-stu-id="92c84-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-133">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-134">**10**</span><span class="sxs-lookup"><span data-stu-id="92c84-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="92c84-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-136">**11**</span><span class="sxs-lookup"><span data-stu-id="92c84-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="92c84-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-138">**12**</span><span class="sxs-lookup"><span data-stu-id="92c84-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-139">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-140">**13**</span><span class="sxs-lookup"><span data-stu-id="92c84-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="92c84-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-142">**14**</span><span class="sxs-lookup"><span data-stu-id="92c84-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="92c84-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-144">**15**</span><span class="sxs-lookup"><span data-stu-id="92c84-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="92c84-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-146">**16**</span><span class="sxs-lookup"><span data-stu-id="92c84-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="92c84-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-148">**17**</span><span class="sxs-lookup"><span data-stu-id="92c84-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="92c84-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-150">**18**</span><span class="sxs-lookup"><span data-stu-id="92c84-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-151">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="92c84-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-152">**19**</span><span class="sxs-lookup"><span data-stu-id="92c84-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-153">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="92c84-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-154">**20**</span><span class="sxs-lookup"><span data-stu-id="92c84-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="92c84-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-156">**21**</span><span class="sxs-lookup"><span data-stu-id="92c84-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-158">**22**</span><span class="sxs-lookup"><span data-stu-id="92c84-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-159">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="92c84-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-160">**23**</span><span class="sxs-lookup"><span data-stu-id="92c84-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="92c84-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="92c84-162">**24**</span><span class="sxs-lookup"><span data-stu-id="92c84-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="92c84-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="92c84-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92c84-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c84-164">Requirements</span></span>



| <span data-ttu-id="92c84-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c84-165">Requirement</span></span> | <span data-ttu-id="92c84-166">Valor</span><span class="sxs-lookup"><span data-stu-id="92c84-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c84-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92c84-167">Minimum supported client</span></span><br/> | <span data-ttu-id="92c84-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92c84-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92c84-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92c84-169">Minimum supported server</span></span><br/> | <span data-ttu-id="92c84-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c84-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92c84-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="92c84-171">Namespace</span></span><br/>                | <span data-ttu-id="92c84-172">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="92c84-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92c84-173">MOF</span><span class="sxs-lookup"><span data-stu-id="92c84-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c84-174"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c84-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c84-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92c84-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c84-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c84-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c84-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="92c84-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c84-178">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="92c84-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="92c84-179">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92c84-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92c84-180">**BaseService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="92c84-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="92c84-181">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="92c84-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

