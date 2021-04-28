---
description: 'Método ResumeService de la clase Win32_Service (proveedores WMI CIMWin32): intenta colocar el servicio al que se hace referencia en el estado reanudado.'
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Método ResumeService de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73c21f282577207b63bcfa2d624c59ddfa3c9bcb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090983"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="f638f-103">Método ResumeService de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f638f-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f638f-104">El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** intenta colocar el servicio al que se hace referencia en el estado reanudado.</span><span class="sxs-lookup"><span data-stu-id="f638f-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="f638f-105">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="f638f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f638f-106">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f638f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f638f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f638f-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="f638f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f638f-108">Parameters</span></span>

<span data-ttu-id="f638f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f638f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f638f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f638f-110">Return value</span></span>

<span data-ttu-id="f638f-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="f638f-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="f638f-112">Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f638f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f638f-113">Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f638f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f638f-114">**0**</span><span class="sxs-lookup"><span data-stu-id="f638f-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f638f-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-116">**1**</span><span class="sxs-lookup"><span data-stu-id="f638f-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f638f-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="f638f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="f638f-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-120">**3**</span><span class="sxs-lookup"><span data-stu-id="f638f-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="f638f-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-122">**4**</span><span class="sxs-lookup"><span data-stu-id="f638f-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-124">**5**</span><span class="sxs-lookup"><span data-stu-id="f638f-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="f638f-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-126">**6**</span><span class="sxs-lookup"><span data-stu-id="f638f-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="f638f-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-128">**7**</span><span class="sxs-lookup"><span data-stu-id="f638f-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-130">**8**</span><span class="sxs-lookup"><span data-stu-id="f638f-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-132">**9**</span><span class="sxs-lookup"><span data-stu-id="f638f-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-133">No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-134">**10**</span><span class="sxs-lookup"><span data-stu-id="f638f-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f638f-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-136">**11**</span><span class="sxs-lookup"><span data-stu-id="f638f-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f638f-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-138">**12**</span><span class="sxs-lookup"><span data-stu-id="f638f-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-139">Se ha quitado del sistema una dependencia en la que se basa este servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-140">**13**</span><span class="sxs-lookup"><span data-stu-id="f638f-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="f638f-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-142">**14**</span><span class="sxs-lookup"><span data-stu-id="f638f-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="f638f-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-144">**15**</span><span class="sxs-lookup"><span data-stu-id="f638f-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f638f-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-146">**16**</span><span class="sxs-lookup"><span data-stu-id="f638f-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="f638f-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-148">**17**</span><span class="sxs-lookup"><span data-stu-id="f638f-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f638f-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-150">**18**</span><span class="sxs-lookup"><span data-stu-id="f638f-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-151">El servicio tiene dependencias circulares cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="f638f-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-152">**19**</span><span class="sxs-lookup"><span data-stu-id="f638f-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-153">Un servicio se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="f638f-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-154">**20**</span><span class="sxs-lookup"><span data-stu-id="f638f-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="f638f-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-156">**21**</span><span class="sxs-lookup"><span data-stu-id="f638f-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-158">**22**</span><span class="sxs-lookup"><span data-stu-id="f638f-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-159">La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-160">**23**</span><span class="sxs-lookup"><span data-stu-id="f638f-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="f638f-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f638f-162">**24**</span><span class="sxs-lookup"><span data-stu-id="f638f-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f638f-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f638f-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f638f-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f638f-164">Remarks</span></span>

<span data-ttu-id="f638f-165">Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio que se detiene y un servicio que está en pausa, los dos estados aparecen de forma diferente al SCM.</span><span class="sxs-lookup"><span data-stu-id="f638f-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="f638f-166">Un servicio detenido es un servicio que no se está ejecutando y debe pasar por todo el procedimiento de inicio del servicio.</span><span class="sxs-lookup"><span data-stu-id="f638f-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="f638f-167">Sin embargo, un servicio en pausa todavía se está ejecutando, pero se ha suspendido su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="f638f-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="f638f-168">Por este problema, un servicio en pausa no necesita pasar por todo el procedimiento de inicio del servicio, sino que necesita un procedimiento diferente para reanudar el funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="f638f-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="f638f-169">Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado.</span><span class="sxs-lookup"><span data-stu-id="f638f-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="f638f-170">Los [**métodos \_ del servicio Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) y **ResumeService** deben usarse en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="f638f-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="f638f-171">Si un servicio está detenido actualmente, debe usar el [**método StartService**](startservice-method-in-class-win32-service.md) para reiniciarlo. **ResumeService** no puede iniciar un servicio que está detenido actualmente.</span><span class="sxs-lookup"><span data-stu-id="f638f-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="f638f-172">Si un servicio está en pausa, debe usar **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="f638f-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="f638f-173">Si usa el [**método StartService**](startservice-method-in-class-win32-service.md) en un servicio en pausa, recibirá el mensaje "El servicio ya se está ejecutando".</span><span class="sxs-lookup"><span data-stu-id="f638f-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="f638f-174">Sin embargo, el servicio permanece en pausa hasta que se le envía el código de control de servicio de reanudación.</span><span class="sxs-lookup"><span data-stu-id="f638f-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="f638f-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f638f-175">Examples</span></span>

<span data-ttu-id="f638f-176">En [el ejemplo Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript (Reanudar servicios de inicio automático que son VBScript en pausa) se reinician los servicios de inicio automático que se han pausado.</span><span class="sxs-lookup"><span data-stu-id="f638f-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="f638f-177">En el siguiente ejemplo de código de VBScript se describe cómo reanudar un servicio en pausa desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="f638f-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="f638f-178">El servicio debe admitir pausas y estar ejecutándose ya.</span><span class="sxs-lookup"><span data-stu-id="f638f-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="f638f-179">En el ejemplo de código perl siguiente se describe cómo reanudar un servicio en pausa desde instancias del [**servicio Win32 \_**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="f638f-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="f638f-180">El servicio debe admitir pausas y estar ejecutándose ya.</span><span class="sxs-lookup"><span data-stu-id="f638f-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="f638f-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f638f-181">Requirements</span></span>



| <span data-ttu-id="f638f-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="f638f-182">Requirement</span></span> | <span data-ttu-id="f638f-183">Valor</span><span class="sxs-lookup"><span data-stu-id="f638f-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f638f-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f638f-184">Minimum supported client</span></span><br/> | <span data-ttu-id="f638f-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f638f-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f638f-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f638f-186">Minimum supported server</span></span><br/> | <span data-ttu-id="f638f-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f638f-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f638f-188">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f638f-188">Namespace</span></span><br/>                | <span data-ttu-id="f638f-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f638f-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="f638f-190">MOF</span><span class="sxs-lookup"><span data-stu-id="f638f-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f638f-191"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f638f-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f638f-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f638f-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f638f-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f638f-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f638f-194">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f638f-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="f638f-195">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f638f-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f638f-196">**Servicio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="f638f-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="f638f-197">Tareas wmi: servicios</span><span class="sxs-lookup"><span data-stu-id="f638f-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

