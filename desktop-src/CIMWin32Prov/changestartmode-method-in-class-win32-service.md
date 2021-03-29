---
description: Modifica el modo de inicio de un \_ servicio Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Método ChangeStartMode de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080181"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="cbd37-103">Método ChangeStartMode de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cbd37-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cbd37-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de [**un \_ servicio de Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="cbd37-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="cbd37-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cbd37-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cbd37-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cbd37-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbd37-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="cbd37-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbd37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd37-109">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cbd37-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-110">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbd37-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="cbd37-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="cbd37-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="cbd37-112">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbd37-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="cbd37-113">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="cbd37-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="cbd37-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="cbd37-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="cbd37-115">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbd37-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="cbd37-116">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="cbd37-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="cbd37-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="cbd37-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="cbd37-118">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="cbd37-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")</span><span class="sxs-lookup"><span data-stu-id="cbd37-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="cbd37-120">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd37-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cbd37-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="cbd37-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="cbd37-122">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="cbd37-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd37-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbd37-123">Return value</span></span>

<span data-ttu-id="cbd37-124">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="cbd37-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="cbd37-125">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cbd37-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cbd37-126">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cbd37-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cbd37-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="cbd37-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-128">0</span><span class="sxs-lookup"><span data-stu-id="cbd37-128">0</span></span>

<span data-ttu-id="cbd37-129">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbd37-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-130">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="cbd37-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-131">1</span><span class="sxs-lookup"><span data-stu-id="cbd37-131">1</span></span>

<span data-ttu-id="cbd37-132">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbd37-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-133">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="cbd37-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-134">2</span><span class="sxs-lookup"><span data-stu-id="cbd37-134">2</span></span>

<span data-ttu-id="cbd37-135">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="cbd37-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-136">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="cbd37-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-137">3</span><span class="sxs-lookup"><span data-stu-id="cbd37-137">3</span></span>

<span data-ttu-id="cbd37-138">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="cbd37-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-139">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="cbd37-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-140">4</span><span class="sxs-lookup"><span data-stu-id="cbd37-140">4</span></span>

<span data-ttu-id="cbd37-141">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-142">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="cbd37-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-143">5</span><span class="sxs-lookup"><span data-stu-id="cbd37-143">5</span></span>

<span data-ttu-id="cbd37-144">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="cbd37-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-145">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="cbd37-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-146">6</span><span class="sxs-lookup"><span data-stu-id="cbd37-146">6</span></span>

<span data-ttu-id="cbd37-147">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="cbd37-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-148">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="cbd37-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-149">7</span><span class="sxs-lookup"><span data-stu-id="cbd37-149">7</span></span>

<span data-ttu-id="cbd37-150">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-151">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="cbd37-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-152">8</span><span class="sxs-lookup"><span data-stu-id="cbd37-152">8</span></span>

<span data-ttu-id="cbd37-153">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-154">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="cbd37-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-155">9</span><span class="sxs-lookup"><span data-stu-id="cbd37-155">9</span></span>

<span data-ttu-id="cbd37-156">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-157">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="cbd37-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-158">10</span><span class="sxs-lookup"><span data-stu-id="cbd37-158">10</span></span>

<span data-ttu-id="cbd37-159">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="cbd37-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-160">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="cbd37-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-161">11</span><span class="sxs-lookup"><span data-stu-id="cbd37-161">11</span></span>

<span data-ttu-id="cbd37-162">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cbd37-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-163">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="cbd37-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-164">12</span><span class="sxs-lookup"><span data-stu-id="cbd37-164">12</span></span>

<span data-ttu-id="cbd37-165">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-166">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="cbd37-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-167">13</span><span class="sxs-lookup"><span data-stu-id="cbd37-167">13</span></span>

<span data-ttu-id="cbd37-168">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="cbd37-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-169">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="cbd37-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-170">14</span><span class="sxs-lookup"><span data-stu-id="cbd37-170">14</span></span>

<span data-ttu-id="cbd37-171">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-172">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="cbd37-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-173">15</span><span class="sxs-lookup"><span data-stu-id="cbd37-173">15</span></span>

<span data-ttu-id="cbd37-174">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-175">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="cbd37-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-176">16</span><span class="sxs-lookup"><span data-stu-id="cbd37-176">16</span></span>

<span data-ttu-id="cbd37-177">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-178">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="cbd37-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-179">17</span><span class="sxs-lookup"><span data-stu-id="cbd37-179">17</span></span>

<span data-ttu-id="cbd37-180">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbd37-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-181">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="cbd37-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-182">18</span><span class="sxs-lookup"><span data-stu-id="cbd37-182">18</span></span>

<span data-ttu-id="cbd37-183">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="cbd37-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-184">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="cbd37-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-185">19</span><span class="sxs-lookup"><span data-stu-id="cbd37-185">19</span></span>

<span data-ttu-id="cbd37-186">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="cbd37-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-187">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="cbd37-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-188">20</span><span class="sxs-lookup"><span data-stu-id="cbd37-188">20</span></span>

<span data-ttu-id="cbd37-189">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="cbd37-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-190">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="cbd37-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-191">21</span><span class="sxs-lookup"><span data-stu-id="cbd37-191">21</span></span>

<span data-ttu-id="cbd37-192">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-193">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="cbd37-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-194">22</span><span class="sxs-lookup"><span data-stu-id="cbd37-194">22</span></span>

<span data-ttu-id="cbd37-195">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-196">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="cbd37-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-197">23</span><span class="sxs-lookup"><span data-stu-id="cbd37-197">23</span></span>

<span data-ttu-id="cbd37-198">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-199">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="cbd37-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-200">24</span><span class="sxs-lookup"><span data-stu-id="cbd37-200">24</span></span>

<span data-ttu-id="cbd37-201">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="cbd37-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="cbd37-202">**Otros**</span><span class="sxs-lookup"><span data-stu-id="cbd37-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="cbd37-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="cbd37-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="cbd37-204">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cbd37-204">Examples</span></span>

<span data-ttu-id="cbd37-205">El siguiente [cambio de StartMode de un](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) ejemplo de PowerShell de servicio, extraído de la galería de TechNet, cambia el modo de inicio de un servicio.</span><span class="sxs-lookup"><span data-stu-id="cbd37-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="cbd37-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbd37-206">Requirements</span></span>



| <span data-ttu-id="cbd37-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd37-207">Requirement</span></span> | <span data-ttu-id="cbd37-208">Value</span><span class="sxs-lookup"><span data-stu-id="cbd37-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd37-209">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbd37-209">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd37-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbd37-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbd37-211">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbd37-211">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd37-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbd37-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbd37-213">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cbd37-213">Namespace</span></span><br/>                | <span data-ttu-id="cbd37-214">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cbd37-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbd37-215">MOF</span><span class="sxs-lookup"><span data-stu-id="cbd37-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbd37-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbd37-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbd37-217">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbd37-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd37-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd37-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd37-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbd37-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="cbd37-220">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbd37-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cbd37-221">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="cbd37-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="cbd37-222">Tareas WMI: servicios</span><span class="sxs-lookup"><span data-stu-id="cbd37-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

