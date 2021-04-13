---
description: SetPriority&\# 32; El método de clase WMI intenta cambiar la prioridad de ejecución del proceso.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Método SetPriority de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539261"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="1a2b4-103">Método SetPriority de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="1a2b4-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="1a2b4-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPriority** intenta cambiar la prioridad de ejecución del proceso.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="1a2b4-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1a2b4-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a2b4-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="1a2b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a2b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a2b4-109">*Prioridad* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1a2b4-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a2b4-110">Nueva clase de prioridad para el proceso.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-110">New priority class for the process.</span></span> <span data-ttu-id="1a2b4-111">Tenga en cuenta que estos valores son diferentes de los indicados explícitamente en la propiedad **Priority** del [**\_ proceso Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="1a2b4-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-113">Especificado para un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="1a2b4-114">Los subprocesos del proceso son retenidos por los subprocesos de un proceso que se ejecutan en una clase de prioridad más alta, por ejemplo, un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="1a2b4-115">Los procesos secundarios heredan la clase de prioridad de inactividad.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="1a2b4-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Por debajo** de lo Normal (16384)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-117">Indica un proceso que tiene prioridad sobre **la \_ \_ clase de prioridad de inactividad**, pero por debajo de la **\_ \_ clase de prioridad normal**.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="1a2b4-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-119">Se especifica para un proceso sin necesidad de programación especial.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="1a2b4-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Por encima** de lo Normal (32768)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-121">Indica un proceso que tiene prioridad sobre **la \_ \_ clase de prioridad normal**, pero por debajo de la **\_ \_ clase de prioridad alta**.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="1a2b4-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Prioridad alta** (128)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-123">Se especifica para un proceso que realiza tareas críticas en el tiempo que se deben ejecutar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="1a2b4-124">Los subprocesos del proceso tienen prioridad sobre los subprocesos de aquellos procesos de clase de prioridad normal o inactiva.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="1a2b4-125">Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="1a2b4-126">Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación de clase de prioridad alta puede usar casi todo el tiempo de CPU disponible.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="1a2b4-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="1a2b4-128">Especificado para un proceso que tiene la prioridad más alta posible.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="1a2b4-129">Los subprocesos del proceso tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="1a2b4-130">Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés del disco no se vacíen o que el mouse no responda.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a2b4-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a2b4-131">Return value</span></span>

<span data-ttu-id="1a2b4-132">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="1a2b4-133">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1a2b4-134">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1a2b4-135">**Finalización correcta** (0)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-136">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-137">**Privilegios insuficientes** (3)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-138">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-139">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-140">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1a2b4-141">**Otro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="1a2b4-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1a2b4-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a2b4-142">Remarks</span></span>

<span data-ttu-id="1a2b4-143">Para establecer la prioridad en tiempo real, el autor de la  llamada debe tener el **\_ \_ \_ \_ privilegio de prioridad base** de SeIncreaseBasePriorityPrivilege (se Inc).</span><span class="sxs-lookup"><span data-stu-id="1a2b4-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="1a2b4-144">Sin este privilegio, la prioridad más alta puede establecerse en una prioridad alta.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="1a2b4-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1a2b4-145">Examples</span></span>

<span data-ttu-id="1a2b4-146">El ejemplo de [modificación de la prioridad de un proceso en ejecución](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) de VBScript cambia la prioridad de una instancia en ejecución de Notepad.exe de normal a por encima de lo normal.</span><span class="sxs-lookup"><span data-stu-id="1a2b4-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2b4-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a2b4-147">Requirements</span></span>



| <span data-ttu-id="1a2b4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a2b4-148">Requirement</span></span> | <span data-ttu-id="1a2b4-149">Value</span><span class="sxs-lookup"><span data-stu-id="1a2b4-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2b4-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a2b4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1a2b4-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a2b4-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a2b4-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a2b4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1a2b4-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a2b4-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a2b4-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a2b4-154">Namespace</span></span><br/>                | <span data-ttu-id="1a2b4-155">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a2b4-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a2b4-156">MOF</span><span class="sxs-lookup"><span data-stu-id="1a2b4-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a2b4-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b4-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a2b4-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a2b4-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a2b4-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a2b4-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a2b4-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a2b4-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a2b4-161">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a2b4-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a2b4-162">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="1a2b4-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

