---
description: Intenta colocar el servicio administrado por el controlador del sistema en el estado de reanudación.
ms.assetid: 16bacf06-4236-4d58-9b09-cb86bb73d78a
ms.tgt_platform: multiple
title: Método ResumeService de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d326fcd0a3bc9801f5e214cdc8740170cf1f1cf8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998159"
---
# <a name="resumeservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="42362-103">Método ResumeService de la \_ clase SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="42362-103">ResumeService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="42362-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** intenta colocar el servicio administrado por el controlador del sistema en el estado de reanudación.</span><span class="sxs-lookup"><span data-stu-id="42362-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the system driver in the resumed state.</span></span>

<span data-ttu-id="42362-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="42362-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="42362-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="42362-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="42362-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42362-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="42362-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42362-108">Parameters</span></span>

<span data-ttu-id="42362-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="42362-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42362-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42362-110">Return value</span></span>

<span data-ttu-id="42362-111">Devuelve un valor de 0 (cero) si se aceptó la solicitud **ResumeService** , 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="42362-111">Returns a value of 0 (zero) if the **ResumeService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="42362-112">**0**</span><span class="sxs-lookup"><span data-stu-id="42362-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="42362-113">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42362-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="42362-114">**1**</span><span class="sxs-lookup"><span data-stu-id="42362-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="42362-115">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42362-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="42362-116">**2**</span><span class="sxs-lookup"><span data-stu-id="42362-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="42362-117">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="42362-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="42362-118">**3**</span><span class="sxs-lookup"><span data-stu-id="42362-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="42362-119">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="42362-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="42362-120">**4**</span><span class="sxs-lookup"><span data-stu-id="42362-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="42362-121">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-122">**5**</span><span class="sxs-lookup"><span data-stu-id="42362-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="42362-123">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="42362-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="42362-124">**6**</span><span class="sxs-lookup"><span data-stu-id="42362-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="42362-125">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="42362-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="42362-126">**7**</span><span class="sxs-lookup"><span data-stu-id="42362-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="42362-127">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="42362-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="42362-128">**8**</span><span class="sxs-lookup"><span data-stu-id="42362-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="42362-129">Se produjo un error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-130">**9**</span><span class="sxs-lookup"><span data-stu-id="42362-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="42362-131">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="42362-132">**10**</span><span class="sxs-lookup"><span data-stu-id="42362-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="42362-133">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="42362-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="42362-134">**11**</span><span class="sxs-lookup"><span data-stu-id="42362-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="42362-135">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="42362-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="42362-136">**12**</span><span class="sxs-lookup"><span data-stu-id="42362-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="42362-137">Una dependencia para la que se basa este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="42362-138">**13**</span><span class="sxs-lookup"><span data-stu-id="42362-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="42362-139">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="42362-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-140">**14**</span><span class="sxs-lookup"><span data-stu-id="42362-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="42362-141">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="42362-142">**15**</span><span class="sxs-lookup"><span data-stu-id="42362-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="42362-143">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="42362-144">**16**</span><span class="sxs-lookup"><span data-stu-id="42362-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="42362-145">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="42362-146">**17**</span><span class="sxs-lookup"><span data-stu-id="42362-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="42362-147">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-148">**18**</span><span class="sxs-lookup"><span data-stu-id="42362-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="42362-149">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-150">**19**</span><span class="sxs-lookup"><span data-stu-id="42362-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="42362-151">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="42362-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="42362-152">**20**</span><span class="sxs-lookup"><span data-stu-id="42362-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="42362-153">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-154">**21**</span><span class="sxs-lookup"><span data-stu-id="42362-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="42362-155">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-156">**22**</span><span class="sxs-lookup"><span data-stu-id="42362-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="42362-157">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="42362-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="42362-158">**23**</span><span class="sxs-lookup"><span data-stu-id="42362-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="42362-159">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="42362-160">**24**</span><span class="sxs-lookup"><span data-stu-id="42362-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="42362-161">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="42362-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="42362-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="42362-162">Examples</span></span>

<span data-ttu-id="42362-163">El siguiente código de PowerShell intenta reanudar el servicio "clase de impresora USB de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="42362-163">The following PowerShell code attempts to resume the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.ResumeService()
"Resume Service Called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="42362-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42362-164">Requirements</span></span>



| <span data-ttu-id="42362-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="42362-165">Requirement</span></span> | <span data-ttu-id="42362-166">Value</span><span class="sxs-lookup"><span data-stu-id="42362-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42362-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42362-167">Minimum supported client</span></span><br/> | <span data-ttu-id="42362-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42362-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42362-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42362-169">Minimum supported server</span></span><br/> | <span data-ttu-id="42362-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42362-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42362-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42362-171">Namespace</span></span><br/>                | <span data-ttu-id="42362-172">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="42362-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42362-173">MOF</span><span class="sxs-lookup"><span data-stu-id="42362-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42362-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42362-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42362-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42362-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42362-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42362-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42362-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="42362-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="42362-178">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42362-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="42362-179">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="42362-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

