---
description: Intenta poner el servicio en estado de pausa.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Método PauseService de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b1dfa0b956442f74c17dd6a8c054c229a92466a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659396"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="a3c22-103">Método PauseService de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a3c22-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a3c22-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta poner el servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="a3c22-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="a3c22-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3c22-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3c22-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3c22-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c22-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3c22-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="a3c22-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3c22-108">Parameters</span></span>

<span data-ttu-id="a3c22-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a3c22-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3c22-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3c22-110">Return value</span></span>

<span data-ttu-id="a3c22-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="a3c22-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a3c22-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a3c22-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a3c22-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a3c22-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a3c22-114">**0**</span><span class="sxs-lookup"><span data-stu-id="a3c22-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3c22-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-116">**1**</span><span class="sxs-lookup"><span data-stu-id="a3c22-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3c22-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-118">**2**</span><span class="sxs-lookup"><span data-stu-id="a3c22-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="a3c22-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-120">**3**</span><span class="sxs-lookup"><span data-stu-id="a3c22-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="a3c22-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-122">**4**</span><span class="sxs-lookup"><span data-stu-id="a3c22-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-124">**5**</span><span class="sxs-lookup"><span data-stu-id="a3c22-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="a3c22-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-126">**6**</span><span class="sxs-lookup"><span data-stu-id="a3c22-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="a3c22-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-128">**7**</span><span class="sxs-lookup"><span data-stu-id="a3c22-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-130">**8**</span><span class="sxs-lookup"><span data-stu-id="a3c22-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-132">**9**</span><span class="sxs-lookup"><span data-stu-id="a3c22-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-133">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-134">**10**</span><span class="sxs-lookup"><span data-stu-id="a3c22-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a3c22-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-136">**11**</span><span class="sxs-lookup"><span data-stu-id="a3c22-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a3c22-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-138">**12**</span><span class="sxs-lookup"><span data-stu-id="a3c22-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-139">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-140">**13**</span><span class="sxs-lookup"><span data-stu-id="a3c22-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="a3c22-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-142">**14**</span><span class="sxs-lookup"><span data-stu-id="a3c22-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-144">**15**</span><span class="sxs-lookup"><span data-stu-id="a3c22-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-146">**16**</span><span class="sxs-lookup"><span data-stu-id="a3c22-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-148">**17**</span><span class="sxs-lookup"><span data-stu-id="a3c22-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a3c22-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-150">**18**</span><span class="sxs-lookup"><span data-stu-id="a3c22-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-151">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="a3c22-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-152">**19**</span><span class="sxs-lookup"><span data-stu-id="a3c22-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-153">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="a3c22-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-154">**20**</span><span class="sxs-lookup"><span data-stu-id="a3c22-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="a3c22-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-156">**21**</span><span class="sxs-lookup"><span data-stu-id="a3c22-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-158">**22**</span><span class="sxs-lookup"><span data-stu-id="a3c22-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-159">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-160">**23**</span><span class="sxs-lookup"><span data-stu-id="a3c22-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3c22-162">**24**</span><span class="sxs-lookup"><span data-stu-id="a3c22-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a3c22-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a3c22-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3c22-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3c22-164">Remarks</span></span>

<span data-ttu-id="a3c22-165">Después de determinar qué servicios se pueden detener o pausar, puede utilizar los métodos [**StopService**](stopservice-method-in-class-win32-service.md) y [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="a3c22-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="a3c22-166">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3c22-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="a3c22-167">¿Se puede pausar el servicio?</span><span class="sxs-lookup"><span data-stu-id="a3c22-167">Is the service capable of being paused?</span></span> <span data-ttu-id="a3c22-168">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="a3c22-169">¿Necesita seguir controlando las solicitudes de cliente para los usuarios que ya están conectados al servicio?</span><span class="sxs-lookup"><span data-stu-id="a3c22-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="a3c22-170">Si es así, al pausar un servicio normalmente se le permite administrar los clientes existentes a la vez que deniega el acceso a los clientes nuevos.</span><span class="sxs-lookup"><span data-stu-id="a3c22-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="a3c22-171">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a3c22-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="a3c22-172">¿Necesita volver a configurar un servicio y hacer que los cambios surtan efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="a3c22-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="a3c22-173">Aunque se pueden cambiar las propiedades del servicio mientras se pausa un servicio, la mayoría de ellos no surtirán efecto hasta que el servicio se detenga y se reinicie realmente.</span><span class="sxs-lookup"><span data-stu-id="a3c22-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="a3c22-174">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="a3c22-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="a3c22-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3c22-175">Examples</span></span>

<span data-ttu-id="a3c22-176">En el ejemplo [pausar los servicios que se ejecutan en una cuenta específica](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) de VBScript se pausan todos los servicios que se ejecutan con la cuenta de servicio hipotética "netsvc".</span><span class="sxs-lookup"><span data-stu-id="a3c22-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="a3c22-177">En el ejemplo de código de VBScript siguiente se muestra cómo pausar un servicio específico a partir de instancias del [**\_ servicio de Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3c22-178">El servicio debe admitir la pausa y ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a3c22-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="a3c22-179">El siguiente ejemplo de código Perl muestra cómo pausar un servicio específico a partir de instancias del [**\_ servicio de Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3c22-180">El servicio debe admitir la pausa y ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a3c22-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="a3c22-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3c22-181">Requirements</span></span>



| <span data-ttu-id="a3c22-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c22-182">Requirement</span></span> | <span data-ttu-id="a3c22-183">Value</span><span class="sxs-lookup"><span data-stu-id="a3c22-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3c22-184">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c22-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3c22-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3c22-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3c22-186">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c22-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3c22-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3c22-188">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3c22-188">Namespace</span></span><br/>                | <span data-ttu-id="a3c22-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a3c22-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="a3c22-190">MOF</span><span class="sxs-lookup"><span data-stu-id="a3c22-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3c22-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3c22-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3c22-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3c22-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3c22-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3c22-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3c22-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3c22-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3c22-195">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3c22-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a3c22-196">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="a3c22-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="a3c22-197">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="a3c22-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="a3c22-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a3c22-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

