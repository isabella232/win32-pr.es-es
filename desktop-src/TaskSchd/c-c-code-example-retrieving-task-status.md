---
title: Ejemplo de código de C/C++ para recuperar el estado de la tarea
description: En este ejemplo se recupera el estado actual de la tarea y se muestra en la pantalla. En este ejemplo se supone que la tarea y la tarea de prueba ya existen en el equipo local.
ms.assetid: 7ad40ac7-2363-481a-87fa-18dcf2d749b3
keywords:
- recuperar el estado de la tarea Programador de tareas
- recuperar propiedades de elemento de trabajo Programador de tareas , estado de la tarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626b3e169e51deca34b8a8e4795671998e482a2640d2f222e2b734f69c5d2eb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060253"
---
# <a name="cc-code-example-retrieving-task-status"></a>Ejemplo de código de C/C++: Recuperar el estado de la tarea

En este ejemplo se recupera el estado actual de la tarea y se muestra en la pantalla. En este ejemplo se supone que la tarea y la tarea de prueba ya existen en el equipo local.


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
  // Call ITask::GetStatus. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HRESULT phrStatus;
  
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The status of Test Task is: ");
  
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;
  case SCHED_S_TASK_DISABLED:
       wprintf(L"  SCHED_S_TASK_DISABLED\n");
       break;
  case SCHED_S_TASK_HAS_NOT_RUN:
       wprintf(L"  SCHED_S_TASK_HAS_NOT_RUN\n");
       break;
  case SCHED_S_TASK_NOT_SCHEDULED:
       wprintf(L"  SCHED_S_TASK_NOT_SCHEDULED\n");
       break;
  case SCHED_S_TASK_NO_MORE_RUNS:
       wprintf(L"  SCHED_S_TASK_NO_MORE_RUNS\n");
       break;
  case SCHED_S_TASK_NO_VALID_TRIGGERS:
       wprintf(L"  SCHED_S_TASK_NO_VALID_TRIGGERS\n");
       break;
  default:
       wprintf(L"  unknown status flag!\n"); 
  }
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




