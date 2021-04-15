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
# <a name="working-with-localized-system-profiles"></a>Trabajar con perfiles de sistema localizados

El SDK de Windows Media Format incluye perfiles del sistema con nombres y descripciones en varios idiomas. Los archivos. prx de perfil del sistema localizados se instalan en la \[ \] \\ carpeta SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Para tener acceso a un archivo determinado con los métodos **IWMProfileManagerLanguage** , debe moverlo al directorio raíz del sistema junto con los demás archivos de perfil del sistema. Para obtener una lista de los archivos de Perfil de sistema localizados, consulte [perfiles de sistema localizados](localized-system-profiles.md).

Puede establecer o recuperar el idioma del perfil del sistema mediante los métodos de la interfaz [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) . El idioma se especifica como un valor LANGID, que consta de un identificador de idioma principal y un identificador de idioma secundario. En el código siguiente se muestra cómo recuperar el lenguaje actual. El idioma predeterminado es el Inglés de EE. UU. (0xC0A). Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar perfiles del sistema**](using-system-profiles.md)
</dt> </dl>

 

 




