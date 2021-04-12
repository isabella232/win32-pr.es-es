---
description: La eliminación&\# 8194; El método de clase WMI elimina un servicio existente.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d06301c3620e144d72c2d4c4f3d8bc90e642374a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274984"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="3b5e5-103">Método Delete de la clase Win32_Service (proveedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3b5e5-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3b5e5-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="3b5e5-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3b5e5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b5e5-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3b5e5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5e5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b5e5-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="3b5e5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b5e5-108">Parameters</span></span>

<span data-ttu-id="3b5e5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b5e5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b5e5-110">Return value</span></span>

<span data-ttu-id="3b5e5-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="3b5e5-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3b5e5-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3b5e5-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3b5e5-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3b5e5-114">**0**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-116">**1**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-119">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-120">**3**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-121">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-122">**4**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-123">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-124">**5**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-125">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-126">**6**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-127">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-128">**7**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-129">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-130">**8**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-131">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-132">**9**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-133">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-134">**10**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-135">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-136">**11**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-137">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-138">**12**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-139">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-140">**13**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-141">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-142">**14**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-143">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-144">**15**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-145">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-146">**16**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-147">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-148">**17**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-149">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-150">**18**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-151">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-152">**19**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-153">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-154">**20**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-155">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-156">**21**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-157">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-158">**22**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-159">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-160">**23**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-161">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3b5e5-162">**24**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3b5e5-163">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b5e5-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b5e5-164">Remarks</span></span>

<span data-ttu-id="3b5e5-165">A medida que cambia la organización, puede decidir quitar determinados servicios de determinados equipos.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="3b5e5-166">Los servicios internos y de terceros se pueden quitar mediante WMI, mientras que los servicios del sistema operativo se pueden quitar mediante Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="3b5e5-167">Al preparar la eliminación de servicios, tenga en cuenta la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="3b5e5-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="3b5e5-168">Los servicios deben detenerse antes de quitarlos.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="3b5e5-169">Si el servicio se está ejecutando cuando se emite el comando DELETE, el servicio se marca para su eliminación, pero continúa ejecutándose hasta que se detiene y se cierran todos los identificadores abiertos.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="3b5e5-170">Si el servicio nunca se detiene, el servicio no se eliminará nunca.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="3b5e5-171">Al quitar un servicio no se quita el archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="3b5e5-172">Al quitar un servicio mediante WMI, se eliminan las entradas del registro relacionadas en HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="3b5e5-173">Como resultado, el servicio ya no está instalado y no está disponible a través del complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="3b5e5-174">Sin embargo, WMI no elimina el archivo ejecutable, lo que significa que puede volver a instalar el servicio fácilmente.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="3b5e5-175">Para eliminar el archivo ejecutable, debe recuperar el nombre de la ruta de acceso y, a continuación, eliminar el archivo.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="3b5e5-176">Al quitar un servicio base de Windows 2000 (por ejemplo, DHCP) mediante WMI, se eliminan las entradas del registro para ese servicio, pero no se quita el acceso directo del menú Herramientas administrativas ni se quita el servicio del Asistente para componentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="3b5e5-177">Esto puede confundir a cualquiera que intente determinar cómo se ha configurado el equipo.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="3b5e5-178">Por ejemplo, si quita el servicio DHCP mediante un script de WMI, el servicio DHCP ya no aparece en el complemento Servicios.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="3b5e5-179">Sin embargo, un acceso directo no funcional a la consola DHCP permanece en el menú Herramientas administrativas y, si inicia el Asistente para componentes de Windows, indica que el servicio DHCP está instalado.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="3b5e5-180">Por este motivo, siempre debe utilizar Sysocmgr.exe para quitar los servicios de Windows 2000 mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="3b5e5-181">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3b5e5-181">Examples</span></span>

<span data-ttu-id="3b5e5-182">En el siguiente ejemplo de código de VBScript se describe cómo eliminar un servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-182">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="3b5e5-183">En el siguiente ejemplo de código Perl se describe cómo eliminar un servicio.</span><span class="sxs-lookup"><span data-stu-id="3b5e5-183">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3b5e5-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b5e5-184">Requirements</span></span>



| <span data-ttu-id="3b5e5-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5e5-185">Requirement</span></span> | <span data-ttu-id="3b5e5-186">Value</span><span class="sxs-lookup"><span data-stu-id="3b5e5-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5e5-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5e5-187">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5e5-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b5e5-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b5e5-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5e5-189">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5e5-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b5e5-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b5e5-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b5e5-191">Namespace</span></span><br/>                | <span data-ttu-id="3b5e5-192">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b5e5-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b5e5-193">MOF</span><span class="sxs-lookup"><span data-stu-id="3b5e5-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b5e5-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e5-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b5e5-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b5e5-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b5e5-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b5e5-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b5e5-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b5e5-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b5e5-198">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b5e5-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3b5e5-199">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="3b5e5-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="3b5e5-200">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="3b5e5-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

