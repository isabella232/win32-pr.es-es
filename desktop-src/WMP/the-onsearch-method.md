---
title: Método de búsqueda
description: Método de búsqueda
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Complementos de Windows Media Player, método de búsqueda
- complementos, método de búsqueda
- Complementos de la interfaz de usuario, método de búsqueda
- Complementos de la interfaz de usuario, método de búsqueda
- Método de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075831"
---
# <a name="the-onsearch-method"></a><span data-ttu-id="2c6ba-108">Método de búsqueda</span><span class="sxs-lookup"><span data-stu-id="2c6ba-108">The OnSearch Method</span></span>

<span data-ttu-id="2c6ba-109">Windows llama al método de búsqueda Media Player cuando se hace clic en el botón **Buscar** .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-109">The OnSearch method is called by Windows Media Player when the **Search** button is clicked.</span></span> <span data-ttu-id="2c6ba-110">Este método recupera el objeto **multimedia** actual y lo pasa al método LaunchPage.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-110">This method retrieves the current **Media** object and passes it to the LaunchPage method.</span></span>

<span data-ttu-id="2c6ba-111">El siguiente código se usa para implementar este método:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-111">The following code is used to implement this method:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2c6ba-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c6ba-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c6ba-113">**Implementación de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="2c6ba-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




