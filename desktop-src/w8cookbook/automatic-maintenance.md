---
title: Mantenimiento automático (guías de compatibilidad para Windows)
description: Mantenimiento automático
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488414"
---
# <a name="automatic-maintenance"></a><span data-ttu-id="c2b93-103">Mantenimiento automático</span><span class="sxs-lookup"><span data-stu-id="c2b93-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="c2b93-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="c2b93-104">Platforms</span></span>

<span data-ttu-id="c2b93-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="c2b93-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="c2b93-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2b93-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="c2b93-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2b93-107">Description</span></span>

<span data-ttu-id="c2b93-108">Windows depende de la ejecución de la bandeja de entrada y de la actividad de mantenimiento de terceros para gran parte de su valor de agregar, incluido Windows Update y desfragmentación automática de discos, así como las actualizaciones y los exámenes del antivirus.</span><span class="sxs-lookup"><span data-stu-id="c2b93-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="c2b93-109">Además, las empresas suelen usar actividades de mantenimiento como el análisis de protección de acceso a redes (NAP) para ayudar a aplicar los estándares de seguridad en todas las estaciones de trabajo empresariales.</span><span class="sxs-lookup"><span data-stu-id="c2b93-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="c2b93-110">La actividad de mantenimiento en Windows está diseñada para ejecutarse en segundo plano con una interacción limitada del usuario y un impacto mínimo en el rendimiento y la eficacia energética.</span><span class="sxs-lookup"><span data-stu-id="c2b93-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="c2b93-111">Sin embargo, en Windows 7 y versiones anteriores, el rendimiento y la eficacia energética todavía se ven afectados debido a la programación no determinista y ampliamente modificada de las diversas actividades de mantenimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b93-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="c2b93-112">La capacidad de respuesta a los usuarios se reduce cuando se ejecuta la actividad de mantenimiento mientras los usuarios están usando el equipo activamente.</span><span class="sxs-lookup"><span data-stu-id="c2b93-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="c2b93-113">Las aplicaciones también solicitan al usuario que actualice su software y ejecuten el mantenimiento en segundo plano, y dirigen a los usuarios a varias experiencias, como el centro de actividades, el panel de control, Windows Update, Programador de tareas complemento MMC y controles de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="c2b93-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="c2b93-114">El objetivo del mantenimiento automático es combinar toda la actividad de mantenimiento en segundo plano en Windows y ayudar a los desarrolladores de terceros a agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficacia energética.</span><span class="sxs-lookup"><span data-stu-id="c2b93-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="c2b93-115">Además, el mantenimiento automático permite a los usuarios así como a las empresas controlar la programación y la configuración de la actividad de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="c2b93-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="c2b93-116">**Problemas principales**</span><span class="sxs-lookup"><span data-stu-id="c2b93-116">**Key problems**</span></span>

<span data-ttu-id="c2b93-117">El mantenimiento automático está diseñado para solucionar estos problemas con la actividad de mantenimiento en Windows:</span><span class="sxs-lookup"><span data-stu-id="c2b93-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="c2b93-118">Programación de fecha límite</span><span class="sxs-lookup"><span data-stu-id="c2b93-118">Deadline scheduling</span></span>
-   <span data-ttu-id="c2b93-119">Conflictos de uso de recursos</span><span class="sxs-lookup"><span data-stu-id="c2b93-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="c2b93-120">Eficiencia energética</span><span class="sxs-lookup"><span data-stu-id="c2b93-120">Energy efficiency</span></span>
-   <span data-ttu-id="c2b93-121">Transparencia para el usuario</span><span class="sxs-lookup"><span data-stu-id="c2b93-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="c2b93-122">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="c2b93-122">Functionality</span></span>

<span data-ttu-id="c2b93-123">El mantenimiento automático facilita la eficiencia inactiva y permite que toda la actividad se ejecute de manera oportuna y con prioridad.</span><span class="sxs-lookup"><span data-stu-id="c2b93-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="c2b93-124">También ayuda a habilitar la visibilidad unificada y el control de la actividad de mantenimiento, y permite a los desarrolladores de terceros agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficacia energética.</span><span class="sxs-lookup"><span data-stu-id="c2b93-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="c2b93-125">Para ello, proporciona un modo totalmente automático, modo Iniciado por el usuario, detención automática, fechas límite y notificación, y control empresarial.</span><span class="sxs-lookup"><span data-stu-id="c2b93-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="c2b93-126">Estos son los que se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="c2b93-126">These are each described below.</span></span>

