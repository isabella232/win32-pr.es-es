---
description: En el Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se realizan en operaciones, que son funciones y métodos de bajo nivel de la aplicación.
ms.assetid: a9a0202e-44c9-4192-8ff8-e22bddf26cfe
title: Agrupación de operaciones en tareas en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c869db5dc5acbd4a7e7f9401ebbf97dea481c40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073693"
---
# <a name="grouping-operations-into-tasks-in-c"></a>Agrupación de operaciones en tareas en C++

En el Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se realizan en operaciones, que son funciones y métodos de bajo nivel de la aplicación. A continuación, se asigna una tarea a los roles que deben realizar esa tarea. Una tarea se representa mediante un [**objeto IAzTask.**](/windows/desktop/api/Azroles/nn-azroles-iaztask) Para obtener más información sobre las operaciones y las tareas, vea [Operaciones y tareas.](operations-and-tasks.md)

En el ejemplo siguiente se muestra cómo agrupar las operaciones para crear una tarea. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada Expense y que esta aplicación contiene operaciones definidas en el tema [Defining Operations in C++](defining-operations-in-c--.md).


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzTask* pTask = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR taskName = NULL;
    BSTR opName = NULL;
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
  storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a task object.
    if (!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->CreateTask(taskName, myVar, &pTask);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create task.");

    //  Add operations to the task.
    if (!(opName = SysAllocString(L"RetrieveForm")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 1st operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"EnqueRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 2nd operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 3rd operation to the task.");
    SysFreeString(opName);

    //  Save information to the store.
    hr = pTask->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



