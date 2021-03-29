---
title: Método Delete de la clase Win32_Service (Servicios de Escritorio remoto)
description: La eliminación \ 8194; El método de clase WMI elimina un servicio existente.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto, clase Win32_Service
- Clase Win32_Service Servicios de Escritorio remoto, método Delete
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535308"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="3fb26-106">Método Delete de la clase Win32_Service (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="3fb26-106">Delete method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="3fb26-107">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="3fb26-107">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="3fb26-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3fb26-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3fb26-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3fb26-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb26-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb26-110">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="3fb26-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fb26-111">Parameters</span></span>

<span data-ttu-id="3fb26-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3fb26-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fb26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fb26-113">Return value</span></span>

<span data-ttu-id="3fb26-114">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3fb26-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="3fb26-115">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3fb26-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3fb26-116">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3fb26-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3fb26-117">**0**</span><span class="sxs-lookup"><span data-stu-id="3fb26-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-118">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fb26-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-119">**1**</span><span class="sxs-lookup"><span data-stu-id="3fb26-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-120">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fb26-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3fb26-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="3fb26-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-123">**3**</span><span class="sxs-lookup"><span data-stu-id="3fb26-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-124">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="3fb26-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-125">**4**</span><span class="sxs-lookup"><span data-stu-id="3fb26-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-127">**5**</span><span class="sxs-lookup"><span data-stu-id="3fb26-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-128">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="3fb26-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-129">**6**</span><span class="sxs-lookup"><span data-stu-id="3fb26-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-130">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="3fb26-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-131">**7**</span><span class="sxs-lookup"><span data-stu-id="3fb26-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-132">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-133">**8**</span><span class="sxs-lookup"><span data-stu-id="3fb26-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-134">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-135">**9**</span><span class="sxs-lookup"><span data-stu-id="3fb26-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-136">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-137">**10**</span><span class="sxs-lookup"><span data-stu-id="3fb26-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3fb26-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-139">**11**</span><span class="sxs-lookup"><span data-stu-id="3fb26-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3fb26-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-141">**12**</span><span class="sxs-lookup"><span data-stu-id="3fb26-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-142">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-143">**13**</span><span class="sxs-lookup"><span data-stu-id="3fb26-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="3fb26-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-145">**14**</span><span class="sxs-lookup"><span data-stu-id="3fb26-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-147">**15**</span><span class="sxs-lookup"><span data-stu-id="3fb26-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-149">**16**</span><span class="sxs-lookup"><span data-stu-id="3fb26-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-151">**17**</span><span class="sxs-lookup"><span data-stu-id="3fb26-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3fb26-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-153">**18**</span><span class="sxs-lookup"><span data-stu-id="3fb26-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-154">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="3fb26-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-155">**19**</span><span class="sxs-lookup"><span data-stu-id="3fb26-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-156">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="3fb26-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-157">**20**</span><span class="sxs-lookup"><span data-stu-id="3fb26-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="3fb26-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-159">**21**</span><span class="sxs-lookup"><span data-stu-id="3fb26-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-160">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-161">**22**</span><span class="sxs-lookup"><span data-stu-id="3fb26-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-162">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-163">**23**</span><span class="sxs-lookup"><span data-stu-id="3fb26-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-164">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3fb26-165">**24**</span><span class="sxs-lookup"><span data-stu-id="3fb26-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3fb26-166">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3fb26-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fb26-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fb26-167">Remarks</span></span>

<span data-ttu-id="3fb26-168">A medida que cambia la organización, puede decidir quitar determinados servicios de determinados equipos.</span><span class="sxs-lookup"><span data-stu-id="3fb26-168">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="3fb26-169">Los servicios internos y de terceros se pueden quitar mediante WMI, mientras que los servicios del sistema operativo se pueden quitar mediante Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="3fb26-169">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="3fb26-170">Al preparar la eliminación de servicios, tenga en cuenta la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="3fb26-170">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="3fb26-171">Los servicios deben detenerse antes de quitarlos.</span><span class="sxs-lookup"><span data-stu-id="3fb26-171">Services must be stopped before you remove them.</span></span> <span data-ttu-id="3fb26-172">Si el servicio se está ejecutando cuando se emite el comando DELETE, el servicio se marca para su eliminación, pero continúa ejecutándose hasta que se detiene y se cierran todos los identificadores abiertos.</span><span class="sxs-lookup"><span data-stu-id="3fb26-172">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="3fb26-173">Si el servicio nunca se detiene, el servicio no se eliminará nunca.</span><span class="sxs-lookup"><span data-stu-id="3fb26-173">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="3fb26-174">Al quitar un servicio no se quita el archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-174">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="3fb26-175">Al quitar un servicio mediante WMI, se eliminan las entradas del registro relacionadas en HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="3fb26-175">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="3fb26-176">Como resultado, el servicio ya no está instalado y no está disponible a través del complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="3fb26-176">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="3fb26-177">Sin embargo, WMI no elimina el archivo ejecutable, lo que significa que puede volver a instalar el servicio fácilmente.</span><span class="sxs-lookup"><span data-stu-id="3fb26-177">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="3fb26-178">Para eliminar el archivo ejecutable, debe recuperar el nombre de la ruta de acceso y, a continuación, eliminar el archivo.</span><span class="sxs-lookup"><span data-stu-id="3fb26-178">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="3fb26-179">Al quitar un servicio base de Windows 2000 (por ejemplo, DHCP) mediante WMI, se eliminan las entradas del registro para ese servicio, pero no se quita el acceso directo del menú Herramientas administrativas ni se quita el servicio del Asistente para componentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="3fb26-179">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="3fb26-180">Esto puede confundir a cualquiera que intente determinar cómo se ha configurado el equipo.</span><span class="sxs-lookup"><span data-stu-id="3fb26-180">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="3fb26-181">Por ejemplo, si quita el servicio DHCP mediante un script de WMI, el servicio DHCP ya no aparece en el complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="3fb26-181">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="3fb26-182">Sin embargo, un acceso directo no funcional a la consola DHCP permanece en el menú Herramientas administrativas y, si inicia el Asistente para componentes de Windows, indica que el servicio DHCP está instalado.</span><span class="sxs-lookup"><span data-stu-id="3fb26-182">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="3fb26-183">Por este motivo, siempre debe utilizar Sysocmgr.exe para quitar los servicios de Windows 2000 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3fb26-183">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="3fb26-184">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3fb26-184">Examples</span></span>

<span data-ttu-id="3fb26-185">En el siguiente ejemplo de código de VBScript se describe cómo eliminar un servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-185">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="3fb26-186">En el siguiente ejemplo de código Perl se describe cómo eliminar un servicio.</span><span class="sxs-lookup"><span data-stu-id="3fb26-186">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3fb26-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb26-187">Requirements</span></span>



| <span data-ttu-id="3fb26-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb26-188">Requirement</span></span> | <span data-ttu-id="3fb26-189">Value</span><span class="sxs-lookup"><span data-stu-id="3fb26-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb26-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb26-190">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb26-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fb26-191">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fb26-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb26-192">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb26-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fb26-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fb26-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fb26-194">Namespace</span></span><br/>                | <span data-ttu-id="3fb26-195">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3fb26-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3fb26-196">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb26-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb26-197"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fb26-197"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb26-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fb26-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb26-199"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb26-199"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb26-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fb26-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb26-201">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="3fb26-201">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="3fb26-202">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3fb26-202">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="3fb26-203">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="3fb26-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="3fb26-204">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="3fb26-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

