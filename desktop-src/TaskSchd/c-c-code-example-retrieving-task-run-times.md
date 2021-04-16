---
title: Ejemplo de código de C/C++ que recupera los tiempos de ejecución de la tarea
description: En este ejemplo se recuperan los tiempos de ejecución de la tarea y se muestran en la pantalla. En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.
ms.assetid: ad9eb4a7-f42b-4f5a-86a3-05d02dc88f97
keywords:
- recuperando los tiempos de ejecución de la tarea Programador de tareas
- recuperar propiedades de elementos de trabajo Programador de tareas, tiempos de ejecución de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e9c826735cf6cfc84725d577bc8b9bc07badcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685600"
---
# <a name="cc-code-example-retrieving-task-run-times"></a><span data-ttu-id="eabf3-106">Ejemplo de código de C/C++: recuperar los tiempos de ejecución de la tarea</span><span class="sxs-lookup"><span data-stu-id="eabf3-106">C/C++ Code Example: Retrieving Task Run Times</span></span>

<span data-ttu-id="eabf3-107">En este ejemplo se recuperan los tiempos de ejecución de la tarea y se muestran en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="eabf3-107">This example retrieves the run times of the task and displays them on the screen.</span></span> <span data-ttu-id="eabf3-108">En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="eabf3-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


```C++
#include <windows.h>
#include <wchar.h>
#include <stdio.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>


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
  // Call ITaskScheduler::Activate to get the task object.
  ///////////////////////////////////////////////////////////////////
  ITask *pITask;
  LPCWSTR lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  // Release the ITaskScheduler interface.
  pITS->Release();

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetRunTimes and display the next five run times for 
  // this task.
  ///////////////////////////////////////////////////////////////////
  
  SYSTEMTIME stNow;
  LPSYSTEMTIME pstListOfTimes;
  LPSYSTEMTIME pstListBegin;
  WORD wCountOfRuns = 5;
  
  GetSystemTime(&stNow);
  hr = pITask->GetRunTimes(&stNow,
                           NULL,
                           &wCountOfRuns,
                           &pstListBegin);
  pstListOfTimes = pstListBegin;
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling GetRunTimes: ");
    wprintf(L"error = 0x%x\n", hr);
    CoUninitialize();
    return 1;
  }
  
  wprintf(L"The next %u runtimes for this task are: \n",wCountOfRuns);
  
  for (WORD i = 0; i < wCountOfRuns; i++)
  {
    wprintf(L"\t%u - %u/%u/%u \t %u:%u\n", i+1, pstListOfTimes->wMonth,
                                                pstListOfTimes->wDay,
                                                pstListOfTimes->wYear,
                                                pstListOfTimes->wHour,
                                                pstListOfTimes->wMinute);
    pstListOfTimes++;
  }

  CoTaskMemFree(pstListBegin);
  CoTaskMemFree(pstListOfTimes);
  CoUninitialize();

  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="eabf3-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eabf3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eabf3-110">Ejemplos de Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="eabf3-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




