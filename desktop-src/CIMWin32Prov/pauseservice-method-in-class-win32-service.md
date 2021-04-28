---
description: 'Método PauseService de la clase Win32_Service (proveedores WMI CIMWin32): intenta colocar el servicio en estado en pausa.'
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Método PauseService de la clase Win32_Service (proveedores WMI CIMWin32)
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
ms.openlocfilehash: 7654feea410564137e98861c4c0b5de2b5e7192e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096953"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="0a9a4-103">Método PauseService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0a9a4-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0a9a4-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta colocar el servicio en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="0a9a4-105">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="0a9a4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0a9a4-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0a9a4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a9a4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a9a4-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="0a9a4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a9a4-108">Parameters</span></span>

<span data-ttu-id="0a9a4-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a9a4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a9a4-110">Return value</span></span>

<span data-ttu-id="0a9a4-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="0a9a4-112">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0a9a4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0a9a4-113">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0a9a4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0a9a4-114">**0**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-116">**1**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-118">**2**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-120">**3**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-122">**4**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-124">**5**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-126">**6**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-128">**7**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-130">**8**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-132">**9**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-133">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-134">**10**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-136">**11**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-138">**12**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-139">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-140">**13**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-142">**14**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-144">**15**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-146">**16**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-148">**17**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-150">**18**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-151">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-152">**19**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-153">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-154">**20**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-156">**21**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-158">**22**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-159">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-160">**23**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0a9a4-162">**24**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0a9a4-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a9a4-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a9a4-164">Remarks</span></span>

<span data-ttu-id="0a9a4-165">Después de determinar qué servicios se pueden detener o pausar, puede usar los métodos [**StopService**](stopservice-method-in-class-win32-service.md) y [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="0a9a4-166">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, incluidos los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a9a4-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="0a9a4-167">¿El servicio es capaz de pausar?</span><span class="sxs-lookup"><span data-stu-id="0a9a4-167">Is the service capable of being paused?</span></span> <span data-ttu-id="0a9a4-168">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="0a9a4-169">¿Necesita seguir controlando las solicitudes de cliente de cualquier persona que ya esté conectada al servicio?</span><span class="sxs-lookup"><span data-stu-id="0a9a4-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="0a9a4-170">Si es así, pausar un servicio normalmente le permite controlar los clientes existentes mientras se deniega el acceso a los nuevos clientes.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="0a9a4-171">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="0a9a4-172">¿Necesita volver a configurar un servicio y hacer que los cambios sumen efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="0a9a4-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="0a9a4-173">Aunque las propiedades del servicio se pueden cambiar mientras un servicio está en pausa, la mayoría de ellas no tienen efecto hasta que el servicio se detiene y reinicia realmente.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="0a9a4-174">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="0a9a4-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0a9a4-175">Examples</span></span>

<span data-ttu-id="0a9a4-176">El [ejemplo de VBScript Pausar](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) servicios que se ejecutan en una cuenta específica pausa todos los servicios que se ejecutan en la hipotética cuenta de servicio "Netsvc".</span><span class="sxs-lookup"><span data-stu-id="0a9a4-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="0a9a4-177">En el siguiente ejemplo de código de VBScript se muestra cómo pausar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="0a9a4-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a9a4-178">El servicio debe admitir pausas y estar ejecutándose ya.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-178">The service must support pausing and be running already.</span></span>

 


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



<span data-ttu-id="0a9a4-179">En el ejemplo de código perl siguiente se muestra cómo pausar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="0a9a4-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a9a4-180">El servicio debe admitir pausas y estar ejecutándose ya.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-180">The service must support pausing and be running already.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="0a9a4-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a9a4-181">Requirements</span></span>



| <span data-ttu-id="0a9a4-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a9a4-182">Requirement</span></span> | <span data-ttu-id="0a9a4-183">Valor</span><span class="sxs-lookup"><span data-stu-id="0a9a4-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9a4-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9a4-184">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9a4-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a9a4-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a9a4-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a9a4-186">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9a4-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a9a4-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a9a4-188">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a9a4-188">Namespace</span></span><br/>                | <span data-ttu-id="0a9a4-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="0a9a4-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="0a9a4-190">MOF</span><span class="sxs-lookup"><span data-stu-id="0a9a4-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a9a4-191"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a4-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a9a4-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a9a4-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a9a4-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a4-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9a4-194">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a9a4-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a9a4-195">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a9a4-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0a9a4-196">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="0a9a4-197">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="0a9a4-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="0a9a4-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0a9a4-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

