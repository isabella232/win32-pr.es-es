---
description: 'Método StartService de la clase Win32_Service (proveedores WMI CIMWin32): intenta colocar el servicio al que se hace referencia en su estado de inicio.'
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Método StartService de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086163"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="7beaa-103">Método StartService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7beaa-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7beaa-104">El **método StartService** intenta colocar el servicio al que se hace referencia en su estado de inicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="7beaa-105">En este tema se usa Managed Object Format sintaxis de MOF.</span><span class="sxs-lookup"><span data-stu-id="7beaa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7beaa-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7beaa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7beaa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7beaa-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="7beaa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7beaa-108">Parameters</span></span>

<span data-ttu-id="7beaa-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7beaa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7beaa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7beaa-110">Return value</span></span>

<span data-ttu-id="7beaa-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="7beaa-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="7beaa-112">Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7beaa-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7beaa-113">Para obtener los **valores HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7beaa-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7beaa-114">**0**</span><span class="sxs-lookup"><span data-stu-id="7beaa-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7beaa-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-116">**1**</span><span class="sxs-lookup"><span data-stu-id="7beaa-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7beaa-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-118">**2**</span><span class="sxs-lookup"><span data-stu-id="7beaa-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="7beaa-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-120">**3**</span><span class="sxs-lookup"><span data-stu-id="7beaa-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="7beaa-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-122">**4**</span><span class="sxs-lookup"><span data-stu-id="7beaa-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-124">**5**</span><span class="sxs-lookup"><span data-stu-id="7beaa-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**Propiedad** State) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="7beaa-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-126">**6**</span><span class="sxs-lookup"><span data-stu-id="7beaa-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="7beaa-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-128">**7**</span><span class="sxs-lookup"><span data-stu-id="7beaa-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-130">**8**</span><span class="sxs-lookup"><span data-stu-id="7beaa-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-132">**9**</span><span class="sxs-lookup"><span data-stu-id="7beaa-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-133">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-134">**10**</span><span class="sxs-lookup"><span data-stu-id="7beaa-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="7beaa-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-136">**11**</span><span class="sxs-lookup"><span data-stu-id="7beaa-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7beaa-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-138">**12**</span><span class="sxs-lookup"><span data-stu-id="7beaa-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-139">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-140">**13**</span><span class="sxs-lookup"><span data-stu-id="7beaa-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="7beaa-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-142">**14**</span><span class="sxs-lookup"><span data-stu-id="7beaa-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="7beaa-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-144">**15**</span><span class="sxs-lookup"><span data-stu-id="7beaa-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7beaa-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-146">**16**</span><span class="sxs-lookup"><span data-stu-id="7beaa-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="7beaa-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-148">**17**</span><span class="sxs-lookup"><span data-stu-id="7beaa-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7beaa-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-150">**18**</span><span class="sxs-lookup"><span data-stu-id="7beaa-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-151">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="7beaa-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-152">**19**</span><span class="sxs-lookup"><span data-stu-id="7beaa-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-153">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="7beaa-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-154">**20**</span><span class="sxs-lookup"><span data-stu-id="7beaa-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="7beaa-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-156">**21**</span><span class="sxs-lookup"><span data-stu-id="7beaa-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-158">**22**</span><span class="sxs-lookup"><span data-stu-id="7beaa-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-159">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-160">**23**</span><span class="sxs-lookup"><span data-stu-id="7beaa-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="7beaa-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7beaa-162">**24**</span><span class="sxs-lookup"><span data-stu-id="7beaa-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="7beaa-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7beaa-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7beaa-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7beaa-164">Remarks</span></span>

