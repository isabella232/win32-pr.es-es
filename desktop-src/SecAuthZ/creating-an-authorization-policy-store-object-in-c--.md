---
description: Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, operaciones, tareas, usuarios y grupos de usuarios asociados a la tienda.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Crear un objeto de almacén de directivas de autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001429"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="c469f-104">Crear un objeto de almacén de directivas de autorización en C++</span><span class="sxs-lookup"><span data-stu-id="c469f-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="c469f-105">Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c469f-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="c469f-106">La información incluye las aplicaciones, operaciones, tareas, usuarios y grupos de usuarios asociados a la tienda.</span><span class="sxs-lookup"><span data-stu-id="c469f-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="c469f-107">Cuando una aplicación que usa administrador de autorización se inicializa, carga esta información desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="c469f-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="c469f-108">El almacén de directivas de autorización debe estar ubicado en un sistema de confianza porque los administradores de ese sistema tienen un alto grado de acceso al almacén.</span><span class="sxs-lookup"><span data-stu-id="c469f-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="c469f-109">Administrador de autorización admite el almacenamiento de la Directiva de autorización en el servicio de directorio de Active Directory o en un archivo XML, tal como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c469f-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="c469f-110">En la API de administrador de autorización, un almacén de directivas de autorización se representa mediante un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="c469f-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="c469f-111">En los ejemplos se muestra cómo crear un objeto **AzAuthorizationStore** para un almacén de Active Directory y un almacén XML.</span><span class="sxs-lookup"><span data-stu-id="c469f-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="c469f-112">Creación de un almacén de Active Directory</span><span class="sxs-lookup"><span data-stu-id="c469f-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="c469f-113">Creación de un almacén de SQL Server</span><span class="sxs-lookup"><span data-stu-id="c469f-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="c469f-114">Crear un almacén XML</span><span class="sxs-lookup"><span data-stu-id="c469f-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="c469f-115">Creación de un almacén de Active Directory</span><span class="sxs-lookup"><span data-stu-id="c469f-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="c469f-116">Para usar Active Directory para almacenar la Directiva de autorización, el dominio debe estar en el nivel funcional del dominio de **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="c469f-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="c469f-117">No se encuentra el almacén de directivas de autorización en un **contexto de nomenclatura que no es de dominio** (también denominado partición de aplicación).</span><span class="sxs-lookup"><span data-stu-id="c469f-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="c469f-118">Se recomienda ubicar el almacén en el contenedor de **datos de programa** en una nueva unidad organizativa creada específicamente para el almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="c469f-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="c469f-119">También se recomienda que el almacén se encuentre en la misma red de área local que los servidores de aplicaciones que ejecutan las aplicaciones que usan el almacén.</span><span class="sxs-lookup"><span data-stu-id="c469f-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="c469f-120">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c469f-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="c469f-121">En el ejemplo se supone que hay una unidad organizativa Active Directory denominada datos de programa en un dominio denominado authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="c469f-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="c469f-122">Creación de un almacén de SQL Server</span><span class="sxs-lookup"><span data-stu-id="c469f-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="c469f-123">Administrador de autorización admite la creación de un almacén de directivas de autorización basado en Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c469f-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="c469f-124">Para crear un almacén de autorización basado en SQL Server, use una dirección URL que comience con el prefijo **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="c469f-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="c469f-125">La dirección URL debe contener una cadena de conexión SQL válida, un nombre de base de datos y el nombre del almacén de directivas de autorización: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="c469f-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="c469f-126">Si la instancia de SQL Server no contiene la base de datos de administrador de autorización especificada, el administrador de autorización crea una nueva base de datos con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="c469f-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="c469f-127">Las conexiones a un almacén de SQL Server no se cifran a menos que se configure explícitamente el cifrado SQL para la conexión o se configure el cifrado del tráfico de red que usa el protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="c469f-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="c469f-128">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en una base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c469f-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a><span data-ttu-id="c469f-129">Crear un almacén XML</span><span class="sxs-lookup"><span data-stu-id="c469f-129">Creating an XML Store</span></span>

<span data-ttu-id="c469f-130">Administrador de autorización admite la creación de un almacén de directivas de autorización en formato XML.</span><span class="sxs-lookup"><span data-stu-id="c469f-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="c469f-131">El almacén XML puede ubicarse en el mismo equipo en el que se ejecuta la aplicación, o bien se puede almacenar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="c469f-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="c469f-132">No se admite la edición directa del archivo XML.</span><span class="sxs-lookup"><span data-stu-id="c469f-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="c469f-133">Use el complemento MMC de administrador de autorización o la API de administrador de autorización para editar el almacén de directivas.</span><span class="sxs-lookup"><span data-stu-id="c469f-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="c469f-134">Administrador de autorización no admite la delegación de la administración de un almacén de directivas XML.</span><span class="sxs-lookup"><span data-stu-id="c469f-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="c469f-135">Para obtener información acerca de la delegación, vea [delegar la definición de permisos en C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="c469f-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="c469f-136">En el ejemplo siguiente se muestra cómo crear un objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="c469f-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


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
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



