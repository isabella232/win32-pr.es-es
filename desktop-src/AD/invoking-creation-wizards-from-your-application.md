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
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="01a4b-104">Invocar asistentes para creación desde la aplicación</span><span class="sxs-lookup"><span data-stu-id="01a4b-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="01a4b-105">Una aplicación o componente puede usar los mismos asistentes para crear objetos de servicio de directorio usados por el Active Directory complementos de MMC administrativos. Esto se logra con la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="01a4b-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="01a4b-106">Uso de la interfaz IDsAdminCreateObj</span><span class="sxs-lookup"><span data-stu-id="01a4b-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="01a4b-107">Una aplicación o componente (cliente) crea una instancia de la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase **\_ DsAdminCreateObj CLSID** .</span><span class="sxs-lookup"><span data-stu-id="01a4b-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="01a4b-108">COM debe inicializarse llamando a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de llamar a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="01a4b-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="01a4b-109">Después, el cliente llama a [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) para inicializar el objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="01a4b-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="01a4b-110">**IDsAdminCreateObj:: Initialize** acepta un puntero de interfaz [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) que representa el contenedor en el que se debe crear el objeto y el nombre de clase del objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="01a4b-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="01a4b-111">Al crear objetos de usuario, también es posible especificar un objeto existente que se copiará en el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="01a4b-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="01a4b-112">Cuando se ha inicializado el objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) , el cliente llama a [**IDsAdminCreateObj:: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) para mostrar el Asistente para creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="01a4b-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="01a4b-113">A diferencia de la mayoría de los identificadores de clase e interfaz, los **CLSID \_ DsAdminCreateObj** y **IID \_ ADsAdminCreateObj** no se definen en un archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="01a4b-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="01a4b-114">Esto significa que debe definir el almacenamiento de estos identificadores dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="01a4b-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="01a4b-115">Para ello, debe incluir el archivo initguid. h inmediatamente antes de incluir el DSAdmin. h.</span><span class="sxs-lookup"><span data-stu-id="01a4b-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="01a4b-116">El archivo initguid. h solo debe incluirse una vez en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="01a4b-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="01a4b-117">En el ejemplo de código siguiente se muestra cómo incluir estos archivos.</span><span class="sxs-lookup"><span data-stu-id="01a4b-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="01a4b-118">En el ejemplo de código siguiente se muestra cómo se puede crear y utilizar la interfaz [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) para iniciar el Asistente para crear objetos para un objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="01a4b-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


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



 

 