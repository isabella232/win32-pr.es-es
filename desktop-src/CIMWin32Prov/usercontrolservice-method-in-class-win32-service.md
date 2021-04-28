---
description: 'Método UserControlService de la clase Win32_Service (proveedores WMI CIMWin32): intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.'
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100012"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="e116b-103">Método UserControlService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e116b-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e116b-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="e116b-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="e116b-105">En este tema se Managed Object Format sintaxis de MOF .</span><span class="sxs-lookup"><span data-stu-id="e116b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e116b-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e116b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e116b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e116b-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="e116b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e116b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e116b-109">*ControlCode* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e116b-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e116b-110">Especifica valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="e116b-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e116b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e116b-111">Return value</span></span>

<span data-ttu-id="e116b-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="e116b-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e116b-113">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e116b-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e116b-114">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e116b-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e116b-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e116b-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-116">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e116b-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-117">**1**</span><span class="sxs-lookup"><span data-stu-id="e116b-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-118">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e116b-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-119">**2**</span><span class="sxs-lookup"><span data-stu-id="e116b-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-120">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="e116b-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-121">**3**</span><span class="sxs-lookup"><span data-stu-id="e116b-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-122">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="e116b-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-123">**4**</span><span class="sxs-lookup"><span data-stu-id="e116b-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-124">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-125">**5**</span><span class="sxs-lookup"><span data-stu-id="e116b-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-126">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**Propiedad** State) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="e116b-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-127">**6**</span><span class="sxs-lookup"><span data-stu-id="e116b-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-128">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="e116b-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-129">**7**</span><span class="sxs-lookup"><span data-stu-id="e116b-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-130">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-131">**8**</span><span class="sxs-lookup"><span data-stu-id="e116b-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-132">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-133">**9**</span><span class="sxs-lookup"><span data-stu-id="e116b-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-134">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-135">**10**</span><span class="sxs-lookup"><span data-stu-id="e116b-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-136">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="e116b-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-137">**11**</span><span class="sxs-lookup"><span data-stu-id="e116b-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-138">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e116b-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-139">**12**</span><span class="sxs-lookup"><span data-stu-id="e116b-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-140">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-141">**13**</span><span class="sxs-lookup"><span data-stu-id="e116b-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-142">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="e116b-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-143">**14**</span><span class="sxs-lookup"><span data-stu-id="e116b-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-144">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="e116b-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-145">**15**</span><span class="sxs-lookup"><span data-stu-id="e116b-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-146">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e116b-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-147">**16**</span><span class="sxs-lookup"><span data-stu-id="e116b-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-148">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="e116b-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-149">**17**</span><span class="sxs-lookup"><span data-stu-id="e116b-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-150">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e116b-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-151">**18**</span><span class="sxs-lookup"><span data-stu-id="e116b-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-152">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="e116b-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-153">**19**</span><span class="sxs-lookup"><span data-stu-id="e116b-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-154">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="e116b-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-155">**20**</span><span class="sxs-lookup"><span data-stu-id="e116b-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-156">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="e116b-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-157">**21**</span><span class="sxs-lookup"><span data-stu-id="e116b-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-158">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-159">**22**</span><span class="sxs-lookup"><span data-stu-id="e116b-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-160">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="e116b-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-161">**23**</span><span class="sxs-lookup"><span data-stu-id="e116b-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-162">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="e116b-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e116b-163">**24**</span><span class="sxs-lookup"><span data-stu-id="e116b-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="e116b-164">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e116b-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e116b-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e116b-165">Requirements</span></span>



| <span data-ttu-id="e116b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="e116b-166">Requirement</span></span> | <span data-ttu-id="e116b-167">Valor</span><span class="sxs-lookup"><span data-stu-id="e116b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e116b-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e116b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="e116b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e116b-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e116b-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e116b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="e116b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e116b-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e116b-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e116b-172">Namespace</span></span><br/>                | <span data-ttu-id="e116b-173">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="e116b-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e116b-174">MOF</span><span class="sxs-lookup"><span data-stu-id="e116b-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e116b-175"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e116b-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e116b-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e116b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e116b-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e116b-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e116b-178">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e116b-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="e116b-179">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e116b-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e116b-180">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="e116b-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

