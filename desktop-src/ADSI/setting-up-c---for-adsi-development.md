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
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Configuración de Visual C++ 6,0 para el desarrollo ADSI

El sistema de desarrollo Microsoft Visual C++ 6,0 se puede usar para desarrollar aplicaciones empresariales. Para configurar el entorno de Visual C++ 6,0 para desarrollar una aplicación ADSI, realice los pasos siguientes:

**Configuración del entorno de desarrollo de Microsoft Visual C++ 6,0**

1.  Señale a los directorios de inclusión y de biblioteca. Seleccione **\| Opciones de herramientas**. Haga clic en la pestaña **directorio** y especifique la ruta de acceso a los archivos de encabezado ADSI.
2.  Incluya el archivo activeds. h en el proyecto.
3.  Agregue los archivos activeds. lib y Adsiid. lib a la entrada del vinculador del proyecto.
4.  Comience la programación con ADSI.

Inicie sesión en un dominio de Windows. También debe tener permiso para modificar los datos en Active Directory. De forma predeterminada, el administrador tiene este privilegio. Para escribir este ejemplo de código:

**Visual C++ aplicación de ejemplo: crear un usuario en un dominio**

1.  Inicie Visual C++ 6,0.
2.  Cree un proyecto ejecutable independiente. Puede ser una aplicación MFC, ATL o de consola.
3.  Siga los pasos anteriores para configurar el proyecto.
4.  Escriba el siguiente ejemplo de código. Reemplace la cadena "LDAP: el valor de users, DC = Fabrikam, DC = com" por el ADsPath de un contenedor de su dominio. También debe reemplazar el nombre de usuario "juanpérez" por un nombre de usuario que sea único en su dominio.

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

    

5.  Compile y ejecute la aplicación. Para comprobar que se ha creado el usuario, use la herramienta de administración de usuarios y equipos de Active Directory.

 

 




