---
title: Método LaunchPage
description: Método LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Reproductor de Windows Media complementos, método LaunchPage
- plug-ins,LaunchPage (método)
- complementos de interfaz de usuario, método LaunchPage
- Complementos de interfaz de usuario, método LaunchPage
- Método LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762725"
---
# <a name="the-launchpage-method"></a>Método LaunchPage

El método LaunchPage proporciona la funcionalidad principal del complemento, que consiste en iniciar una página de búsqueda que contiene información sobre el intérprete del elemento multimedia pasado al método .

El método OnSearch llama a este método mediante el objeto **Media** actual.

El código siguiente se usa para implementar este método:


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




