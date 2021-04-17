---
description: Coloca el servicio, representado por el \_ objeto de servicio de Win32, en estado detenido.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Método StopService de la clase Win32_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659564"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="dcffc-103">Método StopService de la clase Win32_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="dcffc-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="dcffc-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio, representado por el objeto de [**\_ servicio de Win32**](win32-service.md) , en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="dcffc-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="dcffc-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dcffc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dcffc-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dcffc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dcffc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcffc-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="dcffc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcffc-108">Parameters</span></span>

<span data-ttu-id="dcffc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dcffc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcffc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcffc-110">Return value</span></span>

<span data-ttu-id="dcffc-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="dcffc-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="dcffc-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dcffc-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dcffc-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dcffc-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dcffc-114">**0**</span><span class="sxs-lookup"><span data-stu-id="dcffc-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dcffc-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-116">**1**</span><span class="sxs-lookup"><span data-stu-id="dcffc-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dcffc-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-118">**2**</span><span class="sxs-lookup"><span data-stu-id="dcffc-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="dcffc-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-120">**3**</span><span class="sxs-lookup"><span data-stu-id="dcffc-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="dcffc-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-122">**4**</span><span class="sxs-lookup"><span data-stu-id="dcffc-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-124">**5**</span><span class="sxs-lookup"><span data-stu-id="dcffc-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="dcffc-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-126">**6**</span><span class="sxs-lookup"><span data-stu-id="dcffc-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="dcffc-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-128">**7**</span><span class="sxs-lookup"><span data-stu-id="dcffc-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-130">**8**</span><span class="sxs-lookup"><span data-stu-id="dcffc-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-132">**9**</span><span class="sxs-lookup"><span data-stu-id="dcffc-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-133">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-134">**10**</span><span class="sxs-lookup"><span data-stu-id="dcffc-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="dcffc-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-136">**11**</span><span class="sxs-lookup"><span data-stu-id="dcffc-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="dcffc-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-138">**12**</span><span class="sxs-lookup"><span data-stu-id="dcffc-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-139">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-140">**13**</span><span class="sxs-lookup"><span data-stu-id="dcffc-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="dcffc-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-142">**14**</span><span class="sxs-lookup"><span data-stu-id="dcffc-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-144">**15**</span><span class="sxs-lookup"><span data-stu-id="dcffc-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-146">**16**</span><span class="sxs-lookup"><span data-stu-id="dcffc-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-148">**17**</span><span class="sxs-lookup"><span data-stu-id="dcffc-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="dcffc-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-150">**18**</span><span class="sxs-lookup"><span data-stu-id="dcffc-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-151">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="dcffc-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-152">**19**</span><span class="sxs-lookup"><span data-stu-id="dcffc-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-153">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="dcffc-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-154">**20**</span><span class="sxs-lookup"><span data-stu-id="dcffc-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="dcffc-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-156">**21**</span><span class="sxs-lookup"><span data-stu-id="dcffc-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-158">**22**</span><span class="sxs-lookup"><span data-stu-id="dcffc-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-159">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-160">**23**</span><span class="sxs-lookup"><span data-stu-id="dcffc-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dcffc-162">**24**</span><span class="sxs-lookup"><span data-stu-id="dcffc-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="dcffc-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dcffc-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcffc-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcffc-164">Remarks</span></span>

