---
title: Directorio de trabajo de configuración de ejemplo de código de C/C++
description: En este ejemplo se establece el directorio de trabajo de una tarea conocida. En este ejemplo se supone que la tarea y la tarea de prueba ya existen en el equipo local.
ms.assetid: bcfcd6af-a3aa-45a8-bde6-0c90aec3e27a
keywords:
- establecer propiedades de tarea Programador de tareas , directorio de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb17def1d6a280f1a132bb99dbf82111af709faaad86aabb4a7b54685e6c699
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738365"
---
# <a name="cc-code-example-setting-working-directory"></a>Ejemplo de código de C/C++: configuración del directorio de trabajo

En este ejemplo se establece el directorio de trabajo de una tarea conocida. En este ejemplo se supone que la tarea y la tarea de prueba ya existen en el equipo local.


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
  // Call ITask::SetWorkingDirectory to specify the current 
  // working directory for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszWorkingDirectory = L"C:\\Temp";
  
  hr = pITask->SetWorkingDirectory(pwszWorkingDirectory);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetWorkingDirectory: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                          TRUE);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }
  
  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"Set the working directory to C:\\Temp.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




