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
# <a name="automatic-maintenance"></a>Mantenimiento automático

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

Windows depende de la ejecución de la bandeja de entrada y de la actividad de mantenimiento de terceros para gran parte de su valor de agregar, incluido Windows Update y desfragmentación automática de discos, así como las actualizaciones y los exámenes del antivirus. Además, las empresas suelen usar actividades de mantenimiento como el análisis de protección de acceso a redes (NAP) para ayudar a aplicar los estándares de seguridad en todas las estaciones de trabajo empresariales.

La actividad de mantenimiento en Windows está diseñada para ejecutarse en segundo plano con una interacción limitada del usuario y un impacto mínimo en el rendimiento y la eficacia energética. Sin embargo, en Windows 7 y versiones anteriores, el rendimiento y la eficacia energética todavía se ven afectados debido a la programación no determinista y ampliamente modificada de las diversas actividades de mantenimiento de Windows. La capacidad de respuesta a los usuarios se reduce cuando se ejecuta la actividad de mantenimiento mientras los usuarios están usando el equipo activamente. Las aplicaciones también solicitan al usuario que actualice su software y ejecuten el mantenimiento en segundo plano, y dirigen a los usuarios a varias experiencias, como el centro de actividades, el panel de control, Windows Update, Programador de tareas complemento MMC y controles de otros fabricantes.

El objetivo del mantenimiento automático es combinar toda la actividad de mantenimiento en segundo plano en Windows y ayudar a los desarrolladores de terceros a agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficacia energética. Además, el mantenimiento automático permite a los usuarios así como a las empresas controlar la programación y la configuración de la actividad de mantenimiento.

**Problemas principales**

El mantenimiento automático está diseñado para solucionar estos problemas con la actividad de mantenimiento en Windows:

-   Programación de fecha límite
-   Conflictos de uso de recursos
-   Eficiencia energética
-   Transparencia para el usuario

## <a name="functionality"></a>Funcionalidad

El mantenimiento automático facilita la eficiencia inactiva y permite que toda la actividad se ejecute de manera oportuna y con prioridad. También ayuda a habilitar la visibilidad unificada y el control de la actividad de mantenimiento, y permite a los desarrolladores de terceros agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficacia energética. Para ello, proporciona un modo totalmente automático, modo Iniciado por el usuario, detención automática, fechas límite y notificación, y control empresarial. Estos son los que se describen a continuación.

**Modo totalmente automático**

Este modo predeterminado permite la programación inteligente durante el tiempo de inactividad del equipo y a las horas programadas: la ejecución y la pausa automática de la actividad de mantenimiento sin intervención del usuario. El usuario puede establecer una programación semanal o diaria. Toda la actividad de mantenimiento no es interactiva y se ejecuta de forma silenciosa.

El equipo se reanuda automáticamente de la suspensión cuando no es probable que el sistema esté en uso, respetando la Directiva de administración de energía, que en el caso de los equipos portátiles, tiene como valor predeterminado permitir la reactivación solo si se encuentra en corriente alterna. Los recursos completos del sistema con alta potencia se usan para completar la actividad de mantenimiento lo más rápido posible. Si el sistema se reanudó de la suspensión para el mantenimiento automático, se solicita que vuelva a estar en suspensión.

Las interacciones de usuario requeridas relacionadas con actividades como la configuración se realizan fuera de la ejecución de mantenimiento automático.

**Modo Iniciado por el usuario**

Si los usuarios necesitan prepararse para viajar, esperan tener energía de batería durante un período prolongado o desean optimizar el rendimiento y la capacidad de respuesta, tienen la opción de iniciar el mantenimiento automático a petición. Los usuarios pueden configurar atributos de mantenimiento automático, incluida la programación de ejecución automática. Pueden ver el estado actual de la ejecución del mantenimiento automático y pueden detener el mantenimiento automático si es necesario.

**Detención automática**

