---
description: Coloca el servicio representado por el \_ objeto SystemDriver de Win32 en estado detenido.
ms.assetid: 0fa8ef44-39eb-448e-8d33-38a5af9a0c13
ms.tgt_platform: multiple
title: Método StopService de la clase Win32_SystemDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb45a414ea9cc7198487dbb61d122722816f4728
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000592"
---
# <a name="stopservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="9087a-103">Método StopService de la \_ clase SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="9087a-103">StopService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="9087a-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio representado por el objeto [**\_ SystemDriver de Win32**](win32-systemdriver.md) en el estado Stopped.</span><span class="sxs-lookup"><span data-stu-id="9087a-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_SystemDriver**](win32-systemdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="9087a-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9087a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9087a-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9087a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9087a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9087a-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="9087a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9087a-108">Parameters</span></span>

<span data-ttu-id="9087a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9087a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9087a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9087a-110">Return value</span></span>

<span data-ttu-id="9087a-111">Devuelve un valor de 0 (cero) si el servicio se detuvo correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9087a-111">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9087a-112">**0**</span><span class="sxs-lookup"><span data-stu-id="9087a-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-113">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9087a-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-114">**1**</span><span class="sxs-lookup"><span data-stu-id="9087a-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-115">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9087a-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-116">**2**</span><span class="sxs-lookup"><span data-stu-id="9087a-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-117">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="9087a-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-118">**3**</span><span class="sxs-lookup"><span data-stu-id="9087a-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-119">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="9087a-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-120">**4**</span><span class="sxs-lookup"><span data-stu-id="9087a-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-121">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-122">**5**</span><span class="sxs-lookup"><span data-stu-id="9087a-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-123">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="9087a-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-124">**6**</span><span class="sxs-lookup"><span data-stu-id="9087a-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-125">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="9087a-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-126">**7**</span><span class="sxs-lookup"><span data-stu-id="9087a-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-127">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-128">**8**</span><span class="sxs-lookup"><span data-stu-id="9087a-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-129">Se produjo un error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-130">**9**</span><span class="sxs-lookup"><span data-stu-id="9087a-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-131">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-132">**10**</span><span class="sxs-lookup"><span data-stu-id="9087a-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-133">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9087a-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-134">**11**</span><span class="sxs-lookup"><span data-stu-id="9087a-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-135">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="9087a-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-136">**12**</span><span class="sxs-lookup"><span data-stu-id="9087a-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-137">Una dependencia para la que se basa este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-138">**13**</span><span class="sxs-lookup"><span data-stu-id="9087a-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-139">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="9087a-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-140">**14**</span><span class="sxs-lookup"><span data-stu-id="9087a-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-141">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-142">**15**</span><span class="sxs-lookup"><span data-stu-id="9087a-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-143">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-144">**16**</span><span class="sxs-lookup"><span data-stu-id="9087a-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-145">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-146">**17**</span><span class="sxs-lookup"><span data-stu-id="9087a-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-147">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-148">**18**</span><span class="sxs-lookup"><span data-stu-id="9087a-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-149">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-150">**19**</span><span class="sxs-lookup"><span data-stu-id="9087a-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-151">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="9087a-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-152">**20**</span><span class="sxs-lookup"><span data-stu-id="9087a-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-153">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-154">**21**</span><span class="sxs-lookup"><span data-stu-id="9087a-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-155">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-156">**22**</span><span class="sxs-lookup"><span data-stu-id="9087a-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-157">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9087a-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-158">**23**</span><span class="sxs-lookup"><span data-stu-id="9087a-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-159">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9087a-160">**24**</span><span class="sxs-lookup"><span data-stu-id="9087a-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="9087a-161">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9087a-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9087a-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9087a-162">Examples</span></span>

<span data-ttu-id="9087a-163">El siguiente código de PowerShell detiene el servicio "clase de impresora USB de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="9087a-163">The following PowerShell code stops the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StopService()
"Stop Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="9087a-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9087a-164">Requirements</span></span>



| <span data-ttu-id="9087a-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="9087a-165">Requirement</span></span> | <span data-ttu-id="9087a-166">Value</span><span class="sxs-lookup"><span data-stu-id="9087a-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9087a-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9087a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9087a-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9087a-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9087a-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9087a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9087a-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9087a-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9087a-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9087a-171">Namespace</span></span><br/>                | <span data-ttu-id="9087a-172">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9087a-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9087a-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9087a-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9087a-174"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="9087a-174"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="9087a-175">MOF</span><span class="sxs-lookup"><span data-stu-id="9087a-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9087a-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9087a-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9087a-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9087a-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9087a-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9087a-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9087a-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="9087a-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="9087a-180">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9087a-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9087a-181">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="9087a-181">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

