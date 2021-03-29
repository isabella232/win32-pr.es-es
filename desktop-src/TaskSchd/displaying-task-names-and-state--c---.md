---
title: Mostrar nombres de tarea y Estados (C++)
description: En estos dos ejemplos de C++ se muestra cómo enumerar tareas. En un ejemplo se muestra cómo mostrar la información de las tareas en una carpeta de tareas y los otros ejemplos muestran cómo Mostrar información de todas las tareas en ejecución.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6189960ef5b6e4ad78e75f156a482481f347b4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779819"
---
# <a name="displaying-task-names-and-states-c"></a>Mostrar nombres de tarea y Estados (C++)

En estos dos ejemplos de C++ se muestra cómo enumerar tareas. En un ejemplo se muestra cómo mostrar la información de las tareas en una carpeta de tareas y los otros ejemplos muestran cómo Mostrar información de todas las tareas en ejecución.

En el procedimiento siguiente se describe cómo mostrar los nombres de tarea y el estado de todas las tareas de una carpeta de tareas.

**Para mostrar los nombres de tarea y el estado de todas las tareas de una carpeta de tareas**

1.  Inicialice COM y establezca la seguridad COM general.
2.  Cree el objeto [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

    Este objeto le permite conectarse al servicio Programador de tareas y obtener acceso a una carpeta de tareas específica.

3.  Obtenga una carpeta de tareas que contenga las tareas sobre las que desea obtener información.

    Use el método [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) para obtener la carpeta.

4.  Obtiene la colección de tareas de la carpeta.

    Use el método [**ITaskFolder:: GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) para obtener la colección de tareas ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).

5.  Obtiene el número de tareas de la colección y enumera cada tarea de la colección.

    Use la [**propiedad Item de IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) para obtener una instancia de [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) . Cada instancia contendrá una tarea en la colección. A continuación, puede mostrar la información (valores de propiedad) de cada tarea registrada.

En el siguiente ejemplo de C++ se muestra cómo mostrar el nombre y el estado de todas las tareas en la carpeta de tareas raíz.


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
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
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



En el procedimiento siguiente se describe cómo mostrar los nombres de tarea y el estado de todas las tareas en ejecución.

**Para mostrar los nombres de tarea y el estado de todas las tareas en ejecución**

1.  Inicialice COM y establezca la seguridad COM general.
2.  Cree el objeto [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

    Este objeto le permite conectarse al servicio Programador de tareas y obtener acceso a una carpeta de tareas específica.

3.  Use el método [**ITaskService:: GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) para obtener una colección de todas las tareas en ejecución ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)). Puede especificar para obtener instancias de la tarea en ejecución, incluyendo o excluyendo tareas ocultas.
4.  Obtiene el número de tareas de la colección y enumera cada tarea de la colección.

    Use la [**propiedad Item de IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) para obtener una instancia de [**IRunningTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) . Cada instancia contendrá una tarea en la colección. A continuación, puede mostrar la información (valores de propiedad) de cada tarea registrada.

En el siguiente ejemplo de C++ se muestra cómo mostrar el nombre y el estado de todas las tareas en ejecución, incluidas las tareas ocultas.


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
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
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el Programador de tareas](using-the-task-scheduler.md)
</dt> </dl>

 

 




