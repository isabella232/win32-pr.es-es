---
title: Mantenimiento automático (Guía de compatibilidad para Windows)
description: Mantenimiento automático
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a839191d84f3f20fcc598b42433c888b090b2b174dd6891c0b5b9fc72f0af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028873"
---
# <a name="automatic-maintenance"></a>Mantenimiento automático

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

Windows depende de la ejecución de la actividad de mantenimiento de la bandeja de entrada y de terceros durante gran parte de su valor agregado, incluida la actualización de Windows y la desfragmentación automática del disco, así como de las actualizaciones y exámenes antivirus. Además, las empresas suelen usar la actividad de mantenimiento, como el examen de protección de acceso a redes (NAP) para ayudar a aplicar estándares de seguridad en todas las estaciones de trabajo empresariales.

La actividad de mantenimiento Windows está diseñada para ejecutarse en segundo plano con una interacción limitada del usuario y un impacto mínimo en el rendimiento y la eficiencia energética. Sin embargo, en Windows 7 y versiones anteriores, el rendimiento y la eficiencia energética todavía se ven afectados debido a la programación no determinista y ampliamente variada de las diversas actividades de mantenimiento en Windows. La capacidad de respuesta a los usuarios se reduce cuando se ejecuta la actividad de mantenimiento mientras los usuarios usan activamente el equipo. Las aplicaciones también suelen pedir al usuario que actualice su software y ejecute el mantenimiento en segundo plano, así como dirigir a los usuarios a varias experiencias, incluidos el Centro de acciones, Panel de control, Windows Update Programador de tareas, un complemento MMC y controles de terceros.

El objetivo de Mantenimiento automático es combinar toda la actividad de mantenimiento en segundo plano en Windows y ayudar a los desarrolladores de terceros a agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficiencia energética. Además, Mantenimiento automático permite a los usuarios y a las empresas controlar la programación y configuración de la actividad de mantenimiento.

**Problemas clave**

Mantenimiento automático está diseñado para solucionar estos problemas con la actividad de mantenimiento en Windows:

-   Programación de fecha límite
-   Conflictos de uso de recursos
-   Eficiencia energética
-   Transparencia para el usuario

## <a name="functionality"></a>Funcionalidad

Mantenimiento automático facilita la eficacia inactiva y permite que toda la actividad se ejecute de forma oportuna y prioritaria. También ayuda a habilitar la visibilidad unificada y el control sobre la actividad de mantenimiento, y permite a los desarrolladores de terceros agregar su actividad de mantenimiento a Windows sin afectar negativamente al rendimiento y la eficiencia energética. Para ello, proporciona un modo totalmente automático, el modo iniciado por el usuario, la detección automática, las fechas límite y la notificación, y el control empresarial. Cada uno de ellos se describe a continuación.

**Modo totalmente automático**

Este modo predeterminado permite la programación inteligente durante el tiempo de inactividad del equipo y en horas programadas: la ejecución y la pausa automática de la actividad de mantenimiento sin intervención del usuario. El usuario puede establecer una programación semanal o diaria. Toda la actividad de mantenimiento no es interactiva y se ejecuta en modo silencioso.

El equipo se reanuda automáticamente de suspensión cuando es probable que el sistema no esté en uso, respetando la directiva de administración de energía, que en el caso de los equipos portátiles, permite de forma predeterminada la reactivación solo si está en alimentación de ca. Los recursos completos del sistema a gran potencia se usan para completar la actividad de mantenimiento lo antes posible. Si el sistema se reanudó de suspensión durante Mantenimiento automático, se solicita que vuelva a suspensión.

Las interacciones de usuario necesarias relacionadas con actividades como la configuración se realizan fuera de Mantenimiento automático ejecución.

**Modo iniciado por el usuario**

Si los usuarios necesitan prepararse para el viaje, esperar estar encendidos durante un tiempo prolongado o desean optimizar el rendimiento y la capacidad de respuesta, tienen la opción de iniciar Mantenimiento automático a petición. Los usuarios pueden configurar Mantenimiento automático, incluida la programación de ejecución automática. Pueden ver el estado actual de Mantenimiento automático ejecución y pueden detener Mantenimiento automático si es necesario.

