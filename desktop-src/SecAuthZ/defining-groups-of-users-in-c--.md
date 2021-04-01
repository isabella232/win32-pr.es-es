---
description: En el administrador de autorización, un objeto IAzApplicationGroup representa un grupo de usuarios. Los roles se pueden asignar a este grupo de usuarios colectivamente.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Definir grupos de usuarios en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913058"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="d0a54-104">Definir grupos de usuarios en C++</span><span class="sxs-lookup"><span data-stu-id="d0a54-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="d0a54-105">En el administrador de autorización, un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="d0a54-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="d0a54-106">Los roles se pueden asignar a este grupo de usuarios colectivamente.</span><span class="sxs-lookup"><span data-stu-id="d0a54-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="d0a54-107">Un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) también puede incluir otros objetos **IAzApplicationGroup** como miembros.</span><span class="sxs-lookup"><span data-stu-id="d0a54-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="d0a54-108">Para obtener más información acerca de los grupos de aplicaciones, consulte [usuarios y grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="d0a54-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="d0a54-109">Un grupo se puede definir mediante listas explícitas de miembros y no miembros, o bien mediante una consulta LDAP ( [*Protocolo ligero de acceso a directorios*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="d0a54-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="d0a54-110">En los siguientes ejemplos se muestra cómo crear cada tipo de grupo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="d0a54-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="d0a54-111">Creación de un grupo básico</span><span class="sxs-lookup"><span data-stu-id="d0a54-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="d0a54-112">Crear un grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="d0a54-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="d0a54-113">Creación de un grupo básico</span><span class="sxs-lookup"><span data-stu-id="d0a54-113">Creating a Basic Group</span></span>

<span data-ttu-id="d0a54-114">Los miembros incluidos en los [**miembros y las**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) propiedades que no son [**miembros**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) del objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa el grupo definen un grupo de aplicación básico.</span><span class="sxs-lookup"><span data-stu-id="d0a54-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="d0a54-115">Los usuarios y grupos que se enumeran en la propiedad **Members** se incluyen en el grupo de aplicaciones, y los usuarios y grupos que se enumeran en la propiedad **nonmembers** se excluyen del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d0a54-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="d0a54-116">Que se enumeran en la propiedad los miembros no **miembros** se sustituyen en la propiedad **Members** .</span><span class="sxs-lookup"><span data-stu-id="d0a54-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="d0a54-117">En el ejemplo siguiente se muestra cómo crear un grupo de aplicación básico y agregar todos los usuarios locales como miembros de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="d0a54-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="d0a54-118">En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C.</span><span class="sxs-lookup"><span data-stu-id="d0a54-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

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

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="d0a54-119">Crear un grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="d0a54-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="d0a54-120">Un grupo de consulta LDAP tiene una pertenencia definida por la consulta contenida en el valor de su propiedad [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="d0a54-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="d0a54-121">En el ejemplo siguiente se muestra cómo crear un grupo de aplicaciones de consulta LDAP y cómo agregar todos los usuarios como miembros de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="d0a54-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="d0a54-122">En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C.</span><span class="sxs-lookup"><span data-stu-id="d0a54-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
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



 

 