El mantenimiento automático detiene automáticamente las actividades de mantenimiento que se están ejecutando en ese momento si el usuario comienza a interactuar con el equipo. La actividad de mantenimiento se reanudará cuando el sistema vuelva al estado inactivo.

> [!Note]  
> Todas las actividades del mantenimiento automático deben admitir la detención en 2 segundos o menos. Se debe notificar al usuario que la actividad se ha detenido.

 

**Fechas límite y notificación**

La actividad de mantenimiento crítico debe ejecutarse dentro de una ventana de tiempo predefinida. Si las tareas críticas no se han podido ejecutar en el momento especificado, el mantenimiento automático comenzará a ejecutarse automáticamente en la siguiente oportunidad inactiva del sistema disponible. Sin embargo, si el estado de la tarea permanece detrás de la fecha límite, el mantenimiento automático notificará al usuario acerca de la actividad y proporcionará una opción para una ejecución manual del mantenimiento automático. Se ejecutarán todas las tareas programadas para mantenimiento, aunque las tareas más deshabilitadas tienen prioridad. Esta actividad puede afectar al rendimiento y la capacidad de respuesta del sistema; por lo tanto, el mantenimiento automático notificará al usuario que se está ejecutando la actividad de mantenimiento crítica.

**Control empresarial**

Los profesionales de TI empresariales deben poder determinar cuándo se ejecuta el mantenimiento automático en sus sistemas Windows, aplicar esa programación a través de interfaces de administración estandarizadas y recuperar datos de eventos sobre el estado de los intentos de ejecución de mantenimiento automático. Además, los profesionales de TI deben poder invocar la actividad de mantenimiento automático específica de forma remota a través de las interfaces de administración estándar. Cada vez que se ejecuta el mantenimiento automático, los informes de estado, incluidas las notificaciones cuando no se pudo ejecutar el mantenimiento automático porque el usuario ha pausado manualmente la actividad, se ejecuta. Los profesionales de TI deben considerar la posibilidad de mover scripts de inicio de sesión al mantenimiento automático para facilitar la experiencia de inicio de sesión del usuario.

## <a name="creating-an-automatic-maintenance-task"></a>Creación de una tarea de mantenimiento automática

En esta sección se detalla cómo los desarrolladores pueden crear una tarea mediante una definición de tarea en lenguaje XML o C. Tenga en cuenta que la actividad de mantenimiento no debe iniciar ninguna interfaz de usuario que requiera la interacción del usuario, ya que el mantenimiento automático es completamente silencioso y se ejecuta cuando el usuario no está presente. En realidad, si el usuario interactúa con el equipo durante el mantenimiento automático, las tareas en curso se finalizarán hasta el siguiente período de inactividad.

**Usar XML**

Programador de tareas incluye una herramienta de línea de comandos integrada, schtasks.exe, que puede importar una definición de tarea en formato XML. El esquema de la definición de la tarea se documenta en https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . A continuación se muestra un ejemplo de una tarea de mantenimiento automática definida en XML.


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



Para guardar la tarea en un equipo Windows, guarde el código XML anterior como un archivo de texto y use esta línea de comandos:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Usar C**

También se puede crear una tarea de mantenimiento automática mediante código C. A continuación se muestra un ejemplo de código que se puede usar para configurar las opciones de mantenimiento automático de una tarea:


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



## <a name="validating-tasks"></a>Validación de tareas

Compruebe que la tarea se ha creado correctamente y se ejecuta como parte del mantenimiento.

**Validación de la creación de tareas**

Use esta línea de comandos para exportar la definición de la tarea a un archivo y asegurarse de que la definición de la tarea es la esperada:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Validación de la ejecución de tareas**

Ejecute esta línea de comandos para iniciar la tarea y validar que la interfaz de usuario de Programador de tareas (taskschd. msc) muestra que la tarea se ha ejecutado:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Recursos

-   [Programación de tareas 2,0](/previous-versions/bb756979(v=msdn.10))

 

 