<span data-ttu-id="7beaa-165">Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio que se detiene y un servicio que está en pausa, los dos estados aparecen de forma diferente al SCM.</span><span class="sxs-lookup"><span data-stu-id="7beaa-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="7beaa-166">Un servicio detenido es un servicio que no se está ejecutando y debe pasar por todo el procedimiento de inicio del servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="7beaa-167">Sin embargo, un servicio en pausa todavía se está ejecutando, pero se ha suspendido su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="7beaa-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="7beaa-168">Por este problema, un servicio en pausa no necesita pasar por todo el procedimiento de inicio del servicio, pero necesita un procedimiento diferente para reanudar el funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="7beaa-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="7beaa-169">Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado.</span><span class="sxs-lookup"><span data-stu-id="7beaa-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="7beaa-170">Los [**métodos de \_ servicio Win32**](win32-service.md) **StartService** y [**ResumeService**](resumeservice-method-in-class-win32-service.md) deben usarse en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7beaa-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="7beaa-171">Si un servicio está detenido actualmente, debe usar el **método StartService** para reiniciarlo. [**ResumeService**](resumeservice-method-in-class-win32-service.md) no puede iniciar un servicio que esté detenido actualmente.</span><span class="sxs-lookup"><span data-stu-id="7beaa-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="7beaa-172">Si un servicio está en pausa, debe usar [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7beaa-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="7beaa-173">Si usa el **método StartService** en un servicio en pausa, recibirá el mensaje "El servicio ya se está ejecutando".</span><span class="sxs-lookup"><span data-stu-id="7beaa-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="7beaa-174">Sin embargo, el servicio permanece en pausa hasta que se le envía el código de control de servicio de reanudación.</span><span class="sxs-lookup"><span data-stu-id="7beaa-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="7beaa-175">Si inicia un servicio detenido que depende de otro servicio, se inician ambos servicios.</span><span class="sxs-lookup"><span data-stu-id="7beaa-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="7beaa-176">Cuando se inicia un servicio con este método, los servicios dependientes no se inician automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7beaa-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="7beaa-177">Debe usar la clase de asociación [**Win32 \_ DependentService**](win32-dependentservice.md) y la consulta [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) para buscar los dependientes e iniciarlos por separado.</span><span class="sxs-lookup"><span data-stu-id="7beaa-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="7beaa-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7beaa-178">Examples</span></span>

<span data-ttu-id="7beaa-179">El [ejemplo de PowerShell Habilitar RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) de forma remota habilita el Escritorio remoto remoto.</span><span class="sxs-lookup"><span data-stu-id="7beaa-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="7beaa-180">El ejemplo de PowerShell [Detener, Iniciar, Habilitar](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) o Deshabilitar servicio inicia, detiene, habilita o deshabilita un servicio.</span><span class="sxs-lookup"><span data-stu-id="7beaa-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="7beaa-181">En el siguiente ejemplo de código de VBSScript se muestra cómo iniciar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7beaa-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="7beaa-182">En el ejemplo de código perl siguiente se muestra cómo iniciar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7beaa-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="7beaa-183">El siguiente ejemplo de código VBScript, NetDDE, depende del servicio NetDDEDSDM.</span><span class="sxs-lookup"><span data-stu-id="7beaa-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="7beaa-184">El script busca la clase de la que depende NetDDE y la inicia, lo que no inicia automáticamente NetDDE.</span><span class="sxs-lookup"><span data-stu-id="7beaa-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="7beaa-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7beaa-185">Requirements</span></span>



| <span data-ttu-id="7beaa-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="7beaa-186">Requirement</span></span> | <span data-ttu-id="7beaa-187">Valor</span><span class="sxs-lookup"><span data-stu-id="7beaa-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7beaa-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7beaa-188">Minimum supported client</span></span><br/> | <span data-ttu-id="7beaa-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7beaa-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7beaa-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7beaa-190">Minimum supported server</span></span><br/> | <span data-ttu-id="7beaa-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7beaa-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7beaa-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7beaa-192">Namespace</span></span><br/>                | <span data-ttu-id="7beaa-193">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="7beaa-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7beaa-194">MOF</span><span class="sxs-lookup"><span data-stu-id="7beaa-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7beaa-195"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7beaa-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7beaa-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7beaa-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7beaa-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7beaa-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7beaa-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7beaa-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="7beaa-199">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7beaa-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7beaa-200">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="7beaa-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="7beaa-201">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="7beaa-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

