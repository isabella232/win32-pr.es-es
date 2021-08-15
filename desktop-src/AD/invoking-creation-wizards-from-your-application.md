---
title: Invocar asistentes de creación desde la aplicación
description: Una aplicación o componente puede usar los mismos asistentes para la creación de objetos de servicio de directorio que usa Active Directory complementos MMC administrativos. Esto se logra con la interfaz IDsAdminCreateObj.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Invocar asistentes de creación desde la aplicación AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1d5f8c722e3f673d998d3baaf33b4110293c70875a68fd03e8117f667351bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187079"
---
# <a name="invoking-creation-wizards-from-your-application"></a>Invocar asistentes de creación desde la aplicación

Una aplicación o componente puede usar los mismos asistentes de creación de objetos de servicio de directorio que usa Active Directory complementos MMC administrativos. Esto se logra con la [**interfaz IDsAdminCreateObj.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj)

## <a name="using-the-idsadmincreateobj-interface"></a>Uso de la interfaz IDsAdminCreateObj

Una aplicación o componente (cliente) crea una instancia de la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase **CLSID \_ DsAdminCreateObj.** COM debe inicializarse llamando a [**CoInitialize antes**](/windows/win32/api/objbase/nf-objbase-coinitialize) de llamar a **CoCreateInstance.**

A continuación, el cliente llama a [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) para inicializar el [**objeto IDsAdminCreateObj.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) **IDsAdminCreateObj::Initialize** acepta un puntero de interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) que representa el contenedor en el que se debe crear el objeto y el nombre de clase del objeto que se va a crear. Al crear objetos de usuario, también es posible especificar un objeto existente que se copiará en el nuevo objeto.

Cuando se ha inicializado el objeto [**IDsAdminCreateObj,**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) el cliente llama a [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) para mostrar el Asistente para la creación de objetos.

A diferencia de la mayoría de los identificadores de clase e interfaz, **CLSID \_ DsAdminCreateObj** e **IID \_ ADsAdminCreateObj** no se definen en un archivo de biblioteca. Esto significa que debe definir el almacenamiento para estos identificadores dentro de la aplicación. Para ello, debe incluir el archivo initguid.h inmediatamente antes de incluir dsadmin.h. El archivo initguid.h solo debe incluirse una vez en una aplicación. En el ejemplo de código siguiente se muestra cómo incluir estos archivos.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



En el ejemplo de código siguiente se muestra cómo se puede crear y usar la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) para iniciar el Asistente para la creación de objetos para un objeto de usuario.


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



 

 