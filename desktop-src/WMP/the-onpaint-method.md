---
title: El método OnPaint
description: El método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Complementos de Media Player de Windows, método OnPaint
- complementos, método OnPaint
- Complementos de la interfaz de usuario, método OnPaint
- Complementos de la interfaz de usuario, método OnPaint
- OnPaint (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486975"
---
# <a name="the-onpaint-method"></a><span data-ttu-id="6fc26-108">El método OnPaint</span><span class="sxs-lookup"><span data-stu-id="6fc26-108">The OnPaint Method</span></span>

<span data-ttu-id="6fc26-109">Se llama al método OnPaint siempre que la ventana del complemento debe dibujarse.</span><span class="sxs-lookup"><span data-stu-id="6fc26-109">The OnPaint method is called whenever the plug-in window should paint itself.</span></span> <span data-ttu-id="6fc26-110">Esto sucede cuando la ventana del complemento recibe un mensaje de \_ dibujo de WM, que se asigna al método OnPaint en el mapa de mensajes descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6fc26-110">This occurs when the plug-in window receives a WM\_PAINT message, which is mapped to the OnPaint method in the message map described earlier.</span></span> <span data-ttu-id="6fc26-111">El asistente proporciona una implementación de este método que pinta el negro de fondo y coloca el nombre del complemento en la ventana del complemento.</span><span class="sxs-lookup"><span data-stu-id="6fc26-111">The wizard provides an implementation of this method that paints the background black and places the name of the plug-in in the plug-in window.</span></span> <span data-ttu-id="6fc26-112">La única modificación que es necesaria para el complemento de la interfaz de usuario de búsqueda es la eliminación del código que muestra el texto.</span><span class="sxs-lookup"><span data-stu-id="6fc26-112">The only modification that is necessary for the Search UI plug-in is the removal of the code that displays the text.</span></span>

<span data-ttu-id="6fc26-113">El siguiente código se usa para implementar este método:</span><span class="sxs-lookup"><span data-stu-id="6fc26-113">The following code is used to implement this method:</span></span>


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="6fc26-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fc26-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fc26-115">**Implementación de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="6fc26-115">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




