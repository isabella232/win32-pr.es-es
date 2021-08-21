---
title: El método OnSearch
description: El método OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Reproductor de Windows Media complementos,método OnSearch
- complementos, método OnSearch
- complementos de interfaz de usuario,método OnSearch
- Complementos de interfaz de usuario, método OnSearch
- Método OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118005"
---
# <a name="the-onsearch-method"></a>El método OnSearch

Cuando se hace clic en el botón  Buscar, Reproductor de Windows Media llama al método OnSearch. Este método recupera el objeto **Media** actual y lo pasa al método LaunchPage.

Para implementar este método se usa el código siguiente:


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




