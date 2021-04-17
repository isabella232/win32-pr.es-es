---
description: Intenta colocar el servicio al que se hace referencia en el estado de pausa.
ms.assetid: 57b8ccdd-056a-4bec-a0f8-ecebcf18039e
ms.tgt_platform: multiple
title: Método PauseService de la clase Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4828b81af5d6d543aaf16a34a08350f09078d623
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659760"
---
# <a name="pauseservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="873f3-103">Método PauseService de la \_ clase BaseService de Win32</span><span class="sxs-lookup"><span data-stu-id="873f3-103">PauseService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="873f3-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta colocar el servicio al que se hace referencia en el estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="873f3-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the paused state.</span></span>

<span data-ttu-id="873f3-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="873f3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="873f3-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="873f3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="873f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="873f3-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="873f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="873f3-108">Parameters</span></span>

<span data-ttu-id="873f3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="873f3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="873f3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="873f3-110">Return value</span></span>

<span data-ttu-id="873f3-111">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="873f3-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="873f3-112">**Success**</span><span class="sxs-lookup"><span data-stu-id="873f3-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-113">0</span><span class="sxs-lookup"><span data-stu-id="873f3-113">0</span></span>

<span data-ttu-id="873f3-114">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="873f3-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-115">**No compatible**</span><span class="sxs-lookup"><span data-stu-id="873f3-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-116">1</span><span class="sxs-lookup"><span data-stu-id="873f3-116">1</span></span>

<span data-ttu-id="873f3-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="873f3-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-118">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="873f3-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-119">2</span><span class="sxs-lookup"><span data-stu-id="873f3-119">2</span></span>

<span data-ttu-id="873f3-120">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="873f3-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-121">**Servicios dependientes en ejecución**</span><span class="sxs-lookup"><span data-stu-id="873f3-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-122">3</span><span class="sxs-lookup"><span data-stu-id="873f3-122">3</span></span>

<span data-ttu-id="873f3-123">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="873f3-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-124">**Control de servicio no válido**</span><span class="sxs-lookup"><span data-stu-id="873f3-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-125">4</span><span class="sxs-lookup"><span data-stu-id="873f3-125">4</span></span>

<span data-ttu-id="873f3-126">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-127">**El servicio no puede aceptar el control**</span><span class="sxs-lookup"><span data-stu-id="873f3-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-128">5</span><span class="sxs-lookup"><span data-stu-id="873f3-128">5</span></span>

<span data-ttu-id="873f3-129">El código de control solicitado no se puede enviar al servicio porque el estado del servicio (propiedad de [**Estado**](win32-baseservice.md) [**\_ BaseService de Win32**](win32-baseservice.md)) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="873f3-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-130">**Servicio no activo**</span><span class="sxs-lookup"><span data-stu-id="873f3-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-131">6</span><span class="sxs-lookup"><span data-stu-id="873f3-131">6</span></span>

<span data-ttu-id="873f3-132">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="873f3-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-133">**Tiempo de espera de solicitud de servicio**</span><span class="sxs-lookup"><span data-stu-id="873f3-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-134">7</span><span class="sxs-lookup"><span data-stu-id="873f3-134">7</span></span>

<span data-ttu-id="873f3-135">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-136">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="873f3-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-137">8</span><span class="sxs-lookup"><span data-stu-id="873f3-137">8</span></span>

<span data-ttu-id="873f3-138">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="873f3-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-139">**Ruta de acceso no encontrada**</span><span class="sxs-lookup"><span data-stu-id="873f3-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-140">9</span><span class="sxs-lookup"><span data-stu-id="873f3-140">9</span></span>

<span data-ttu-id="873f3-141">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-142">**El servicio ya se está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="873f3-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-143">10</span><span class="sxs-lookup"><span data-stu-id="873f3-143">10</span></span>

<span data-ttu-id="873f3-144">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="873f3-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-145">**Base de datos de servicio bloqueada**</span><span class="sxs-lookup"><span data-stu-id="873f3-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-146">11</span><span class="sxs-lookup"><span data-stu-id="873f3-146">11</span></span>

<span data-ttu-id="873f3-147">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="873f3-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-148">**Dependencia de servicio eliminada**</span><span class="sxs-lookup"><span data-stu-id="873f3-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-149">12</span><span class="sxs-lookup"><span data-stu-id="873f3-149">12</span></span>

