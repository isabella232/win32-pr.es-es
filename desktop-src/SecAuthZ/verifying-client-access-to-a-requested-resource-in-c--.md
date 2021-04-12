---
description: Llame al método AccessCheck de la interfaz IAzClientContext para comprobar si el cliente tiene acceso a una o varias operaciones.
ms.assetid: 7c8a63c5-2eab-4414-9a3d-c99a92b67a62
title: Comprobar el acceso del cliente a un recurso solicitado en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeffe9cb3312e33a283c1701b58356cdf5ea9b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279312"
---
# <a name="verifying-client-access-to-a-requested-resource-in-c"></a><span data-ttu-id="c891c-103">Comprobar el acceso del cliente a un recurso solicitado en C++</span><span class="sxs-lookup"><span data-stu-id="c891c-103">Verifying Client Access to a Requested Resource in C++</span></span>

<span data-ttu-id="c891c-104">Llame al método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de la interfaz [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para comprobar si el cliente tiene acceso a una o varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="c891c-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) interface to check if the client has access to one or more operations.</span></span> <span data-ttu-id="c891c-105">Un cliente puede ser miembro de más de un rol, y una operación se puede asignar a más de una tarea, por lo que el administrador de autorización comprueba todos los roles y las tareas.</span><span class="sxs-lookup"><span data-stu-id="c891c-105">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="c891c-106">Si un rol al que pertenece el cliente contiene cualquier tarea que contenga una operación, se concede el acceso a esa operación.</span><span class="sxs-lookup"><span data-stu-id="c891c-106">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="c891c-107">Para comprobar el acceso solo a un rol al que pertenece el cliente, establezca la propiedad [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) de la interfaz [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="c891c-107">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) interface.</span></span>

<span data-ttu-id="c891c-108">Al inicializar el almacén de directivas de autorización para la comprobación de acceso, debe pasar cero como el valor del parámetro *lFlags* del método [**IAzAuthorizationStore:: Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) .</span><span class="sxs-lookup"><span data-stu-id="c891c-108">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**IAzAuthorizationStore::Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method.</span></span>

<span data-ttu-id="c891c-109">En el ejemplo siguiente se muestra cómo comprobar el acceso de un cliente a una operación.</span><span class="sxs-lookup"><span data-stu-id="c891c-109">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="c891c-110">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada///Expense y una operación denominada UseFormControl, y que la variable hToken contiene un token de cliente válido.</span><span class="sxs-lookup"><span data-stu-id="c891c-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense and an operation named UseFormControl, and that the variable hToken contains a valid client token.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    void MyHandleError(char *s);

    VARIANT myVar;
    VariantInit(&myVar);//.vt) = VT_NULL;

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

    //  Allocate a string for the  policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\myStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
   &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Set up parameters for access check.

    //  Set up the object name.
    if (!(operationName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");

    //  Get the ID of the operation to check.
    hr = pApp->OpenOperation(operationName, myVar, &pOperation);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open operation.");

    hr = pOperation->get_OperationID(&operationID);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not get operation ID.");

    //  Create a SAFEARRAY for the operation ID.
    varOperationIdArray.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);

    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create an array of indexes.
    LONG* index = new LONG[1];
    index[0] = 0;

    //  Populate a SAFEARRAY with the operation ID.
    varOperationId.vt = VT_I4;
    varOperationId.lVal = operationID;

    hr = SafeArrayPutElement(varOperationIdArray.parray, index,
   &varOperationId);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not put operation ID in array.");

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,
        varOperationIdArray,
        myVar,               // use default application scope
        myVar,
        myVar,
        myVar,
        myVar,
        &varResultsArray);

    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not complete access check.");

    hr = SafeArrayGetElement(varResultsArray.parray, index, &varResult);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not get result from array.");

    if (varResult.lVal == 0)
        printf("Access granted.\n");
    else
        printf("Access denied.\n");
    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
    pOperation->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult); 
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



 

 



