---
title: Método alcrear
description: Método alcrear
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Complementos de Windows Media Player, método de creación
- complementos, método de creación
- Complementos de la interfaz de usuario, método de creación
- Complementos de la interfaz de usuario, método de creación
- Método alcrear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903157"
---
# <a name="the-oncreate-method"></a><span data-ttu-id="ad462-108">Método alcrear</span><span class="sxs-lookup"><span data-stu-id="ad462-108">The OnCreate Method</span></span>

<span data-ttu-id="ad462-109">Se llama al método alcrear cuando se crea por primera vez la ventana del complemento.</span><span class="sxs-lookup"><span data-stu-id="ad462-109">The OnCreate method is called when the plug-in window is first created.</span></span>

<span data-ttu-id="ad462-110">El siguiente código se usa para implementar este método:</span><span class="sxs-lookup"><span data-stu-id="ad462-110">The following code is used to implement this method:</span></span>


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



<span data-ttu-id="ad462-111">Este método crea el botón **Buscar** y lo asocia al \_ identificador de comando de búsqueda de IDC, que se define al principio del archivo:</span><span class="sxs-lookup"><span data-stu-id="ad462-111">This method creates the **Search** button and associates it with the IDC\_SEARCH command ID, which is defined at the beginning of the file:</span></span>


```C++
#define IDC_SEARCH 2000

```



<span data-ttu-id="ad462-112">Este identificador de comando se asigna al método de búsqueda en la sección mapa de mensajes que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ad462-112">This command ID is mapped to the OnSearch method in the message map section described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad462-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad462-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad462-114">**Implementación de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="ad462-114">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




