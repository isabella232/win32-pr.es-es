---
description: Modifica el modo de inicio de un objeto de servicio derivado de Win32 \_ BaseService.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Método ChangeStartMode de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153058"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="128ab-103">Método ChangeStartMode de la \_ clase BaseService de Win32</span><span class="sxs-lookup"><span data-stu-id="128ab-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="128ab-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de un objeto de servicio derivado de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="128ab-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="128ab-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="128ab-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="128ab-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="128ab-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="128ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="128ab-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="128ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="128ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128ab-109">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="128ab-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128ab-110">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="128ab-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="128ab-111">El valor predeterminado es "Automatic".</span><span class="sxs-lookup"><span data-stu-id="128ab-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="128ab-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="128ab-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="128ab-113">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="128ab-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="128ab-114">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="128ab-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="128ab-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="128ab-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="128ab-116">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="128ab-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="128ab-117">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="128ab-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="128ab-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="128ab-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="128ab-119">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="128ab-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")</span><span class="sxs-lookup"><span data-stu-id="128ab-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="128ab-121">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="128ab-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="128ab-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="128ab-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="128ab-123">El servicio está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="128ab-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128ab-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="128ab-124">Return value</span></span>

<span data-ttu-id="128ab-125">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="128ab-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="128ab-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="128ab-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-127">0</span><span class="sxs-lookup"><span data-stu-id="128ab-127">0</span></span>

<span data-ttu-id="128ab-128">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="128ab-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-129">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="128ab-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-130">1</span><span class="sxs-lookup"><span data-stu-id="128ab-130">1</span></span>

<span data-ttu-id="128ab-131">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="128ab-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-132">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="128ab-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-133">2</span><span class="sxs-lookup"><span data-stu-id="128ab-133">2</span></span>

<span data-ttu-id="128ab-134">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="128ab-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-135">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="128ab-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-136">3</span><span class="sxs-lookup"><span data-stu-id="128ab-136">3</span></span>

<span data-ttu-id="128ab-137">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="128ab-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-138">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="128ab-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-139">4</span><span class="sxs-lookup"><span data-stu-id="128ab-139">4</span></span>

<span data-ttu-id="128ab-140">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-141">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="128ab-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-142">5</span><span class="sxs-lookup"><span data-stu-id="128ab-142">5</span></span>

<span data-ttu-id="128ab-143">El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad de [**Estado**](win32-baseservice.md) [**\_ BaseService de Win32**](win32-baseservice.md)) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="128ab-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-144">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="128ab-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-145">6</span><span class="sxs-lookup"><span data-stu-id="128ab-145">6</span></span>

<span data-ttu-id="128ab-146">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="128ab-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-147">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="128ab-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-148">7</span><span class="sxs-lookup"><span data-stu-id="128ab-148">7</span></span>

<span data-ttu-id="128ab-149">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-150">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="128ab-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-151">8</span><span class="sxs-lookup"><span data-stu-id="128ab-151">8</span></span>

<span data-ttu-id="128ab-152">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="128ab-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-153">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="128ab-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-154">9</span><span class="sxs-lookup"><span data-stu-id="128ab-154">9</span></span>

<span data-ttu-id="128ab-155">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-156">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="128ab-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-157">10</span><span class="sxs-lookup"><span data-stu-id="128ab-157">10</span></span>

<span data-ttu-id="128ab-158">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="128ab-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-159">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="128ab-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-160">11</span><span class="sxs-lookup"><span data-stu-id="128ab-160">11</span></span>

<span data-ttu-id="128ab-161">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="128ab-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-162">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="128ab-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-163">12</span><span class="sxs-lookup"><span data-stu-id="128ab-163">12</span></span>

<span data-ttu-id="128ab-164">Una dependencia en la que se basaba este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-165">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="128ab-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-166">13</span><span class="sxs-lookup"><span data-stu-id="128ab-166">13</span></span>

<span data-ttu-id="128ab-167">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="128ab-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-168">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="128ab-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-169">14</span><span class="sxs-lookup"><span data-stu-id="128ab-169">14</span></span>

<span data-ttu-id="128ab-170">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-171">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="128ab-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-172">15</span><span class="sxs-lookup"><span data-stu-id="128ab-172">15</span></span>

<span data-ttu-id="128ab-173">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-174">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="128ab-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-175">16</span><span class="sxs-lookup"><span data-stu-id="128ab-175">16</span></span>

<span data-ttu-id="128ab-176">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-177">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="128ab-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-178">17</span><span class="sxs-lookup"><span data-stu-id="128ab-178">17</span></span>

<span data-ttu-id="128ab-179">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-180">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="128ab-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-181">18</span><span class="sxs-lookup"><span data-stu-id="128ab-181">18</span></span>

<span data-ttu-id="128ab-182">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-183">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="128ab-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-184">19</span><span class="sxs-lookup"><span data-stu-id="128ab-184">19</span></span>

<span data-ttu-id="128ab-185">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="128ab-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-186">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="128ab-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-187">20</span><span class="sxs-lookup"><span data-stu-id="128ab-187">20</span></span>

<span data-ttu-id="128ab-188">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-189">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="128ab-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-190">21</span><span class="sxs-lookup"><span data-stu-id="128ab-190">21</span></span>

<span data-ttu-id="128ab-191">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-192">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="128ab-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-193">22</span><span class="sxs-lookup"><span data-stu-id="128ab-193">22</span></span>

<span data-ttu-id="128ab-194">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="128ab-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-195">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="128ab-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-196">23</span><span class="sxs-lookup"><span data-stu-id="128ab-196">23</span></span>

<span data-ttu-id="128ab-197">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-198">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="128ab-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-199">24</span><span class="sxs-lookup"><span data-stu-id="128ab-199">24</span></span>

<span data-ttu-id="128ab-200">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="128ab-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="128ab-201">**Otros**</span><span class="sxs-lookup"><span data-stu-id="128ab-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="128ab-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="128ab-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="128ab-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128ab-203">Requirements</span></span>



| <span data-ttu-id="128ab-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="128ab-204">Requirement</span></span> | <span data-ttu-id="128ab-205">Value</span><span class="sxs-lookup"><span data-stu-id="128ab-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="128ab-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128ab-206">Minimum supported client</span></span><br/> | <span data-ttu-id="128ab-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="128ab-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="128ab-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="128ab-208">Minimum supported server</span></span><br/> | <span data-ttu-id="128ab-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="128ab-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="128ab-210">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="128ab-210">Namespace</span></span><br/>                | <span data-ttu-id="128ab-211">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="128ab-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="128ab-212">MOF</span><span class="sxs-lookup"><span data-stu-id="128ab-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="128ab-213"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="128ab-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="128ab-214">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="128ab-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="128ab-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="128ab-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="128ab-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="128ab-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="128ab-217">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="128ab-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="128ab-218">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="128ab-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

