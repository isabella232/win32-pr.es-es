---
title: Ejemplo de código de C/C++ que recupera el tiempo de espera de inactividad de tarea
description: En este ejemplo se recupera el tiempo de espera de inactividad de la tarea y se muestra en la pantalla. En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.
ms.assetid: 2784b925-678c-422c-ae78-84d2982c2b02
keywords:
- recuperando el tiempo de espera de inactividad de la tarea Programador de tareas
- recuperar propiedades de elementos de trabajo Programador de tareas, tiempo de espera de inactividad de la tarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c109faf55be8039c2c39652f8c513b6b38bd17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357133"
---
# <a name="cc-code-example-retrieving-task-idle-wait-time"></a><span data-ttu-id="a2d10-106">Ejemplo de código de C/C++: recuperar el tiempo de espera de inactividad de la tarea</span><span class="sxs-lookup"><span data-stu-id="a2d10-106">C/C++ Code Example: Retrieving Task Idle-wait Time</span></span>

<span data-ttu-id="a2d10-107">En este ejemplo se recupera el tiempo de espera de inactividad de la tarea y se muestra en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a2d10-107">This example retrieves the idle-wait time of the task and displays it on the screen.</span></span> <span data-ttu-id="a2d10-108">En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="a2d10-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  ITaskScheduler *pITS;
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetIdleWait. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  WORD pwIdleMinutes;
  WORD pwDeadlineMinutes;
  
  hr = pITask->GetIdleWait(&pwIdleMinutes,
                           &pwDeadlineMinutes);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetIdleWait: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The idle wait of Test Task is: \n");
  wprintf(L" %d minutes\n", pwIdleMinutes);
  wprintf(L" %d minutes\n", pwDeadlineMinutes);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="a2d10-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2d10-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d10-110">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="a2d10-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




