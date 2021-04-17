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
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="85e0b-103">Delegación de la definición de permisos en C++</span><span class="sxs-lookup"><span data-stu-id="85e0b-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="85e0b-104">Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de la administración.</span><span class="sxs-lookup"><span data-stu-id="85e0b-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="85e0b-105">La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito.</span><span class="sxs-lookup"><span data-stu-id="85e0b-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="85e0b-106">En cada nivel, hay una lista de administradores y lectores.</span><span class="sxs-lookup"><span data-stu-id="85e0b-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="85e0b-107">Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado.</span><span class="sxs-lookup"><span data-stu-id="85e0b-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="85e0b-108">Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.</span><span class="sxs-lookup"><span data-stu-id="85e0b-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="85e0b-109">También se debe agregar un usuario o grupo que sea administrador o lector de una aplicación como usuario delegado del almacén de directivas que contiene esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="85e0b-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="85e0b-110">De forma similar, un usuario o grupo que sea administrador o lector de un ámbito debe agregarse como un usuario delegado de la aplicación que contiene ese ámbito.</span><span class="sxs-lookup"><span data-stu-id="85e0b-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="85e0b-111">Por ejemplo, para delegar la administración de un ámbito, agregue primero el usuario o el grupo a la lista de usuarios delegados del almacén que contiene el ámbito llamando al método [**IAzAuthorizationStore:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="85e0b-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="85e0b-112">A continuación, agregue el usuario o el grupo a la lista de usuarios delegados de la aplicación que contiene el ámbito mediante una llamada al método [**IAzApplication:: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="85e0b-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="85e0b-113">Por último, agregue el usuario o el grupo a la lista de administradores del ámbito llamando al método [**IAzScope:: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .</span><span class="sxs-lookup"><span data-stu-id="85e0b-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="85e0b-114">Los almacenes de directivas basados en XML no admiten la delegación en cualquier nivel.</span><span class="sxs-lookup"><span data-stu-id="85e0b-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="85e0b-115">No se puede delegar un ámbito dentro de un almacén de autorización almacenado en Active Directory si el ámbito contiene definiciones de tareas que incluyen reglas de autorización o definiciones de roles que incluyen reglas de autorización.</span><span class="sxs-lookup"><span data-stu-id="85e0b-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="85e0b-116">En el ejemplo siguiente se muestra cómo delegar la administración de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="85e0b-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="85e0b-117">En el ejemplo se supone que existe un almacén de directivas de autorización de Active Directory en la ubicación especificada, que este almacén de directivas contiene una aplicación denominada///Expense y que esta aplicación no contiene tareas con scripts de reglas de negocios.</span><span class="sxs-lookup"><span data-stu-id="85e0b-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



