---
title: Ejemplo de código de C/C++ finalización de una tarea
description: En este ejemplo se comprueba el estado de una tarea conocida y finaliza la tarea si se está ejecutando.
ms.assetid: 2131b966-6179-4a80-a3f1-ebb8967a7a90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ea8adf901d417db13eb8c4f840acf0f283d3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676129"
---
# <a name="cc-code-example-terminating-a-task"></a><span data-ttu-id="5d862-103">Ejemplo de código de C/C++: finalizar una tarea</span><span class="sxs-lookup"><span data-stu-id="5d862-103">C/C++ Code Example: Terminating a Task</span></span>

<span data-ttu-id="5d862-104">En este ejemplo se comprueba el estado de una tarea conocida y finaliza la tarea si se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5d862-104">This example verifies the status of a known task and terminates the task if it is running.</span></span>


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
  
  //Release ITaskScheduler interface.
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
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Terminate if the status is SCHED_S_TASK_RUNNING.
  ///////////////////////////////////////////////////////////////////
  
  if(phrStatus==SCHED_S_TASK_RUNNING)
  {
    hr = pITask->Terminate();
    if (FAILED(hr))
    {
      wprintf(L"Failed calling ITask::Terminate: ");
      wprintf(L"error = 0x%x\n",hr);
      pITask->Release();
      CoUninitialize();
      return 1;
    }
  wprintf(L"Test Task is terminated.\n");
  }
  else
  {
    wprintf(L"Test Task is not running.\n");
  }

  // Release the ITask interface.
  pITask->Release();
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="5d862-105">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d862-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d862-106">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="5d862-106">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




