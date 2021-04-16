---
title: Novedades de Programador de tareas
description: Lista de nuevas funcionalidades introducidas por versiones diferentes de Programador de tareas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Programador de tareas Programador de tareas, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677247"
---
# <a name="whats-new-in-task-scheduler"></a><span data-ttu-id="10f9b-104">Novedades de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="10f9b-104">What's New in Task Scheduler</span></span>

<span data-ttu-id="10f9b-105">Los cambios siguientes resumen las novedades de las distintas versiones de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="10f9b-105">The following changes summarize what is new in different versions of Task Scheduler.</span></span>

## <a name="windows-10-and-windows-server-2016"></a><span data-ttu-id="10f9b-106">Windows 10 (y Windows Server 2016)</span><span class="sxs-lookup"><span data-stu-id="10f9b-106">Windows 10 (and Windows Server 2016)</span></span>

<span data-ttu-id="10f9b-107">Los siguientes cambios de Programador de tareas se introdujeron en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="10f9b-107">The following Task Scheduler changes are introduced in Windows 10.</span></span>

-   <span data-ttu-id="10f9b-108">Cuando el ahorro de batería está activado, las tareas de Windows Programador de tareas se desencadenan solo si la tarea es:</span><span class="sxs-lookup"><span data-stu-id="10f9b-108">When battery saver is on, Windows Task Scheduler tasks are triggered only if the task is:</span></span>

    -   <span data-ttu-id="10f9b-109">No está configurado para **iniciar la tarea solo si el equipo está inactivo... (la** tarea no usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span><span class="sxs-lookup"><span data-stu-id="10f9b-109">Not set to **Start the task only if the computer is idle...** (task doesn't use [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))</span></span>
    -   <span data-ttu-id="10f9b-110">No está configurado para ejecutarse durante el mantenimiento automático (la tarea no usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span><span class="sxs-lookup"><span data-stu-id="10f9b-110">Not set to run during automatic maintenance (task doesn't use [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))</span></span>
    -   <span data-ttu-id="10f9b-111">Está configurado para **ejecutarse solo cuando el usuario ha iniciado sesión** (la tarea [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) es el **\_ \_ \_ token interactivo interactivo de inicio** de sesión de tarea o el **grupo de inicio de \_ sesión \_ de tareas**)</span><span class="sxs-lookup"><span data-stu-id="10f9b-111">Is set to **Run only when user is logged on** (task [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) is **TASK\_LOGON\_INTERACTIVE\_TOKEN** or **TASK\_LOGON\_GROUP**)</span></span>

    <span data-ttu-id="10f9b-112">El resto de los desencadenadores se retrasa hasta que el ahorro de batería está desactivado.</span><span class="sxs-lookup"><span data-stu-id="10f9b-112">All other triggers are delayed until battery saver is off.</span></span> <span data-ttu-id="10f9b-113">Para obtener más información sobre el acceso al estado del ahorro de batería en la aplicación, consulte [**\_ \_ Estado de la energía del sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span><span class="sxs-lookup"><span data-stu-id="10f9b-113">For more information about accessing battery saver status in your application, see [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status).</span></span> <span data-ttu-id="10f9b-114">Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="10f9b-114">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="10f9b-115">Por motivos de seguridad, un usuario que no es administrador no puede ver ni administrar una tarea de Programador de tareas de Windows creada por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="10f9b-115">For security reasons, a non-administrator user cannot view nor manage a Windows Task Scheduler task that was created by another user.</span></span>

## <a name="windows-8"></a><span data-ttu-id="10f9b-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="10f9b-116">Windows 8</span></span>

<span data-ttu-id="10f9b-117">En Windows 8 se introdujeron los siguientes cambios Programador de tareas 2,0:</span><span class="sxs-lookup"><span data-stu-id="10f9b-117">The following Task Scheduler 2.0 changes are introduced in Windows 8:</span></span>

-   <span data-ttu-id="10f9b-118">Compatibilidad con PowerShell: los usuarios pueden administrar (crear, eliminar, modificar, iniciar explícitamente, detener, etc.) Windows Programador de tareas tareas mediante el módulo de PowerShell ScheduledTasks.</span><span class="sxs-lookup"><span data-stu-id="10f9b-118">Powershell support: users can manage (create, delete, modify, explicitly start, stop etc.) Windows Task Scheduler tasks using the ScheduledTasks powershell module.</span></span>
-   <span data-ttu-id="10f9b-119">Contraseñas administradas: los administradores pueden usar el Active Directory cuentas de contraseña administradas como entidades de seguridad de tareas.</span><span class="sxs-lookup"><span data-stu-id="10f9b-119">Managed passwords: administrators can use the Active Directory managed password accounts as task principals.</span></span> <span data-ttu-id="10f9b-120">Estas tareas ya no requieren una directiva de restablecimiento de contraseña forzada.</span><span class="sxs-lookup"><span data-stu-id="10f9b-120">These tasks no longer require an enforced password reset policy.</span></span>
-   <span data-ttu-id="10f9b-121">Cambios de la API: se introdujeron dos nuevas configuraciones de tarea con la interfaz [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .</span><span class="sxs-lookup"><span data-stu-id="10f9b-121">API changes: Introduced two new task settings with the [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) interface.</span></span>
    -   <span data-ttu-id="10f9b-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): las tareas que usan estos valores se tratan como un nuevo tipo de tareas programadas que se invocan durante el tiempo de mantenimiento automático del sistema operativo, de acuerdo con la periodicidad y la fecha límite especificadas.</span><span class="sxs-lookup"><span data-stu-id="10f9b-122">[**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): tasks using these settings are treated as a new type of scheduled tasks that are invoked during OS automatic maintenance time, according to the specified periodicity and deadline.</span></span>
    -   <span data-ttu-id="10f9b-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): las tareas que se establecen en volatile siempre están deshabilitadas en un arranque del sistema operativo y se deben volver a habilitar explícitamente cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="10f9b-123">[**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): tasks that are set to be volatile are always disabled on an OS boot and must be explicitly re-enabled back when required.</span></span> <span data-ttu-id="10f9b-124">Los clústeres de conmutación por error usan las tareas volátiles para asegurarse de que solo se programa una instancia de tarea en un clúster a la vez.</span><span class="sxs-lookup"><span data-stu-id="10f9b-124">Volatile tasks are utilized by the failover clusters to ensure only one task instance is scheduled on a cluster at a time.</span></span>
-   <span data-ttu-id="10f9b-125">El motor de programación unificado ahora admite las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="10f9b-125">The unified scheduling engine now supports the following features:</span></span>
    -   <span data-ttu-id="10f9b-126">Tipo de inicio de sesión S4U, mediante el elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10f9b-126">S4U Logon type, through the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element.</span></span>
    -   <span data-ttu-id="10f9b-127">Valores de consulta XPath para desencadenadores de eventos, a través del elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10f9b-127">XPath query values for event triggers, through the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element.</span></span>
    -   <span data-ttu-id="10f9b-128">No permita que finalice la tarea a través del elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="10f9b-128">Do not allow task hard terminate, through the [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) element.</span></span>
-   <span data-ttu-id="10f9b-129">Características desusadas en esta versión</span><span class="sxs-lookup"><span data-stu-id="10f9b-129">Features deprecated in this release</span></span>
    -   <span data-ttu-id="10f9b-130">Acción: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (puede usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) con el cmdlet [send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) de [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)como solución alternativa).</span><span class="sxs-lookup"><span data-stu-id="10f9b-130">Action: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (you can use [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) with the [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround).</span></span>
    -   <span data-ttu-id="10f9b-131">Acción: [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span><span class="sxs-lookup"><span data-stu-id="10f9b-131">Action: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).</span></span>
    -   <span data-ttu-id="10f9b-132">AT.exe utilidad cmdline</span><span class="sxs-lookup"><span data-stu-id="10f9b-132">AT.exe cmdline utility</span></span>

## <a name="windows-7"></a><span data-ttu-id="10f9b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10f9b-133">Windows 7</span></span>

<span data-ttu-id="10f9b-134">En Windows 7 se introdujeron los siguientes cambios Programador de tareas 2,0:</span><span class="sxs-lookup"><span data-stu-id="10f9b-134">The following Task Scheduler 2.0 changes are introduced in Windows 7:</span></span>

-   <span data-ttu-id="10f9b-135">Usar el motor de programación unificado proporcionado por el sistema operativo subyacente.</span><span class="sxs-lookup"><span data-stu-id="10f9b-135">Using the unified scheduling engine provided by the underlying operating system.</span></span>
-   <span data-ttu-id="10f9b-136">Capacidad de rechazar las tareas iniciales en las sesiones remotas integradas (ferrocarril).</span><span class="sxs-lookup"><span data-stu-id="10f9b-136">Ability to reject starting tasks in Remote Applications Integrated Locally (RAIL) sessions.</span></span>
-   <span data-ttu-id="10f9b-137">Protección de la seguridad de tareas (solo para tareas que se ejecutan como "servicio de red" o "servicio LOCAL"):</span><span class="sxs-lookup"><span data-stu-id="10f9b-137">Task security hardening (for tasks running as "NETWORK SERVICE" or "LOCAL SERVICE" only):</span></span>

    -   <span data-ttu-id="10f9b-138">Capacidad de asignar un tipo de identificador de seguridad (SID) de token de proceso (por ejemplo, Unrestricted o None) a una tarea.</span><span class="sxs-lookup"><span data-stu-id="10f9b-138">Ability to assign a process token security identifier (SID) type (for example, unrestricted or none) to a task.</span></span>
    -   <span data-ttu-id="10f9b-139">Permita que los desarrolladores de tareas soliciten el conjunto exacto de privilegios que requiere su tarea.</span><span class="sxs-lookup"><span data-stu-id="10f9b-139">Allow task developers to request the exact set of privileges that their task requires.</span></span>

-   <span data-ttu-id="10f9b-140">Cambios de la API:</span><span class="sxs-lookup"><span data-stu-id="10f9b-140">API changes:</span></span>

    -   <span data-ttu-id="10f9b-141">Compatibilidad con la protección de la seguridad de tareas: la nueva característica de protección de la seguridad de tareas se presenta con la nueva interfaz IPrincipal2.</span><span class="sxs-lookup"><span data-stu-id="10f9b-141">Task security hardening support: new task security hardening feature is introduced with new IPrincipal2 interface.</span></span>
    -   <span data-ttu-id="10f9b-142">Se introdujeron dos nuevas configuraciones de tarea con la nueva interfaz ITaskSettings2.</span><span class="sxs-lookup"><span data-stu-id="10f9b-142">Introduced two new task settings with the new ITaskSettings2 interface.</span></span>

        -   <span data-ttu-id="10f9b-143">DisallowStartOnRemoteAppSession: el nuevo valor de DisallowStartOnRemoteAppSession puede rechazar un inicio de tarea si se desencadena en [las sesiones remotas integradas localmente (ferrocarril)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .</span><span class="sxs-lookup"><span data-stu-id="10f9b-143">DisallowStartOnRemoteAppSession: The new DisallowStartOnRemoteAppSession setting can reject a task start if triggered in [Remote Applications Integrated Locally (RAIL)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) sessions.</span></span>
        -   <span data-ttu-id="10f9b-144">UseUnifiedSchedulingEngine: el uso del valor de UseUnifiedSchedulingEngine proporciona un comportamiento cohesivo para tareas y servicios de Windows, ya que se administra de forma uniforme mediante un motor de programación común para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="10f9b-144">UseUnifiedSchedulingEngine: Using the UseUnifiedSchedulingEngine setting provides a cohesive behavior for Windows Tasks and Services because it is being managed in a uniform manner by a common system-wide scheduling engine.</span></span> <span data-ttu-id="10f9b-145">Aunque se recomienda usar un motor unificado, no es compatible con algunas de las características Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="10f9b-145">Although using a unified engine is recommended, it does not support some of the Task Scheduler features.</span></span> <span data-ttu-id="10f9b-146">Si la combinación de propiedades no permite la ejecución de la tarea en un motor unificado, se rechazará el registro de este.</span><span class="sxs-lookup"><span data-stu-id="10f9b-146">If the combination of properties will not allow running of the task under a unified engine, the registration of such will be rejected.</span></span>
        -   <span data-ttu-id="10f9b-147">Las características de la tarea que no son compatibles con el motor de programación unificado incluyen:</span><span class="sxs-lookup"><span data-stu-id="10f9b-147">The task features that are not supported by the unified scheduling engine include:</span></span>

            -   <span data-ttu-id="10f9b-148">Tipos de inicio de sesión:</span><span class="sxs-lookup"><span data-stu-id="10f9b-148">Logon types:</span></span>

                -   [<span data-ttu-id="10f9b-149">\_ \_ \_ contraseña o token interactivo \_ de inicio de sesión de \_ tareas</span><span class="sxs-lookup"><span data-stu-id="10f9b-149">TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD</span></span>](./taskschedulerschema-logontype-principaltype-element.md)

            -   <span data-ttu-id="10f9b-150">Directiva de varias instancias:</span><span class="sxs-lookup"><span data-stu-id="10f9b-150">Multiple instance policy:</span></span>

                -   [<span data-ttu-id="10f9b-151">**instancias de tarea \_ \_ detener \_ existentes**</span><span class="sxs-lookup"><span data-stu-id="10f9b-151">**TASK\_INSTANCES\_STOP\_EXISTING**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   <span data-ttu-id="10f9b-152">Acciones:</span><span class="sxs-lookup"><span data-stu-id="10f9b-152">Actions:</span></span>

                -   [<span data-ttu-id="10f9b-153">Enviar correo electrónico</span><span class="sxs-lookup"><span data-stu-id="10f9b-153">Send email</span></span>](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [<span data-ttu-id="10f9b-154">Mensaje para mostrar</span><span class="sxs-lookup"><span data-stu-id="10f9b-154">Display message</span></span>](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   <span data-ttu-id="10f9b-155">Configuración:</span><span class="sxs-lookup"><span data-stu-id="10f9b-155">Settings:</span></span>

                -   [<span data-ttu-id="10f9b-156">Configuración de red de tareas</span><span class="sxs-lookup"><span data-stu-id="10f9b-156">Task network settings</span></span>](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [<span data-ttu-id="10f9b-157">No permitir finalizar la tarea</span><span class="sxs-lookup"><span data-stu-id="10f9b-157">Do not allow task hard terminate</span></span>](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   <span data-ttu-id="10f9b-158">Desencadenadores:</span><span class="sxs-lookup"><span data-stu-id="10f9b-158">Triggers:</span></span>

                -   [<span data-ttu-id="10f9b-159">Límite de tiempo de ejecución del desencadenador</span><span class="sxs-lookup"><span data-stu-id="10f9b-159">Trigger execution time limit</span></span>](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [<span data-ttu-id="10f9b-160">Patrones de repetición para desencadenadores de calendario</span><span class="sxs-lookup"><span data-stu-id="10f9b-160">Repetition patterns for calendar triggers</span></span>]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [<span data-ttu-id="10f9b-161">Valores de consulta XPath para desencadenadores de eventos</span><span class="sxs-lookup"><span data-stu-id="10f9b-161">XPath query values for event triggers</span></span>]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   <span data-ttu-id="10f9b-162">Tipos de desencadenador [de día de la semana](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) [mensual](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) y mensual</span><span class="sxs-lookup"><span data-stu-id="10f9b-162">[Monthly](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) and [Monthly day-of-week](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) trigger types</span></span>

## <a name="windows-vista"></a><span data-ttu-id="10f9b-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10f9b-163">Windows Vista</span></span>

<span data-ttu-id="10f9b-164">La API Programador de tareas 2,0 se debe usar en el desarrollo de aplicaciones que usan el servicio Programador de tareas en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10f9b-164">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="10f9b-165">Para obtener más información, vea [referencia de programador de tareas](task-scheduler-reference.md) y [usar el programador de tareas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="10f9b-165">For more information, see [Task Scheduler Reference](task-scheduler-reference.md) and [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a><span data-ttu-id="10f9b-166">Windows 2000, Windows XP y Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10f9b-166">Windows 2000, Windows XP, and Windows Server 2003</span></span>

<span data-ttu-id="10f9b-167">La API Programador de tareas 2,0 no está disponible.</span><span class="sxs-lookup"><span data-stu-id="10f9b-167">The Task Scheduler 2.0 API is not available.</span></span> <span data-ttu-id="10f9b-168">Use Programador de tareas 1,0.</span><span class="sxs-lookup"><span data-stu-id="10f9b-168">Use Task Scheduler 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10f9b-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10f9b-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f9b-170">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="10f9b-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="10f9b-171">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="10f9b-171">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 
