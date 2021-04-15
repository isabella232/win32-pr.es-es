---
title: Trabajar con perfiles de sistema localizados
description: Trabajar con perfiles de sistema localizados
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- perfiles, sistema
- perfiles del sistema, localizados
- perfiles del sistema, interfaz IWMProfileManagerLanguage
- perfiles de sistema localizados, acerca de
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676339"
---
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="62e4d-108">Trabajar con perfiles de sistema localizados</span><span class="sxs-lookup"><span data-stu-id="62e4d-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="62e4d-109">El SDK de Windows Media Format incluye perfiles del sistema con nombres y descripciones en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="62e4d-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="62e4d-110">Los archivos. prx de perfil del sistema localizados se instalan en la \[ \] \\ carpeta SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles</span><span class="sxs-lookup"><span data-stu-id="62e4d-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="62e4d-111">Para tener acceso a un archivo determinado con los métodos **IWMProfileManagerLanguage** , debe moverlo al directorio raíz del sistema junto con los demás archivos de perfil del sistema.</span><span class="sxs-lookup"><span data-stu-id="62e4d-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="62e4d-112">Para obtener una lista de los archivos de Perfil de sistema localizados, consulte [perfiles de sistema localizados](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="62e4d-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="62e4d-113">Puede establecer o recuperar el idioma del perfil del sistema mediante los métodos de la interfaz [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) .</span><span class="sxs-lookup"><span data-stu-id="62e4d-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="62e4d-114">El idioma se especifica como un valor LANGID, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="62e4d-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="62e4d-115">En el código siguiente se muestra cómo recuperar el lenguaje actual.</span><span class="sxs-lookup"><span data-stu-id="62e4d-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="62e4d-116">El idioma predeterminado es el Inglés de EE. UU. (0xC0A).</span><span class="sxs-lookup"><span data-stu-id="62e4d-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="62e4d-117">Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="62e4d-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="62e4d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62e4d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62e4d-119">**Usar perfiles del sistema**</span><span class="sxs-lookup"><span data-stu-id="62e4d-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