<span data-ttu-id="c2b93-127">**Modo totalmente automático**</span><span class="sxs-lookup"><span data-stu-id="c2b93-127">**Fully automatic mode**</span></span>

<span data-ttu-id="c2b93-128">Este modo predeterminado permite la programación inteligente durante el tiempo de inactividad del equipo y a las horas programadas: la ejecución y la pausa automática de la actividad de mantenimiento sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2b93-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="c2b93-129">El usuario puede establecer una programación semanal o diaria.</span><span class="sxs-lookup"><span data-stu-id="c2b93-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="c2b93-130">Toda la actividad de mantenimiento no es interactiva y se ejecuta de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="c2b93-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="c2b93-131">El equipo se reanuda automáticamente de la suspensión cuando no es probable que el sistema esté en uso, respetando la Directiva de administración de energía, que en el caso de los equipos portátiles, tiene como valor predeterminado permitir la reactivación solo si se encuentra en corriente alterna.</span><span class="sxs-lookup"><span data-stu-id="c2b93-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="c2b93-132">Los recursos completos del sistema con alta potencia se usan para completar la actividad de mantenimiento lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="c2b93-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="c2b93-133">Si el sistema se reanudó de la suspensión para el mantenimiento automático, se solicita que vuelva a estar en suspensión.</span><span class="sxs-lookup"><span data-stu-id="c2b93-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="c2b93-134">Las interacciones de usuario requeridas relacionadas con actividades como la configuración se realizan fuera de la ejecución de mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="c2b93-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="c2b93-135">**Modo Iniciado por el usuario**</span><span class="sxs-lookup"><span data-stu-id="c2b93-135">**User-initiated mode**</span></span>

<span data-ttu-id="c2b93-136">Si los usuarios necesitan prepararse para viajar, esperan tener energía de batería durante un período prolongado o desean optimizar el rendimiento y la capacidad de respuesta, tienen la opción de iniciar el mantenimiento automático a petición.</span><span class="sxs-lookup"><span data-stu-id="c2b93-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="c2b93-137">Los usuarios pueden configurar atributos de mantenimiento automático, incluida la programación de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="c2b93-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="c2b93-138">Pueden ver el estado actual de la ejecución del mantenimiento automático y pueden detener el mantenimiento automático si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c2b93-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="c2b93-139">**Detención automática**</span><span class="sxs-lookup"><span data-stu-id="c2b93-139">**Automatic stop**</span></span>

<span data-ttu-id="c2b93-140">El mantenimiento automático detiene automáticamente las actividades de mantenimiento que se están ejecutando en ese momento si el usuario comienza a interactuar con el equipo.</span><span class="sxs-lookup"><span data-stu-id="c2b93-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="c2b93-141">La actividad de mantenimiento se reanudará cuando el sistema vuelva al estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="c2b93-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="c2b93-142">Todas las actividades del mantenimiento automático deben admitir la detención en 2 segundos o menos.</span><span class="sxs-lookup"><span data-stu-id="c2b93-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="c2b93-143">Se debe notificar al usuario que la actividad se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="c2b93-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="c2b93-144">**Fechas límite y notificación**</span><span class="sxs-lookup"><span data-stu-id="c2b93-144">**Deadlines and notification**</span></span>

<span data-ttu-id="c2b93-145">La actividad de mantenimiento crítico debe ejecutarse dentro de una ventana de tiempo predefinida.</span><span class="sxs-lookup"><span data-stu-id="c2b93-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="c2b93-146">Si las tareas críticas no se han podido ejecutar en el momento especificado, el mantenimiento automático comenzará a ejecutarse automáticamente en la siguiente oportunidad inactiva del sistema disponible.</span><span class="sxs-lookup"><span data-stu-id="c2b93-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="c2b93-147">Sin embargo, si el estado de la tarea permanece detrás de la fecha límite, el mantenimiento automático notificará al usuario acerca de la actividad y proporcionará una opción para una ejecución manual del mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="c2b93-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="c2b93-148">Se ejecutarán todas las tareas programadas para mantenimiento, aunque las tareas más deshabilitadas tienen prioridad.</span><span class="sxs-lookup"><span data-stu-id="c2b93-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="c2b93-149">Esta actividad puede afectar al rendimiento y la capacidad de respuesta del sistema; por lo tanto, el mantenimiento automático notificará al usuario que se está ejecutando la actividad de mantenimiento crítica.</span><span class="sxs-lookup"><span data-stu-id="c2b93-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="c2b93-150">**Control empresarial**</span><span class="sxs-lookup"><span data-stu-id="c2b93-150">**Enterprise control**</span></span>