<span data-ttu-id="dcffc-165">Después de determinar qué servicios se pueden detener o pausar, puede utilizar los métodos **StopService** y [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para detener y pausar los servicios.</span><span class="sxs-lookup"><span data-stu-id="dcffc-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="dcffc-166">La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dcffc-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="dcffc-167">¿Se puede pausar el servicio?</span><span class="sxs-lookup"><span data-stu-id="dcffc-167">Is the service capable of being paused?</span></span> <span data-ttu-id="dcffc-168">Si no es así, la única opción es detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="dcffc-169">¿Necesita seguir controlando las solicitudes de cliente para los usuarios que ya están conectados al servicio?</span><span class="sxs-lookup"><span data-stu-id="dcffc-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="dcffc-170">Si es así, al pausar un servicio normalmente se le permite administrar los clientes existentes a la vez que deniega el acceso a los clientes nuevos.</span><span class="sxs-lookup"><span data-stu-id="dcffc-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="dcffc-171">Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="dcffc-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="dcffc-172">¿Necesita volver a configurar un servicio y hacer que los cambios surtan efecto inmediatamente?</span><span class="sxs-lookup"><span data-stu-id="dcffc-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="dcffc-173">Aunque se pueden cambiar las propiedades del servicio mientras se pausa un servicio, la mayoría de ellos no surtirán efecto hasta que el servicio se detenga y se reinicie realmente.</span><span class="sxs-lookup"><span data-stu-id="dcffc-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="dcffc-174">El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="dcffc-175">Si intenta detener un servicio que tiene servicios dependientes en ejecución, se produce un error en el método **StopService** con un valor devuelto de 3.</span><span class="sxs-lookup"><span data-stu-id="dcffc-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="dcffc-176">Los servicios dependientes deben detenerse en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="dcffc-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="dcffc-177">Si detiene un servicio, compruebe inmediatamente el [**\_ servicio Win32**](win32-service.md).**Propiedad State** , ya que el valor puede seguir mostrando el servicio como en ejecución.</span><span class="sxs-lookup"><span data-stu-id="dcffc-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="dcffc-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dcffc-178">Examples</span></span>

<span data-ttu-id="dcffc-179">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) El ejemplo de PowerShell establece el estado del servicio para los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="dcffc-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="dcffc-180">En el ejemplo de VBScript [detener un servicio y su dependientes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) se detiene un servicio y todos los servicios dependientes.</span><span class="sxs-lookup"><span data-stu-id="dcffc-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="dcffc-181">El siguiente ejemplo de código de VBScript muestra cómo cerrar un servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="dcffc-182">El siguiente ejemplo de código Perl muestra cómo apagar un servicio.</span><span class="sxs-lookup"><span data-stu-id="dcffc-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="dcffc-183">En el ejemplo de código de VBScript siguiente se muestra que no se puede detener el servicio NetDDE hasta que los servicios dependientes se hayan detenido.</span><span class="sxs-lookup"><span data-stu-id="dcffc-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="dcffc-184">Para ejecutar el script, asegúrese de que el servicio NetDDE y sus servicios dependientes se están ejecutando con el complemento de MMC Services. msc o el comando **net start** .</span><span class="sxs-lookup"><span data-stu-id="dcffc-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="dcffc-185">La [**clase \_ DependentService de Win32**](win32-dependentservice.md) permite buscar dependencias de servicio a través [de una consulta ASSOCIATORS of](/windows/desktop/WmiSdk/associators-of-statement) .</span><span class="sxs-lookup"><span data-stu-id="dcffc-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="dcffc-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcffc-186">Requirements</span></span>



| <span data-ttu-id="dcffc-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcffc-187">Requirement</span></span> | <span data-ttu-id="dcffc-188">Value</span><span class="sxs-lookup"><span data-stu-id="dcffc-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcffc-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcffc-189">Minimum supported client</span></span><br/> | <span data-ttu-id="dcffc-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcffc-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dcffc-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcffc-191">Minimum supported server</span></span><br/> | <span data-ttu-id="dcffc-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcffc-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dcffc-193">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dcffc-193">Namespace</span></span><br/>                | <span data-ttu-id="dcffc-194">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dcffc-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dcffc-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcffc-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcffc-196"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcffc-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="dcffc-197">MOF</span><span class="sxs-lookup"><span data-stu-id="dcffc-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcffc-198"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcffc-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcffc-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcffc-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcffc-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcffc-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcffc-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcffc-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="dcffc-202">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dcffc-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dcffc-203">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="dcffc-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="dcffc-204">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="dcffc-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="dcffc-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="dcffc-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

