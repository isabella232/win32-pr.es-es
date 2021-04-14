---
title: Cómo agregar compatibilidad para varios monitores
description: DirectWrite incluye compatibilidad con sistemas con varios monitores.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420999"
---
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="2820d-103">Cómo agregar compatibilidad para varios monitores</span><span class="sxs-lookup"><span data-stu-id="2820d-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="2820d-104">[DirectWrite](direct-write-portal.md) incluye compatibilidad con sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="2820d-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="2820d-105">Los distintos monitores pueden tener diferentes geometrías de píxeles (RGB, BGR o FLAT) u otros atributos.</span><span class="sxs-lookup"><span data-stu-id="2820d-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="2820d-106">Para obtener más información acerca de la geometría de píxeles, vea el tema de referencia de la [**\_ \_ geometría de DWRITE píxeles**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) .</span><span class="sxs-lookup"><span data-stu-id="2820d-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="2820d-107">En este tema se muestra cómo agregar compatibilidad para varios monitores a la aplicación de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="2820d-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="2820d-108">Para admitir varios monitores, debe controlar el mensaje de la ventana de **\_ WINDOWPOSCHANGED de WM** .</span><span class="sxs-lookup"><span data-stu-id="2820d-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="2820d-109">Este mensaje se envía cuando se mueve la ventana, por lo que debe comprobar si la ventana se ha desactivado en un monitor diferente, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="2820d-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



<span data-ttu-id="2820d-110">Si la ventana se encuentra en un nuevo monitor, debe crear los parámetros de representación para el nuevo monitor mediante el método [**IDWriteFactory:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="2820d-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="2820d-111">No use el método [**IDWriteFactory:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para crear los parámetros de representación, ya que siempre crea parámetros para el monitor principal.</span><span class="sxs-lookup"><span data-stu-id="2820d-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="2820d-112">Cuando tenga un objeto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , establezca los parámetros de representación para el destino de representación mediante el método [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="2820d-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="2820d-113">Por último, use la función [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para que la ventana se vuelva a dibujar con los nuevos parámetros de representación.</span><span class="sxs-lookup"><span data-stu-id="2820d-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 