<span data-ttu-id="c2b93-151">Los profesionales de TI empresariales deben poder determinar cuándo se ejecuta el mantenimiento automático en sus sistemas Windows, aplicar esa programación a través de interfaces de administración estandarizadas y recuperar datos de eventos sobre el estado de los intentos de ejecución de mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="c2b93-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="c2b93-152">Además, los profesionales de TI deben poder invocar la actividad de mantenimiento automático específica de forma remota a través de las interfaces de administración estándar.</span><span class="sxs-lookup"><span data-stu-id="c2b93-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="c2b93-153">Cada vez que se ejecuta el mantenimiento automático, los informes de estado, incluidas las notificaciones cuando no se pudo ejecutar el mantenimiento automático porque el usuario ha pausado manualmente la actividad, se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="c2b93-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="c2b93-154">Los profesionales de TI deben considerar la posibilidad de mover scripts de inicio de sesión al mantenimiento automático para facilitar la experiencia de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="c2b93-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="c2b93-155">Creación de una tarea de mantenimiento automática</span><span class="sxs-lookup"><span data-stu-id="c2b93-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="c2b93-156">En esta sección se detalla cómo los desarrolladores pueden crear una tarea mediante una definición de tarea en lenguaje XML o C.</span><span class="sxs-lookup"><span data-stu-id="c2b93-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="c2b93-157">Tenga en cuenta que la actividad de mantenimiento no debe iniciar ninguna interfaz de usuario que requiera la interacción del usuario, ya que el mantenimiento automático es completamente silencioso y se ejecuta cuando el usuario no está presente.</span><span class="sxs-lookup"><span data-stu-id="c2b93-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="c2b93-158">En realidad, si el usuario interactúa con el equipo durante el mantenimiento automático, las tareas en curso se finalizarán hasta el siguiente período de inactividad.</span><span class="sxs-lookup"><span data-stu-id="c2b93-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="c2b93-159">**Usar XML**</span><span class="sxs-lookup"><span data-stu-id="c2b93-159">**Using XML**</span></span>

<span data-ttu-id="c2b93-160">Programador de tareas incluye una herramienta de línea de comandos integrada, schtasks.exe, que puede importar una definición de tarea en formato XML.</span><span class="sxs-lookup"><span data-stu-id="c2b93-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="c2b93-161">El esquema de la definición de la tarea se documenta en https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="c2b93-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="c2b93-162">A continuación se muestra un ejemplo de una tarea de mantenimiento automática definida en XML.</span><span class="sxs-lookup"><span data-stu-id="c2b93-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



<span data-ttu-id="c2b93-163">Para guardar la tarea en un equipo Windows, guarde el código XML anterior como un archivo de texto y use esta línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="c2b93-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="c2b93-164">**Usar C**</span><span class="sxs-lookup"><span data-stu-id="c2b93-164">**Using C**</span></span>

<span data-ttu-id="c2b93-165">También se puede crear una tarea de mantenimiento automática mediante código C.</span><span class="sxs-lookup"><span data-stu-id="c2b93-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="c2b93-166">A continuación se muestra un ejemplo de código que se puede usar para configurar las opciones de mantenimiento automático de una tarea:</span><span class="sxs-lookup"><span data-stu-id="c2b93-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a><span data-ttu-id="c2b93-167">Validación de tareas</span><span class="sxs-lookup"><span data-stu-id="c2b93-167">Validating tasks</span></span>

<span data-ttu-id="c2b93-168">Compruebe que la tarea se ha creado correctamente y se ejecuta como parte del mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="c2b93-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="c2b93-169">**Validación de la creación de tareas**</span><span class="sxs-lookup"><span data-stu-id="c2b93-169">**Validating task creation**</span></span>

<span data-ttu-id="c2b93-170">Use esta línea de comandos para exportar la definición de la tarea a un archivo y asegurarse de que la definición de la tarea es la esperada:</span><span class="sxs-lookup"><span data-stu-id="c2b93-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="c2b93-171">**Validación de la ejecución de tareas**</span><span class="sxs-lookup"><span data-stu-id="c2b93-171">**Validating task execution**</span></span>

<span data-ttu-id="c2b93-172">Ejecute esta línea de comandos para iniciar la tarea y validar que la interfaz de usuario de Programador de tareas (taskschd. msc) muestra que la tarea se ha ejecutado:</span><span class="sxs-lookup"><span data-stu-id="c2b93-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="c2b93-173">Recursos</span><span class="sxs-lookup"><span data-stu-id="c2b93-173">Resources</span></span>

-   <span data-ttu-id="c2b93-174">[Programación de tareas 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c2b93-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 