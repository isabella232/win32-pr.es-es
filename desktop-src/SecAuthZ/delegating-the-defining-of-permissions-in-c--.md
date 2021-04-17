---
description: Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de la administración.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Delegación de la definición de permisos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652898"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Delegación de la definición de permisos en C++

Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de la administración. La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito.

En cada nivel, hay una lista de administradores y lectores. Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado. Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.

También se debe agregar un usuario o grupo que sea administrador o lector de una aplicación como usuario delegado del almacén de directivas que contiene esa aplicación. De forma similar, un usuario o grupo que sea administrador o lector de un ámbito debe agregarse como un usuario delegado de la aplicación que contiene ese ámbito.

Por ejemplo, para delegar la administración de un ámbito, agregue primero el usuario o el grupo a la lista de usuarios delegados del almacén que contiene el ámbito llamando al método [**IAzAuthorizationStore:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) . A continuación, agregue el usuario o el grupo a la lista de usuarios delegados de la aplicación que contiene el ámbito mediante una llamada al método [**IAzApplication:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) . Por último, agregue el usuario o el grupo a la lista de administradores del ámbito llamando al método [**IAzScope:: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .

Los almacenes de directivas basados en XML no admiten la delegación en cualquier nivel.

No se puede delegar un ámbito dentro de un almacén de autorización almacenado en Active Directory si el ámbito contiene definiciones de tareas que incluyen reglas de autorización o definiciones de roles que incluyen reglas de autorización.

En el ejemplo siguiente se muestra cómo delegar la administración de una aplicación. En el ejemplo se supone que existe un almacén de directivas de autorización de Active Directory en la ubicación especificada, que este almacén de directivas contiene una aplicación denominada///Expense y que esta aplicación no contiene tareas con scripts de reglas de negocios.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
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
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
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



 

 



