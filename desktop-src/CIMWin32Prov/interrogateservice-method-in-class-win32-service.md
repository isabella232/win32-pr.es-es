---
description: Solicita que el servicio al que se hace referencia actualice su estado al administrador de servicios.
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
ms.openlocfilehash: 7ad1f56afcbe42ced19da823c454291a7b5282d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152988"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="b75d5-103">Método InterrogateService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b75d5-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b75d5-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio al que se hace referencia actualice su estado con el administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="b75d5-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="b75d5-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b75d5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b75d5-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b75d5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b75d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b75d5-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="b75d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b75d5-108">Parameters</span></span>

<span data-ttu-id="b75d5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b75d5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b75d5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b75d5-110">Return value</span></span>

<span data-ttu-id="b75d5-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="b75d5-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b75d5-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b75d5-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b75d5-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b75d5-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b75d5-114">**0**</span><span class="sxs-lookup"><span data-stu-id="b75d5-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b75d5-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-116">**1**</span><span class="sxs-lookup"><span data-stu-id="b75d5-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b75d5-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-118">**2**</span><span class="sxs-lookup"><span data-stu-id="b75d5-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="b75d5-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-120">**3**</span><span class="sxs-lookup"><span data-stu-id="b75d5-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="b75d5-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-122">**4**</span><span class="sxs-lookup"><span data-stu-id="b75d5-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-124">**5**</span><span class="sxs-lookup"><span data-stu-id="b75d5-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="b75d5-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-126">**6**</span><span class="sxs-lookup"><span data-stu-id="b75d5-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="b75d5-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-128">**7**</span><span class="sxs-lookup"><span data-stu-id="b75d5-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-130">**8**</span><span class="sxs-lookup"><span data-stu-id="b75d5-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-132">**9**</span><span class="sxs-lookup"><span data-stu-id="b75d5-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-133">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-134">**10**</span><span class="sxs-lookup"><span data-stu-id="b75d5-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b75d5-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-136">**11**</span><span class="sxs-lookup"><span data-stu-id="b75d5-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="b75d5-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-138">**12**</span><span class="sxs-lookup"><span data-stu-id="b75d5-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-139">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-140">**13**</span><span class="sxs-lookup"><span data-stu-id="b75d5-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="b75d5-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-142">**14**</span><span class="sxs-lookup"><span data-stu-id="b75d5-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-144">**15**</span><span class="sxs-lookup"><span data-stu-id="b75d5-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-146">**16**</span><span class="sxs-lookup"><span data-stu-id="b75d5-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-148">**17**</span><span class="sxs-lookup"><span data-stu-id="b75d5-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b75d5-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-150">**18**</span><span class="sxs-lookup"><span data-stu-id="b75d5-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-151">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="b75d5-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-152">**19**</span><span class="sxs-lookup"><span data-stu-id="b75d5-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-153">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="b75d5-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-154">**20**</span><span class="sxs-lookup"><span data-stu-id="b75d5-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="b75d5-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-156">**21**</span><span class="sxs-lookup"><span data-stu-id="b75d5-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-158">**22**</span><span class="sxs-lookup"><span data-stu-id="b75d5-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-159">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="b75d5-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-160">**23**</span><span class="sxs-lookup"><span data-stu-id="b75d5-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b75d5-162">**24**</span><span class="sxs-lookup"><span data-stu-id="b75d5-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b75d5-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b75d5-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b75d5-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b75d5-164">Requirements</span></span>



| <span data-ttu-id="b75d5-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b75d5-165">Requirement</span></span> | <span data-ttu-id="b75d5-166">Value</span><span class="sxs-lookup"><span data-stu-id="b75d5-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b75d5-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b75d5-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b75d5-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b75d5-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b75d5-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b75d5-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b75d5-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b75d5-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b75d5-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b75d5-171">Namespace</span></span><br/>                | <span data-ttu-id="b75d5-172">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b75d5-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b75d5-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b75d5-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b75d5-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b75d5-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b75d5-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b75d5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b75d5-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b75d5-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b75d5-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="b75d5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75d5-178">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="b75d5-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="b75d5-179">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b75d5-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b75d5-180">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="b75d5-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="b75d5-181">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="b75d5-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

