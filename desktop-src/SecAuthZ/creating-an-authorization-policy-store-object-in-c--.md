---
description: Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, las operaciones, las tareas, los usuarios y los grupos de usuarios asociados al almacén.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Crear un objeto de almacén de directivas de autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160829"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Crear un objeto de almacén de directivas de autorización en C++

Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, las operaciones, las tareas, los usuarios y los grupos de usuarios asociados al almacén. Cuando se inicializa una aplicación que usa el Administrador de autorización, carga esta información desde el almacén. El almacén de directivas de autorización debe encontrarse en un sistema de confianza porque los administradores de ese sistema tienen un alto grado de acceso al almacén.

El Administrador de autorización admite el almacenamiento de la directiva de autorización Active Directory servicio de directorio o en un archivo XML, como se muestra en los ejemplos siguientes. En la API de Authorization Manager, un almacén de directivas de autorización se representa mediante [**un objeto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) En los ejemplos se muestra cómo crear un **objeto AzAuthorizationStore** para un Active Directory y un almacén XML.

-   [Creación de una Active Directory Store](#creating-an-active-directory-store)
-   [Creación de un SQL Server Store](#creating-a-sql-server-store)
-   [Creación de un almacén XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Creación de una Active Directory Store

Para usar Active Directory para almacenar la directiva de autorización, el dominio debe estar en el nivel funcional de dominio Windows **Server 2003.** El almacén de directivas de autorización no se puede encontrar en un contexto de nomenclatura que no sea **de dominio** (también denominado partición de aplicación). Se recomienda que el almacén  se encuentra en el contenedor Datos del programa en una nueva unidad organizativa creada específicamente para el almacén de directivas de autorización. También se recomienda que el almacén se encuentra dentro de la misma red de área local que los servidores de aplicaciones que ejecutan aplicaciones que usan el almacén.

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en Active Directory. En el ejemplo se supone que hay una unidad organizativa Active Directory denominada Datos de programa en un dominio denominado authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Creación de un SQL Server Store

El Administrador de autorización admite la creación de un Microsoft SQL Server de directivas de autorización basado en directivas. Para crear un SQL Server de autorización basado en el servidor, use una dirección URL que comience con el **prefijo MSSQL://**. La dirección URL debe contener una cadena de conexión SQL, un nombre de base de datos y el nombre del almacén de directivas de autorización: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Si la instancia de SQL Server no contiene la base de datos del Administrador de autorización especificada, el Administrador de autorización crea una nueva base de datos con ese nombre.

> [!Note]  
> Las conexiones a un almacén de SQL Server no se cifran a menos que configure explícitamente un cifrado de SQL para la conexión o configure el cifrado del tráfico de red que usa seguridad de protocolo de Internet (IPsec).

 

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en una base SQL Server datos.


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



## <a name="creating-an-xml-store"></a>Creación de un almacén XML

Authorization Manager admite la creación de un almacén de directivas de autorización en formato XML. El almacén XML se puede encontrar en el mismo equipo donde se ejecuta la aplicación o se puede almacenar de forma remota. No se admite la edición directa del archivo XML. Use el complemento MMC de Authorization Manager o la API de Authorization Manager para editar el almacén de directivas.

El Administrador de autorización no admite la delegación de la administración de un almacén de directivas XML. Para obtener información sobre la delegación, vea [Delegación de la definición de permisos en C++.](delegating-the-defining-of-permissions-in-c--.md)

En el ejemplo siguiente se muestra cómo crear un [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa un almacén de directivas de autorización en un archivo XML.


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



 

 



