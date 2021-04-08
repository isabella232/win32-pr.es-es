---
description: Intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_Service (proveedores WMI de CIMWin32)
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
ms.openlocfilehash: 8c523617826bd5d608b8c6b1ee242863f7591a61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000764"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="510ab-103">Método UserControlService de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="510ab-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="510ab-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** intenta enviar un código de control definido por el usuario al servicio al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="510ab-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="510ab-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="510ab-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="510ab-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="510ab-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="510ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="510ab-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="510ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="510ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="510ab-109">*ControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="510ab-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="510ab-110">Especifica los valores definidos (de 128 a 255) que proporcionan comandos de control específicos para un usuario.</span><span class="sxs-lookup"><span data-stu-id="510ab-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="510ab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="510ab-111">Return value</span></span>

<span data-ttu-id="510ab-112">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="510ab-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="510ab-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="510ab-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="510ab-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="510ab-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="510ab-115">**0**</span><span class="sxs-lookup"><span data-stu-id="510ab-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-116">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="510ab-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-117">**1**</span><span class="sxs-lookup"><span data-stu-id="510ab-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-118">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="510ab-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-119">**2**</span><span class="sxs-lookup"><span data-stu-id="510ab-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-120">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="510ab-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-121">**3**</span><span class="sxs-lookup"><span data-stu-id="510ab-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-122">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="510ab-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-123">**4**</span><span class="sxs-lookup"><span data-stu-id="510ab-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-124">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-125">**5**</span><span class="sxs-lookup"><span data-stu-id="510ab-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-126">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="510ab-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-127">**6**</span><span class="sxs-lookup"><span data-stu-id="510ab-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-128">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="510ab-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-129">**7**</span><span class="sxs-lookup"><span data-stu-id="510ab-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-130">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-131">**8**</span><span class="sxs-lookup"><span data-stu-id="510ab-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-132">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-133">**9**</span><span class="sxs-lookup"><span data-stu-id="510ab-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-134">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-135">**10**</span><span class="sxs-lookup"><span data-stu-id="510ab-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-136">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="510ab-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-137">**11**</span><span class="sxs-lookup"><span data-stu-id="510ab-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-138">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="510ab-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-139">**12**</span><span class="sxs-lookup"><span data-stu-id="510ab-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-140">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-141">**13**</span><span class="sxs-lookup"><span data-stu-id="510ab-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-142">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="510ab-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-143">**14**</span><span class="sxs-lookup"><span data-stu-id="510ab-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-144">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-145">**15**</span><span class="sxs-lookup"><span data-stu-id="510ab-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-146">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-147">**16**</span><span class="sxs-lookup"><span data-stu-id="510ab-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-148">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-149">**17**</span><span class="sxs-lookup"><span data-stu-id="510ab-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-150">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="510ab-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-151">**18**</span><span class="sxs-lookup"><span data-stu-id="510ab-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-152">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="510ab-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-153">**19**</span><span class="sxs-lookup"><span data-stu-id="510ab-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-154">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="510ab-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-155">**20**</span><span class="sxs-lookup"><span data-stu-id="510ab-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-156">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="510ab-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-157">**21**</span><span class="sxs-lookup"><span data-stu-id="510ab-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-158">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-159">**22**</span><span class="sxs-lookup"><span data-stu-id="510ab-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-160">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="510ab-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-161">**23**</span><span class="sxs-lookup"><span data-stu-id="510ab-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-162">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="510ab-163">**24**</span><span class="sxs-lookup"><span data-stu-id="510ab-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="510ab-164">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="510ab-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="510ab-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="510ab-165">Requirements</span></span>



| <span data-ttu-id="510ab-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="510ab-166">Requirement</span></span> | <span data-ttu-id="510ab-167">Value</span><span class="sxs-lookup"><span data-stu-id="510ab-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="510ab-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="510ab-168">Minimum supported client</span></span><br/> | <span data-ttu-id="510ab-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="510ab-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="510ab-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="510ab-170">Minimum supported server</span></span><br/> | <span data-ttu-id="510ab-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="510ab-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="510ab-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="510ab-172">Namespace</span></span><br/>                | <span data-ttu-id="510ab-173">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="510ab-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="510ab-174">MOF</span><span class="sxs-lookup"><span data-stu-id="510ab-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="510ab-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="510ab-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="510ab-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="510ab-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="510ab-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="510ab-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="510ab-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="510ab-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="510ab-179">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="510ab-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="510ab-180">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="510ab-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

