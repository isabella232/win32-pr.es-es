---
title: Método UserControlService de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método UserControlService de la clase Win32_Service (Servicios de Escritorio remoto): intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.'
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- Método UserControlService Servicios de Escritorio remoto
- Método UserControlService Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto método , UserControlService
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090613"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="a1715-106">Método UserControlService de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="a1715-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="a1715-107">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="a1715-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="a1715-108">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="a1715-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a1715-109">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a1715-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1715-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1715-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="a1715-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1715-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1715-112">*ControlCode* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1715-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1715-113">Especifica valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="a1715-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1715-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1715-114">Return value</span></span>

<span data-ttu-id="a1715-115">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a1715-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a1715-116">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a1715-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a1715-117">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a1715-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a1715-118">**0**</span><span class="sxs-lookup"><span data-stu-id="a1715-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-119">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1715-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-120">**1**</span><span class="sxs-lookup"><span data-stu-id="a1715-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-121">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1715-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-122">**2**</span><span class="sxs-lookup"><span data-stu-id="a1715-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-123">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="a1715-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-124">**3**</span><span class="sxs-lookup"><span data-stu-id="a1715-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-125">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="a1715-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-126">**4**</span><span class="sxs-lookup"><span data-stu-id="a1715-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-127">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-128">**5**</span><span class="sxs-lookup"><span data-stu-id="a1715-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-129">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="a1715-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-130">**6**</span><span class="sxs-lookup"><span data-stu-id="a1715-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-131">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="a1715-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-132">**7**</span><span class="sxs-lookup"><span data-stu-id="a1715-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-133">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-134">**8**</span><span class="sxs-lookup"><span data-stu-id="a1715-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-135">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-136">**9**</span><span class="sxs-lookup"><span data-stu-id="a1715-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-137">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-138">**10**</span><span class="sxs-lookup"><span data-stu-id="a1715-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-139">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a1715-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-140">**11**</span><span class="sxs-lookup"><span data-stu-id="a1715-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-141">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a1715-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-142">**12**</span><span class="sxs-lookup"><span data-stu-id="a1715-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-143">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-144">**13**</span><span class="sxs-lookup"><span data-stu-id="a1715-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-145">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="a1715-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-146">**14**</span><span class="sxs-lookup"><span data-stu-id="a1715-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-147">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a1715-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-148">**15**</span><span class="sxs-lookup"><span data-stu-id="a1715-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-149">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a1715-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-150">**16**</span><span class="sxs-lookup"><span data-stu-id="a1715-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-151">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="a1715-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-152">**17**</span><span class="sxs-lookup"><span data-stu-id="a1715-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-153">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a1715-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-154">**18**</span><span class="sxs-lookup"><span data-stu-id="a1715-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-155">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="a1715-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-156">**19**</span><span class="sxs-lookup"><span data-stu-id="a1715-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-157">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="a1715-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-158">**20**</span><span class="sxs-lookup"><span data-stu-id="a1715-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-159">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="a1715-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-160">**21**</span><span class="sxs-lookup"><span data-stu-id="a1715-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-161">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-162">**22**</span><span class="sxs-lookup"><span data-stu-id="a1715-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-163">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a1715-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-164">**23**</span><span class="sxs-lookup"><span data-stu-id="a1715-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-165">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="a1715-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a1715-166">**24**</span><span class="sxs-lookup"><span data-stu-id="a1715-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a1715-167">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a1715-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1715-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1715-168">Requirements</span></span>



| <span data-ttu-id="a1715-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1715-169">Requirement</span></span> | <span data-ttu-id="a1715-170">Valor</span><span class="sxs-lookup"><span data-stu-id="a1715-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1715-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1715-171">Minimum supported client</span></span><br/> | <span data-ttu-id="a1715-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1715-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1715-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1715-173">Minimum supported server</span></span><br/> | <span data-ttu-id="a1715-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1715-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1715-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1715-175">Namespace</span></span><br/>                | <span data-ttu-id="a1715-176">\\TerminalServices de CIMv2 \\ raíz</span><span class="sxs-lookup"><span data-stu-id="a1715-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a1715-177">MOF</span><span class="sxs-lookup"><span data-stu-id="a1715-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1715-178"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1715-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1715-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1715-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1715-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1715-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1715-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1715-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1715-182">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="a1715-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="a1715-183">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a1715-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="a1715-184">**TerminalService de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a1715-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

