---
description: En el Administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que los grupos de usuarios se pueden anidar.
ms.assetid: b01883d6-eae6-4f3a-b269-90c22827f116
title: Agregar usuarios a un grupo de aplicaciones en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fa08ddd93ba1743a20e3eb14a5f62344741c90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073727"
---
# <a name="adding-users-to-an-application-group-in-c"></a>Agregar usuarios a un grupo de aplicaciones en C++

En el Administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que los grupos de usuarios se pueden anidar. Un grupo de aplicaciones se representa mediante un [**objeto IAzApplicationGroup.**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)

Para permitir que los miembros de un grupo de aplicaciones realicen una tarea o un conjunto de tareas, asigne ese grupo de aplicaciones a un rol que contenga esas tareas. Los roles se representan mediante [**objetos IAzRole.**](/windows/desktop/api/Azroles/nn-azroles-iazrole)

En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones, agregar un usuario como miembro del grupo de aplicaciones y asignar el grupo de aplicaciones a un rol existente. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada Expense y que esta aplicación contiene un rol denominado Administrador de gastos.


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
    IAzApplicationGroup* pAppGroup = NULL;
    IAzRole* pRole = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR groupName = NULL;
    BSTR userName = NULL;
    BSTR roleName = NULL;
    
    
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

    //  Allocate a string for the name of the policy store.
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

    //  Allocate a string for the group name.
    if (!(groupName = SysAllocString(L"Approvers")))
        MyHandleError("Could not allocate group name string.");

    //  Create an IAzApplicationGroup object.
    hr = pApp->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add a member to the group.
 //  Replace with valid domain and user name.
    if (!(userName = SysAllocString(L"domain\\username")))
        MyHandleError("Could not allocate user name string.");

    hr = pAppGroup->AddMemberName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add user to application group.");

    //  Save information to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save group information.");

    //  Open an IAzRole object.
    if (!(roleName = SysAllocString(L"Expense Administrator")))
        MyHandleError("Could not allocate role name string.");

    hr = pApp->OpenRole(roleName, myVar, &pRole);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open role object.");

    //  Add the group to the role.
    hr = pRole->AddAppMember(groupName, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not add the application group to the role.");


    //  Save information to the store.
    hr = pRole->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save role data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pAppGroup->Release();
    pRole->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(groupName);
    SysFreeString(roleName);
    SysFreeString(userName);
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



 

 



