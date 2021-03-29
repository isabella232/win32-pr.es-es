---
description: Intenta enviar un código de control definido por el usuario a un servicio.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Método UserControlService de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907465"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="6f28e-103">Método UserControlService de la \_ clase BaseService de Win32</span><span class="sxs-lookup"><span data-stu-id="6f28e-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="6f28e-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) intenta enviar un código de control definido por el usuario a un servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="6f28e-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6f28e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6f28e-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6f28e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f28e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f28e-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="6f28e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f28e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f28e-109">*ControlCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f28e-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-110">Valor que especifica un comando de control para un servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="6f28e-111">Por ejemplo, un comando de control es un comando de "pausa" o "continuar".</span><span class="sxs-lookup"><span data-stu-id="6f28e-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="6f28e-112">El valor puede ser un código predefinido, o un valor y una acción que define el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="6f28e-113">Estos son los códigos de control predefinidos:</span><span class="sxs-lookup"><span data-stu-id="6f28e-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="6f28e-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_continuar con el control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-115">Notifica a un servicio en pausa que se reanude.</span><span class="sxs-lookup"><span data-stu-id="6f28e-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="6f28e-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_interrogación de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-117">Notifica a un servicio que informe de la información de estado actual al administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="6f28e-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="6f28e-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-119">Notifica a un servicio de red que hay un nuevo componente para el enlace.</span><span class="sxs-lookup"><span data-stu-id="6f28e-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="6f28e-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-121">Notifica a un servicio de red que uno de sus enlaces está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6f28e-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="6f28e-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-123">Notifica a un servicio de red que se ha habilitado un enlace deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6f28e-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="6f28e-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-125">Notifica a un servicio de red que se ha quitado un componente para el enlace.</span><span class="sxs-lookup"><span data-stu-id="6f28e-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="6f28e-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-127">Notifica a un servicio que se han modificado sus parámetros de inicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="6f28e-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_pausa de control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-129">Notifica a un servicio que se PAUSE.</span><span class="sxs-lookup"><span data-stu-id="6f28e-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="6f28e-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_detención del control de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="6f28e-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="6f28e-131">Notifica a un servicio que se detenga.</span><span class="sxs-lookup"><span data-stu-id="6f28e-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f28e-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f28e-132">Return value</span></span>

<span data-ttu-id="6f28e-133">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="6f28e-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6f28e-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="6f28e-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-135">0</span><span class="sxs-lookup"><span data-stu-id="6f28e-135">0</span></span>

<span data-ttu-id="6f28e-136">Se acepta la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f28e-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-137">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="6f28e-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-138">1</span><span class="sxs-lookup"><span data-stu-id="6f28e-138">1</span></span>

<span data-ttu-id="6f28e-139">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f28e-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-140">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="6f28e-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-141">2</span><span class="sxs-lookup"><span data-stu-id="6f28e-141">2</span></span>

<span data-ttu-id="6f28e-142">El usuario no tiene los derechos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="6f28e-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-143">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="6f28e-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-144">3</span><span class="sxs-lookup"><span data-stu-id="6f28e-144">3</span></span>

<span data-ttu-id="6f28e-145">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="6f28e-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-146">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="6f28e-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-147">4</span><span class="sxs-lookup"><span data-stu-id="6f28e-147">4</span></span>

<span data-ttu-id="6f28e-148">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-149">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="6f28e-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-150">5</span><span class="sxs-lookup"><span data-stu-id="6f28e-150">5</span></span>

<span data-ttu-id="6f28e-151">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="6f28e-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-152">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="6f28e-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-153">6</span><span class="sxs-lookup"><span data-stu-id="6f28e-153">6</span></span>

<span data-ttu-id="6f28e-154">No se inició el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-155">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="6f28e-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-156">7</span><span class="sxs-lookup"><span data-stu-id="6f28e-156">7</span></span>

<span data-ttu-id="6f28e-157">El servicio no responde rápidamente a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-158">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="6f28e-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-159">8</span><span class="sxs-lookup"><span data-stu-id="6f28e-159">8</span></span>

