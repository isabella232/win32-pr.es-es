---
title: Trabajar con perfiles de sistema localizados
description: Trabajar con perfiles de sistema localizados
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- profiles,system
- perfiles del sistema, localizados
- perfiles del sistema, interfaz IWMProfileManagerLanguage
- perfiles del sistema localizados, acerca de
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9525ae51334b14b467324fa393438a9ad52106f4c7519c5ad9b0d00af9e3084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083719"
---
# <a name="working-with-localized-system-profiles"></a>Trabajar con perfiles de sistema localizados

El SDK Windows Media Format incluye perfiles del sistema con nombres y descripciones en varios idiomas. Los archivos .prx del perfil del sistema localizados se instalan en la carpeta \[ SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles. Para acceder a un archivo determinado con los métodos **IWMProfileManagerLanguage,** debe moverlo al directorio raíz del sistema junto con los demás archivos de perfil del sistema. Para obtener una lista de los archivos de perfil del sistema localizados, vea [Perfiles de sistema localizados.](localized-system-profiles.md)

Puede establecer o recuperar el lenguaje de perfil del sistema mediante los métodos de la [**interfaz IWMProfileManagerLanguage.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) El idioma se especifica como un valor LANGID, que consta de un identificador de idioma principal y un identificador de idioma secundario. En el código siguiente se muestra cómo recuperar el lenguaje actual. El idioma predeterminado es inglés de EE. UU. (0x409). Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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

[**Uso de perfiles del sistema**](using-system-profiles.md)
</dt> </dl>

 

 




