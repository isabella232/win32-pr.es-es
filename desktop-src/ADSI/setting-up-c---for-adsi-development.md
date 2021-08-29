---
title: Configuración de Visual C++ 6.0 para el desarrollo de ADSI
description: En este tema se muestra cómo configurar C++ en Visual Studio para que pueda desarrollar una aplicación ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configuración de C++ para el desarrollo adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7401977ea1980acb0f62e24d93c3aadf480cda8ef47a8e8d6e5c88ccbcb0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082289"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Configuración de Visual C++ 6.0 para el desarrollo de ADSI

El Microsoft Visual C++ de desarrollo de la versión 6.0 se puede usar para desarrollar aplicaciones empresariales. Para configurar el entorno Visual C++ 6.0 para desarrollar una aplicación ADSI, realice los pasos siguientes:

**Configuración del entorno Microsoft Visual C++ desarrollo de Microsoft Visual C++ 6.0**

1.  Seleccione el directorio include y library. Seleccione **Opciones \| de herramientas**. Haga clic en **la pestaña** Directorio y especifique la ruta de acceso a los archivos de encabezado ADSI.
2.  Incluya el archivo Activeds.h en el proyecto.
3.  Agregue los archivos Activeds.lib y Adsiid.lib a la entrada del vinculador del proyecto.
4.  Comience a programar con ADSI.

Inicie sesión en un dominio Windows usuario. También debe tener permiso para modificar datos en Active Directory. De forma predeterminada, el administrador tiene este privilegio. Para escribir este ejemplo de código:

**Una aplicación Visual C++ ejemplo: Crear un usuario en un dominio**

1.  Inicie Visual C++ 6.0.
2.  Cree un proyecto ejecutable independiente. Puede ser una aplicación MFC, ATL o de consola.
3.  Siga los pasos anteriores para configurar el proyecto.
4.  Escriba el ejemplo de código siguiente. Reemplace la cadena "LDAP://CN=users,DC=fabrikam,DC=com" por la ruta ADsPath de un contenedor del dominio. También debe reemplazar el nombre de usuario "jeffsmith" por un nombre de usuario que sea único en el dominio.

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

    

5.  Compile y ejecute la aplicación. Para comprobar que se ha creado el usuario, use la herramienta Usuarios y equipos de Active Directory administración de datos.

 

 