<span data-ttu-id="6f28e-160">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="6f28e-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-161">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="6f28e-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-162">9</span><span class="sxs-lookup"><span data-stu-id="6f28e-162">9</span></span>

<span data-ttu-id="6f28e-163">No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-164">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="6f28e-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-165">10</span><span class="sxs-lookup"><span data-stu-id="6f28e-165">10</span></span>

<span data-ttu-id="6f28e-166">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6f28e-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-167">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="6f28e-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-168">11</span><span class="sxs-lookup"><span data-stu-id="6f28e-168">11</span></span>

<span data-ttu-id="6f28e-169">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6f28e-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-170">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="6f28e-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-171">12</span><span class="sxs-lookup"><span data-stu-id="6f28e-171">12</span></span>

<span data-ttu-id="6f28e-172">Una dependencia en la que se basa este servicio se quita del sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-173">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="6f28e-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-174">13</span><span class="sxs-lookup"><span data-stu-id="6f28e-174">13</span></span>

<span data-ttu-id="6f28e-175">El servicio no encuentra el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="6f28e-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-176">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="6f28e-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-177">14</span><span class="sxs-lookup"><span data-stu-id="6f28e-177">14</span></span>

<span data-ttu-id="6f28e-178">El servicio está deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-179">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="6f28e-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-180">15</span><span class="sxs-lookup"><span data-stu-id="6f28e-180">15</span></span>

<span data-ttu-id="6f28e-181">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-182">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="6f28e-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-183">16</span><span class="sxs-lookup"><span data-stu-id="6f28e-183">16</span></span>

<span data-ttu-id="6f28e-184">El servicio se va a quitar del sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-185">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="6f28e-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-186">17</span><span class="sxs-lookup"><span data-stu-id="6f28e-186">17</span></span>

<span data-ttu-id="6f28e-187">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-188">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="6f28e-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-189">18</span><span class="sxs-lookup"><span data-stu-id="6f28e-189">18</span></span>

<span data-ttu-id="6f28e-190">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-191">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="6f28e-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-192">19</span><span class="sxs-lookup"><span data-stu-id="6f28e-192">19</span></span>

<span data-ttu-id="6f28e-193">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="6f28e-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-194">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="6f28e-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-195">20</span><span class="sxs-lookup"><span data-stu-id="6f28e-195">20</span></span>

<span data-ttu-id="6f28e-196">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-197">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="6f28e-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-198">21</span><span class="sxs-lookup"><span data-stu-id="6f28e-198">21</span></span>

<span data-ttu-id="6f28e-199">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-200">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="6f28e-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-201">22</span><span class="sxs-lookup"><span data-stu-id="6f28e-201">22</span></span>

<span data-ttu-id="6f28e-202">La cuenta con la que se ejecuta este servicio no es válida o no tiene permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="6f28e-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-203">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="6f28e-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-204">23</span><span class="sxs-lookup"><span data-stu-id="6f28e-204">23</span></span>

<span data-ttu-id="6f28e-205">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-206">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="6f28e-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-207">24</span><span class="sxs-lookup"><span data-stu-id="6f28e-207">24</span></span>

<span data-ttu-id="6f28e-208">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6f28e-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="6f28e-209">**Otros**</span><span class="sxs-lookup"><span data-stu-id="6f28e-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6f28e-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="6f28e-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f28e-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f28e-211">Requirements</span></span>



| <span data-ttu-id="6f28e-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f28e-212">Requirement</span></span> | <span data-ttu-id="6f28e-213">Value</span><span class="sxs-lookup"><span data-stu-id="6f28e-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f28e-214">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f28e-214">Minimum supported client</span></span><br/> | <span data-ttu-id="6f28e-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f28e-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f28e-216">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f28e-216">Minimum supported server</span></span><br/> | <span data-ttu-id="6f28e-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f28e-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f28e-218">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f28e-218">Namespace</span></span><br/>                | <span data-ttu-id="6f28e-219">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6f28e-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f28e-220">MOF</span><span class="sxs-lookup"><span data-stu-id="6f28e-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f28e-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f28e-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f28e-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f28e-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f28e-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f28e-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f28e-224">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f28e-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f28e-225">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f28e-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6f28e-226">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="6f28e-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