<span data-ttu-id="873f3-150">Una dependencia en la que se basaba este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-151">**Error de dependencia de servicio**</span><span class="sxs-lookup"><span data-stu-id="873f3-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-152">13</span><span class="sxs-lookup"><span data-stu-id="873f3-152">13</span></span>

<span data-ttu-id="873f3-153">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="873f3-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-154">**Servicio deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="873f3-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-155">14</span><span class="sxs-lookup"><span data-stu-id="873f3-155">14</span></span>

<span data-ttu-id="873f3-156">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-157">**Error de inicio de sesión de servicio**</span><span class="sxs-lookup"><span data-stu-id="873f3-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-158">15</span><span class="sxs-lookup"><span data-stu-id="873f3-158">15</span></span>

<span data-ttu-id="873f3-159">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-160">**Servicio marcado para eliminación**</span><span class="sxs-lookup"><span data-stu-id="873f3-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-161">16</span><span class="sxs-lookup"><span data-stu-id="873f3-161">16</span></span>

<span data-ttu-id="873f3-162">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-163">**Servicio sin subproceso**</span><span class="sxs-lookup"><span data-stu-id="873f3-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-164">17</span><span class="sxs-lookup"><span data-stu-id="873f3-164">17</span></span>

<span data-ttu-id="873f3-165">No hay ningún subproceso de ejecución para el servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-166">**Estado dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="873f3-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-167">18</span><span class="sxs-lookup"><span data-stu-id="873f3-167">18</span></span>

<span data-ttu-id="873f3-168">Hay dependencias circulares al iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-169">**Estado nombre duplicado**</span><span class="sxs-lookup"><span data-stu-id="873f3-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-170">19</span><span class="sxs-lookup"><span data-stu-id="873f3-170">19</span></span>

<span data-ttu-id="873f3-171">Hay un servicio que se ejecuta con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="873f3-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-172">**Estado nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="873f3-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-173">20</span><span class="sxs-lookup"><span data-stu-id="873f3-173">20</span></span>

<span data-ttu-id="873f3-174">Hay caracteres no válidos en el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-175">**Estado parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="873f3-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-176">21</span><span class="sxs-lookup"><span data-stu-id="873f3-176">21</span></span>

<span data-ttu-id="873f3-177">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-178">**Estado cuenta de servicio no válida**</span><span class="sxs-lookup"><span data-stu-id="873f3-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-179">22</span><span class="sxs-lookup"><span data-stu-id="873f3-179">22</span></span>

<span data-ttu-id="873f3-180">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="873f3-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-181">**El servicio de estado existe**</span><span class="sxs-lookup"><span data-stu-id="873f3-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-182">23</span><span class="sxs-lookup"><span data-stu-id="873f3-182">23</span></span>

<span data-ttu-id="873f3-183">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-184">**Servicio ya pausado**</span><span class="sxs-lookup"><span data-stu-id="873f3-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-185">24</span><span class="sxs-lookup"><span data-stu-id="873f3-185">24</span></span>

<span data-ttu-id="873f3-186">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="873f3-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="873f3-187">**Otros**</span><span class="sxs-lookup"><span data-stu-id="873f3-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="873f3-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="873f3-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="873f3-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="873f3-189">Requirements</span></span>



| <span data-ttu-id="873f3-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="873f3-190">Requirement</span></span> | <span data-ttu-id="873f3-191">Value</span><span class="sxs-lookup"><span data-stu-id="873f3-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="873f3-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="873f3-192">Minimum supported client</span></span><br/> | <span data-ttu-id="873f3-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="873f3-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="873f3-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="873f3-194">Minimum supported server</span></span><br/> | <span data-ttu-id="873f3-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="873f3-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="873f3-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="873f3-196">Namespace</span></span><br/>                | <span data-ttu-id="873f3-197">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="873f3-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="873f3-198">MOF</span><span class="sxs-lookup"><span data-stu-id="873f3-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="873f3-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="873f3-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="873f3-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="873f3-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="873f3-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="873f3-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873f3-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="873f3-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="873f3-203">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="873f3-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="873f3-204">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="873f3-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

