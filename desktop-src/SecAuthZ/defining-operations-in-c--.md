---
description: En Administrador de autorización, una operación es una función o método de bajo nivel de una aplicación.
ms.assetid: 458c5418-94c5-4977-8203-f8299387c6da
title: Definir operaciones en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31431390d3c95dbf4248ffeebc63f29f1fa6757d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361715"
---
# <a name="defining-operations-in-c"></a><span data-ttu-id="38385-103">Definir operaciones en C++</span><span class="sxs-lookup"><span data-stu-id="38385-103">Defining Operations in C++</span></span>

<span data-ttu-id="38385-104">En Administrador de autorización, una operación es una función o método de bajo nivel de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="38385-104">In Authorization Manager, an operation is a low-level function or method of an application.</span></span> <span data-ttu-id="38385-105">Estas operaciones se agrupan como tareas.</span><span class="sxs-lookup"><span data-stu-id="38385-105">These operations are grouped together as tasks.</span></span> <span data-ttu-id="38385-106">Los usuarios de la aplicación solicitan permiso para completar tareas.</span><span class="sxs-lookup"><span data-stu-id="38385-106">Users of the application request permission to complete tasks.</span></span> <span data-ttu-id="38385-107">Una operación se representa mediante un objeto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="38385-107">An operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="38385-108">Para obtener más información sobre las operaciones, vea [operaciones y tareas](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="38385-108">For more information about operations, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="38385-109">En el ejemplo siguiente se muestra cómo definir operaciones en un almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="38385-109">The following example shows how to define operations in an authorization policy store.</span></span> <span data-ttu-id="38385-110">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada///Expense.</span><span class="sxs-lookup"><span data-stu-id="38385-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


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
    IAzOperation* pOp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
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

    //  Create operations.

    //  Create first operation.
    if (!(opName = SysAllocString(L"RetrieveForm")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");
    
    //  Set the OperationID property.
    hr = pOp->put_OperationID(1);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create second operation.
    if (!(opName = SysAllocString(L"EnqueRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(2);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create third operation.
    if (!(opName = SysAllocString(L"DequeRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(3);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create fourth operation.
    if (!(opName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(4);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create fifth operation.
    if (!(opName = SysAllocString(L"MarkFormApproved")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(5);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Create sixth operation.
    if (!(opName = SysAllocString(L"SendApprovalNotify")))
        MyHandleError("Could not allocate operation name string.");
    hr = pApp->CreateOperation(opName, myVar, &pOp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create operation.");

    //  Set the OperationID property.
    hr = pOp->put_OperationID(6);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not set operation ID.");

    //  Save the operation to the store.
    hr = pOp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save operation.");
    SysFreeString(opName);

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pOp->Release();
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



 

 



