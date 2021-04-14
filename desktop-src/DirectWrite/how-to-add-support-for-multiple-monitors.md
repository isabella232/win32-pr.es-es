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
# <a name="how-to-add-support-for-multiple-monitors"></a>Cómo agregar compatibilidad para varios monitores

[DirectWrite](direct-write-portal.md) incluye compatibilidad con sistemas con varios monitores. Los distintos monitores pueden tener diferentes geometrías de píxeles (RGB, BGR o FLAT) u otros atributos. Para obtener más información acerca de la geometría de píxeles, vea el tema de referencia de la [**\_ \_ geometría de DWRITE píxeles**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . En este tema se muestra cómo agregar compatibilidad para varios monitores a la aplicación de DirectWrite.

Para admitir varios monitores, debe controlar el mensaje de la ventana de **\_ WINDOWPOSCHANGED de WM** . Este mensaje se envía cuando se mueve la ventana, por lo que debe comprobar si la ventana se ha desactivado en un monitor diferente, tal y como se muestra en el código siguiente.


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



Si la ventana se encuentra en un nuevo monitor, debe crear los parámetros de representación para el nuevo monitor mediante el método [**IDWriteFactory:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .

> [!Note]  
> No use el método [**IDWriteFactory:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para crear los parámetros de representación, ya que siempre crea parámetros para el monitor principal.

 

Cuando tenga un objeto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , establezca los parámetros de representación para el destino de representación mediante el método [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .

Por último, use la función [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para que la ventana se vuelva a dibujar con los nuevos parámetros de representación.

 

 