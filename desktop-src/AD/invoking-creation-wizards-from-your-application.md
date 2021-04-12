---
title: Invocar asistentes para creación desde la aplicación
description: Una aplicación o componente puede usar los mismos asistentes para crear objetos de servicio de directorio usados por el Active Directory complementos de MMC administrativos. Esto se logra con la interfaz IDsAdminCreateObj.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Invocar asistentes para creación desde el AD de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487423"
---
# <a name="invoking-creation-wizards-from-your-application"></a>Invocar asistentes para creación desde la aplicación

Una aplicación o componente puede usar los mismos asistentes para crear objetos de servicio de directorio usados por el Active Directory complementos de MMC administrativos. Esto se logra con la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .

## <a name="using-the-idsadmincreateobj-interface"></a>Uso de la interfaz IDsAdminCreateObj

Una aplicación o componente (cliente) crea una instancia de la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase **\_ DsAdminCreateObj CLSID** . COM debe inicializarse llamando a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de llamar a **CoCreateInstance** .

Después, el cliente llama a [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) para inicializar el objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) . **IDsAdminCreateObj:: Initialize** acepta un puntero de interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) que representa el contenedor en el que se debe crear el objeto y el nombre de clase del objeto que se va a crear. Al crear objetos de usuario, también es posible especificar un objeto existente que se copiará en el nuevo objeto.

Cuando se ha inicializado el objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) , el cliente llama a [**IDsAdminCreateObj:: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) para mostrar el Asistente para creación de objetos.

A diferencia de la mayoría de los identificadores de clase e interfaz, los **CLSID \_ DsAdminCreateObj** y **IID \_ ADsAdminCreateObj** no se definen en un archivo de biblioteca. Esto significa que debe definir el almacenamiento de estos identificadores dentro de la aplicación. Para ello, debe incluir el archivo initguid. h inmediatamente antes de incluir el DSAdmin. h. El archivo initguid. h solo debe incluirse una vez en una aplicación. En el ejemplo de código siguiente se muestra cómo incluir estos archivos.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



En el ejemplo de código siguiente se muestra cómo se puede crear y utilizar la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) para iniciar el Asistente para crear objetos para un objeto de usuario.


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 