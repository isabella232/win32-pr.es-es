---
title: Ejemplo de código de C/C++ editar un elemento de trabajo
description: Este ejemplo muestra las páginas de propiedades de una tarea conocida y permite al usuario editar las propiedades del elemento de trabajo. En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.
ms.assetid: 526bc354-3585-43aa-a727-03c04e607a64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec02a7b7b12f350e7ed61220c9bdeebe920fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075734"
---
# <a name="cc-code-example-editing-a-work-item"></a>Ejemplo de código de C/C++: editar un elemento de trabajo

Este ejemplo muestra las páginas de propiedades de una tarea conocida y permite al usuario editar las propiedades del elemento de trabajo. En este ejemplo se da por supuesto que la tarea y la tarea de prueba ya existen en el equipo local.


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
  
  //Release ITaskScheduler interface
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate, ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::EditWorkItem. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HWND hParent = NULL;
  DWORD dwReserved = 0;
  
  hr = pITask->EditWorkItem(hParent,
                            dwReserved);
  // Release ITask interface
  pITask->Release();
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::EditWorkItem, ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




