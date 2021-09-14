---
title: Ejemplo de código de C/C++ creación de una tarea mediante NewWorkItem
description: En este ejemplo se crea una sola tarea.
ms.assetid: a96bae5d-fa36-41ab-8baf-144683fc6b52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8573c5d5d097bdbe58c14329a5029046eecfae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068670"
---
# <a name="cc-code-example-creating-a-task-using-newworkitem"></a>Ejemplo de código de C/C++: Crear una tarea mediante NewWorkItem

En este ejemplo se crea una sola tarea.


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <objidl.h>
#include <wchar.h>
#include <stdio.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  /////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then 
  // call CoCreateInstance to get the Task Scheduler object. 
  /////////////////////////////////////////////////////////////////
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
  
  
  /////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::NewWorkItem to create new task.
  /////////////////////////////////////////////////////////////////
  LPCWSTR pwszTaskName;
  ITask *pITask;
  IPersistFile *pIPersistFile;
  pwszTaskName = L"Test Task";
  
  hr = pITS->NewWorkItem(pwszTaskName,         // Name of task
                         CLSID_CTask,          // Class identifier 
                         IID_ITask,            // Interface identifier
                         (IUnknown**)&pITask); // Address of task 
                                                                                                                                                                                            //  interface
  
  
  pITS->Release();                               // Release object
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling NewWorkItem, error = 0x%x\n",hr);
     return 1;
  }
  
  
  /////////////////////////////////////////////////////////////////
  // Call IUnknown::QueryInterface to get a pointer to 
  // IPersistFile and IPersistFile::Save to save 
  // the new task to disk.
  /////////////////////////////////////////////////////////////////
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  pITask->Release();
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling QueryInterface, error = 0x%x\n",hr);
     return 1;
  }
  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  pIPersistFile->Release();
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling Save, error = 0x%x\n",hr);
     return 1;
  }
  
  
  CoUninitialize();
  printf("Created task.\n");
  return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