**Detección automática**

Mantenimiento automático detiene automáticamente las actividades de mantenimiento que se están ejecutando actualmente si el usuario comienza a interactuar con el equipo. La actividad de mantenimiento se reanudará cuando el sistema vuelva al estado de inactividad.

> [!Note]  
> Todas las actividades de Mantenimiento automático deben admitir la detención en 2 segundos o menos. Se debe notificar al usuario que la actividad se ha detenido.

 

**Fechas límite y notificación**

La actividad de mantenimiento crítico debe ejecutarse dentro de un período de tiempo predefinido. Si las tareas críticas no se han podido ejecutar dentro de su tiempo designado, Mantenimiento automático se iniciará automáticamente la ejecución en la siguiente oportunidad de inactividad del sistema disponible. Sin embargo, si el estado de la tarea sigue estando por detrás de la fecha límite, Mantenimiento automático notificará al usuario sobre la actividad y proporcionará una opción para una ejecución manual de Mantenimiento automático. Todas las tareas programadas para mantenimiento se ejecutarán, aunque las tareas más hadas tienen prioridad. Esta actividad puede afectar a la capacidad de respuesta y el rendimiento del sistema; por lo tanto, Mantenimiento automático notificará al usuario que se está ejecutando una actividad de mantenimiento crítica.

**Enterprise control**

Enterprise Los profesionales de TI deben ser capaces de determinar cuándo Mantenimiento automático se ejecuta en sus sistemas Windows, aplicar esa programación a través de interfaces de administración estandarizadas y recuperar datos de eventos sobre el estado de los intentos de Mantenimiento automático ejecución. Además, los profesionales de IT deben poder invocar actividades específicas Mantenimiento automático remotamente a través de interfaces de administración estándar. Cada vez Mantenimiento automático, se ejecutan informes de estado, incluidas las notificaciones Mantenimiento automático no se pudieron ejecutar porque el usuario ha pausado manualmente la actividad. Los profesionales de IT deben considerar la posibilidad de mover scripts de Mantenimiento automático para ayudar a que la experiencia de inicio de sesión del usuario sea más rápida.

## <a name="creating-an-automatic-maintenance-task"></a>Creación de una Mantenimiento automático trabajo

En esta sección se detalla cómo los desarrolladores pueden crear una tarea mediante una definición de tarea en lenguaje XML o C. Tenga en cuenta que la actividad de mantenimiento no debe iniciar ninguna interfaz de usuario que requiera la interacción del usuario, ya que Mantenimiento automático es completamente silenciosa y se ejecuta cuando el usuario no está presente. De hecho, si el usuario interactúa con el equipo durante Mantenimiento automático, las tareas en proceso finalizarán hasta el siguiente período de inactividad.

**Uso de XML**

Programador de tareas incluye una herramienta de línea de comandos integrada, schtasks.exe, que puede importar una definición de tarea en formato XML. El esquema de la definición de tarea se documenta en https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . A continuación se muestra un ejemplo de Mantenimiento automático tarea definida en XML.


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



Para guardar la tarea en un Windows, guarde el XML anterior como un archivo de texto y use esta línea de comandos:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Uso de C**

También Mantenimiento automático tarea de creación mediante código C. A continuación se muestra un ejemplo de código que se puede usar para configurar la configuración de Mantenimiento automático tarea:


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

Use esta línea de comandos para exportar la definición de tarea a un archivo y asegurarse de que la definición de tarea es la esperada:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Validación de la ejecución de tareas**

Ejecute esta línea de comandos para iniciar la tarea y compruebe que Programador de tareas interfaz de usuario (taskschd.msc) muestra que la tarea se ha ejecutado:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Recursos

-   [Programación de tareas 2.0](/previous-versions/bb756979(v=msdn.10))

 

 