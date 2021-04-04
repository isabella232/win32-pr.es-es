---
description: Solicita que el servicio actualice su estado al administrador de servicios.
ms.assetid: 118156ef-ee43-4f73-af41-e295a0a850b9
ms.tgt_platform: multiple
title: Método InterrogateService de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29e29c152e7fea8de7a2ccaf1e7d86bf3a08d4c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998230"
---
# <a name="interrogateservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="56bc5-103">Método InterrogateService de la \_ clase BaseService de Win32</span><span class="sxs-lookup"><span data-stu-id="56bc5-103">InterrogateService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="56bc5-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que el servicio actualice su estado al administrador de servicios.</span><span class="sxs-lookup"><span data-stu-id="56bc5-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the service update its state to the service manager.</span></span>

<span data-ttu-id="56bc5-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="56bc5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="56bc5-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="56bc5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="56bc5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56bc5-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="56bc5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56bc5-108">Parameters</span></span>

<span data-ttu-id="56bc5-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="56bc5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56bc5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56bc5-110">Return value</span></span>

<span data-ttu-id="56bc5-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="56bc5-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="56bc5-112">**Success**</span><span class="sxs-lookup"><span data-stu-id="56bc5-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-113">0</span><span class="sxs-lookup"><span data-stu-id="56bc5-113">0</span></span>

<span data-ttu-id="56bc5-114">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56bc5-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-115">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="56bc5-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-116">1</span><span class="sxs-lookup"><span data-stu-id="56bc5-116">1</span></span>

<span data-ttu-id="56bc5-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56bc5-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-118">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="56bc5-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-119">2</span><span class="sxs-lookup"><span data-stu-id="56bc5-119">2</span></span>

<span data-ttu-id="56bc5-120">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="56bc5-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-121">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="56bc5-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-122">3</span><span class="sxs-lookup"><span data-stu-id="56bc5-122">3</span></span>

<span data-ttu-id="56bc5-123">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="56bc5-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-124">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="56bc5-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-125">4</span><span class="sxs-lookup"><span data-stu-id="56bc5-125">4</span></span>

<span data-ttu-id="56bc5-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-127">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="56bc5-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-128">5</span><span class="sxs-lookup"><span data-stu-id="56bc5-128">5</span></span>

<span data-ttu-id="56bc5-129">El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad de [**Estado**](win32-baseservice.md) [**\_ BaseService de Win32**](win32-baseservice.md)) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="56bc5-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-130">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="56bc5-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-131">6</span><span class="sxs-lookup"><span data-stu-id="56bc5-131">6</span></span>

<span data-ttu-id="56bc5-132">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="56bc5-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-133">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="56bc5-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-134">7</span><span class="sxs-lookup"><span data-stu-id="56bc5-134">7</span></span>

<span data-ttu-id="56bc5-135">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-136">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="56bc5-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-137">8</span><span class="sxs-lookup"><span data-stu-id="56bc5-137">8</span></span>

<span data-ttu-id="56bc5-138">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="56bc5-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-139">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="56bc5-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-140">9</span><span class="sxs-lookup"><span data-stu-id="56bc5-140">9</span></span>

<span data-ttu-id="56bc5-141">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-142">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="56bc5-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-143">10</span><span class="sxs-lookup"><span data-stu-id="56bc5-143">10</span></span>

<span data-ttu-id="56bc5-144">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="56bc5-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-145">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="56bc5-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-146">11</span><span class="sxs-lookup"><span data-stu-id="56bc5-146">11</span></span>

<span data-ttu-id="56bc5-147">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="56bc5-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-148">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="56bc5-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-149">12</span><span class="sxs-lookup"><span data-stu-id="56bc5-149">12</span></span>

<span data-ttu-id="56bc5-150">Una dependencia en la que se basaba este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-151">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="56bc5-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-152">13</span><span class="sxs-lookup"><span data-stu-id="56bc5-152">13</span></span>

<span data-ttu-id="56bc5-153">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="56bc5-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-154">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="56bc5-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-155">14</span><span class="sxs-lookup"><span data-stu-id="56bc5-155">14</span></span>

<span data-ttu-id="56bc5-156">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-157">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="56bc5-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-158">15</span><span class="sxs-lookup"><span data-stu-id="56bc5-158">15</span></span>

<span data-ttu-id="56bc5-159">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-160">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="56bc5-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-161">16</span><span class="sxs-lookup"><span data-stu-id="56bc5-161">16</span></span>

<span data-ttu-id="56bc5-162">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-163">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="56bc5-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-164">17</span><span class="sxs-lookup"><span data-stu-id="56bc5-164">17</span></span>

<span data-ttu-id="56bc5-165">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-166">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="56bc5-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-167">18</span><span class="sxs-lookup"><span data-stu-id="56bc5-167">18</span></span>

<span data-ttu-id="56bc5-168">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-169">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="56bc5-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-170">19</span><span class="sxs-lookup"><span data-stu-id="56bc5-170">19</span></span>

<span data-ttu-id="56bc5-171">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="56bc5-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-172">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="56bc5-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-173">20</span><span class="sxs-lookup"><span data-stu-id="56bc5-173">20</span></span>

<span data-ttu-id="56bc5-174">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-175">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="56bc5-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-176">21</span><span class="sxs-lookup"><span data-stu-id="56bc5-176">21</span></span>

<span data-ttu-id="56bc5-177">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-178">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="56bc5-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-179">22</span><span class="sxs-lookup"><span data-stu-id="56bc5-179">22</span></span>

<span data-ttu-id="56bc5-180">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="56bc5-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-181">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="56bc5-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-182">23</span><span class="sxs-lookup"><span data-stu-id="56bc5-182">23</span></span>

<span data-ttu-id="56bc5-183">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-184">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="56bc5-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-185">24</span><span class="sxs-lookup"><span data-stu-id="56bc5-185">24</span></span>

<span data-ttu-id="56bc5-186">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="56bc5-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="56bc5-187">**Otros**</span><span class="sxs-lookup"><span data-stu-id="56bc5-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="56bc5-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="56bc5-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56bc5-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56bc5-189">Requirements</span></span>



| <span data-ttu-id="56bc5-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="56bc5-190">Requirement</span></span> | <span data-ttu-id="56bc5-191">Value</span><span class="sxs-lookup"><span data-stu-id="56bc5-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56bc5-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56bc5-192">Minimum supported client</span></span><br/> | <span data-ttu-id="56bc5-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56bc5-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56bc5-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56bc5-194">Minimum supported server</span></span><br/> | <span data-ttu-id="56bc5-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56bc5-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56bc5-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56bc5-196">Namespace</span></span><br/>                | <span data-ttu-id="56bc5-197">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56bc5-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56bc5-198">MOF</span><span class="sxs-lookup"><span data-stu-id="56bc5-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56bc5-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56bc5-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56bc5-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56bc5-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bc5-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bc5-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56bc5-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="56bc5-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="56bc5-203">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56bc5-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="56bc5-204">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="56bc5-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

