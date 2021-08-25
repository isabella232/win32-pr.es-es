---
title: Cómo agregar compatibilidad con varios monitores
description: DirectWrite compatibilidad con sistemas con varios monitores.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048895"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Cómo agregar compatibilidad con varios monitores

[DirectWrite](direct-write-portal.md) compatibilidad con sistemas con varios monitores. Los distintos monitores pueden tener diferentes geometrías de píxeles (RGB, BGR o FLAT) u otros atributos. Para obtener más información sobre la geometría de píxeles, vea el tema [**de referencia DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) En este tema se muestra cómo agregar compatibilidad con varios monitores a la DirectWrite aplicación.

Para admitir varios monitores, debe controlar el mensaje **de ventana WM \_ WINDOWPOSCHANGED.** Este mensaje se envía cuando se mueve la ventana, por lo que debe comprobar si la ventana se ha movido a un monitor diferente, como se muestra en el código siguiente.


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



Si la ventana se encuentra en un nuevo monitor, debe crear parámetros de representación para el nuevo monitor mediante el método [**IDWriteFactory::CreateMonitorRenderingParams.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams)

> [!Note]  
> No use el [**método IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para crear los parámetros de representación, ya que siempre crea parámetros para el monitor principal.

 

Cuando tenga un objeto [**IDWriteRenderingParams,**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) establezca los parámetros de representación para el destino de representación mediante el [**método ID2DRenderTarget::SetTextRenderingParams.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams)

Por último, use [**la función InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para hacer que la ventana se vuelva a dibujar con los nuevos parámetros de representación.

 

 