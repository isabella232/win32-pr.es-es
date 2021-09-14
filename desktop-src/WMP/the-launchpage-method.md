---
title: Método LaunchPage
description: Método LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Reproductor de Windows Media complementos,método LaunchPage
- plug-ins,LaunchPage (método)
- complementos de interfaz de usuario, método LaunchPage
- Complementos de interfaz de usuario, método LaunchPage
- Método LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073211"
---
# <a name="the-launchpage-method"></a>Método LaunchPage

El método LaunchPage proporciona la funcionalidad principal del complemento, que consiste en iniciar una página de búsqueda que contiene información sobre el intérprete del elemento multimedia pasado al método .

El método OnSearch llama a este método mediante el objeto **Media** actual.

Para implementar este método se usa el código siguiente:


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

 

 




