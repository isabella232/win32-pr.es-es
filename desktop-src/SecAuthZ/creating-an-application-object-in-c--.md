---
description: Un almacén de directivas de autorización contiene información de directiva de autorización para una o varias aplicaciones. Para cada aplicación que use ese almacén de directivas, debe crear un objeto IAzApplication y guardarlo en un almacén de directivas.
ms.assetid: 2bba1068-ae03-4388-be4d-9865e42e440e
title: Creación de un objeto de aplicación en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86885124e2fff52bc5cce2260e3d7fb727b58eb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160840"
---
# <a name="creating-an-application-object-in-c"></a>Creación de un objeto de aplicación en C++

Un almacén de directivas de autorización contiene información de directiva de autorización para una o varias aplicaciones. Para cada aplicación que use ese almacén de directivas, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.

En el ejemplo siguiente se muestra cómo crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representa una aplicación y cómo agregar el objeto **IAzApplication** al almacén de directivas de autorización que usa la aplicación. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;

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
    
    //  Initialize the existing store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
         MyHandleError("Could not allocate application name string");
    hr = pStore->CreateApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application.");

    //  Save changes to the store.
    hr = pApp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
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



 

 



