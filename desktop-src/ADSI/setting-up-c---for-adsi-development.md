---
title: Configuración de Visual C++ 6,0 para el desarrollo ADSI
description: En este tema se muestra cómo configurar C++ en Visual Studio para que pueda desarrollar una aplicación ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configurar C++ para el desarrollo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075062"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="d9080-104">Configuración de Visual C++ 6,0 para el desarrollo ADSI</span><span class="sxs-lookup"><span data-stu-id="d9080-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="d9080-105">El sistema de desarrollo Microsoft Visual C++ 6,0 se puede usar para desarrollar aplicaciones empresariales.</span><span class="sxs-lookup"><span data-stu-id="d9080-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="d9080-106">Para configurar el entorno de Visual C++ 6,0 para desarrollar una aplicación ADSI, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d9080-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="d9080-107">**Configuración del entorno de desarrollo de Microsoft Visual C++ 6,0**</span><span class="sxs-lookup"><span data-stu-id="d9080-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="d9080-108">Señale a los directorios de inclusión y de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d9080-108">Point to the include and library directory.</span></span> <span data-ttu-id="d9080-109">Seleccione **\| Opciones de herramientas**.</span><span class="sxs-lookup"><span data-stu-id="d9080-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="d9080-110">Haga clic en la pestaña **directorio** y especifique la ruta de acceso a los archivos de encabezado ADSI.</span><span class="sxs-lookup"><span data-stu-id="d9080-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="d9080-111">Incluya el archivo activeds. h en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="d9080-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="d9080-112">Agregue los archivos activeds. lib y Adsiid. lib a la entrada del vinculador del proyecto.</span><span class="sxs-lookup"><span data-stu-id="d9080-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="d9080-113">Comience la programación con ADSI.</span><span class="sxs-lookup"><span data-stu-id="d9080-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="d9080-114">Inicie sesión en un dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="d9080-114">Log on to a Windows domain.</span></span> <span data-ttu-id="d9080-115">También debe tener permiso para modificar los datos en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9080-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="d9080-116">De forma predeterminada, el administrador tiene este privilegio.</span><span class="sxs-lookup"><span data-stu-id="d9080-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="d9080-117">Para escribir este ejemplo de código:</span><span class="sxs-lookup"><span data-stu-id="d9080-117">To enter this code example:</span></span>

<span data-ttu-id="d9080-118">**Visual C++ aplicación de ejemplo: crear un usuario en un dominio**</span><span class="sxs-lookup"><span data-stu-id="d9080-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="d9080-119">Inicie Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="d9080-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="d9080-120">Cree un proyecto ejecutable independiente.</span><span class="sxs-lookup"><span data-stu-id="d9080-120">Create a standalone executable project.</span></span> <span data-ttu-id="d9080-121">Puede ser una aplicación MFC, ATL o de consola.</span><span class="sxs-lookup"><span data-stu-id="d9080-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="d9080-122">Siga los pasos anteriores para configurar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="d9080-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="d9080-123">Escriba el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="d9080-123">Enter the following code example.</span></span> <span data-ttu-id="d9080-124">Reemplace la cadena "LDAP: el valor de users, DC = Fabrikam, DC = com" por el ADsPath de un contenedor de su dominio.</span><span class="sxs-lookup"><span data-stu-id="d9080-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="d9080-125">También debe reemplazar el nombre de usuario "juanpérez" por un nombre de usuario que sea único en su dominio.</span><span class="sxs-lookup"><span data-stu-id="d9080-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="d9080-126">Compile y ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9080-126">Build and run the application.</span></span> <span data-ttu-id="d9080-127">Para comprobar que se ha creado el usuario, use la herramienta de administración de usuarios y equipos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9080-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




