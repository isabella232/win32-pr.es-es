---
description: Modifica el modo de inicio de un \_ servicio SystemDriver de Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Método ChangeStartMode de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538775"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="44df8-103">Método ChangeStartMode de la \_ clase SystemDriver de Win32</span><span class="sxs-lookup"><span data-stu-id="44df8-103">ChangeStartMode method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="44df8-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de un servicio [**\_ SystemDriver de Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="44df8-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span>

<span data-ttu-id="44df8-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="44df8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44df8-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44df8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44df8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44df8-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="44df8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44df8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44df8-109">*StartMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="44df8-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44df8-110">Modo de inicio del servicio base de Windows.</span><span class="sxs-lookup"><span data-stu-id="44df8-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="44df8-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")</span><span class="sxs-lookup"><span data-stu-id="44df8-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="44df8-112">Controlador de dispositivo Iniciado por el cargador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="44df8-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="44df8-113">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="44df8-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="44df8-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")</span><span class="sxs-lookup"><span data-stu-id="44df8-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="44df8-115">Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="44df8-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="44df8-116">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="44df8-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="44df8-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="44df8-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="44df8-118">Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="44df8-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="44df8-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")</span><span class="sxs-lookup"><span data-stu-id="44df8-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="44df8-120">Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="44df8-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="44df8-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")</span><span class="sxs-lookup"><span data-stu-id="44df8-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="44df8-122">Servicio que ya no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="44df8-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44df8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44df8-123">Return value</span></span>

<span data-ttu-id="44df8-124">Devuelve un valor de 0 (cero) si el servicio se modificó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="44df8-124">Returns a value of 0 (zero) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="44df8-125">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="44df8-125">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-126">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="44df8-126">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-127">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="44df8-127">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-128">**Servicios dependientes en ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="44df8-128">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-129">**Control de servicio no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="44df8-129">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-130">El **servicio no puede aceptar el control** (5)</span><span class="sxs-lookup"><span data-stu-id="44df8-130">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-131">**Servicio no activo** (6)</span><span class="sxs-lookup"><span data-stu-id="44df8-131">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-132">**Tiempo de espera de solicitud de servicio** (7)</span><span class="sxs-lookup"><span data-stu-id="44df8-132">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-133">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="44df8-133">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-134">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="44df8-134">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-135">El **servicio ya se está ejecutando** (10)</span><span class="sxs-lookup"><span data-stu-id="44df8-135">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-136">**Base de datos de servicio bloqueada** (11)</span><span class="sxs-lookup"><span data-stu-id="44df8-136">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-137">**Dependencia de servicio eliminada** (12)</span><span class="sxs-lookup"><span data-stu-id="44df8-137">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-138">**Error de dependencia de servicio** (13)</span><span class="sxs-lookup"><span data-stu-id="44df8-138">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-139">**Servicio deshabilitado** (14)</span><span class="sxs-lookup"><span data-stu-id="44df8-139">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-140">**Error de inicio de sesión de servicio** (15)</span><span class="sxs-lookup"><span data-stu-id="44df8-140">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-141">**Servicio marcado para eliminación** (16)</span><span class="sxs-lookup"><span data-stu-id="44df8-141">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-142">**Servicio sin subproceso** (17)</span><span class="sxs-lookup"><span data-stu-id="44df8-142">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-143">**Estado dependencia circular** (18)</span><span class="sxs-lookup"><span data-stu-id="44df8-143">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-144">**Estado nombre duplicado** (19)</span><span class="sxs-lookup"><span data-stu-id="44df8-144">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-145">**Estado nombre no válido** (20)</span><span class="sxs-lookup"><span data-stu-id="44df8-145">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-146">**Estado parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="44df8-146">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-147">**Estado cuenta de servicio no válida** (22)</span><span class="sxs-lookup"><span data-stu-id="44df8-147">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-148">El **servicio de estado existe** (23)</span><span class="sxs-lookup"><span data-stu-id="44df8-148">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-149">**Servicio ya pausado** (24)</span><span class="sxs-lookup"><span data-stu-id="44df8-149">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="44df8-150">**Otro** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="44df8-150">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44df8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44df8-151">Requirements</span></span>



| <span data-ttu-id="44df8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="44df8-152">Requirement</span></span> | <span data-ttu-id="44df8-153">Value</span><span class="sxs-lookup"><span data-stu-id="44df8-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44df8-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44df8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="44df8-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44df8-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44df8-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44df8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="44df8-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44df8-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44df8-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44df8-158">Namespace</span></span><br/>                | <span data-ttu-id="44df8-159">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44df8-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44df8-160">MOF</span><span class="sxs-lookup"><span data-stu-id="44df8-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44df8-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44df8-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44df8-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44df8-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44df8-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44df8-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44df8-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="44df8-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="44df8-165">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44df8-165">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="44df8-166">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="44df8-166">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

