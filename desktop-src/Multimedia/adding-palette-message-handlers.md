---
title: Agregar controladores de mensajes de paleta
description: Agregar controladores de mensajes de paleta
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib,palettes
- Función DrawDibRealize
- Función DrawDibDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b17512025cadf0e457b596a3bfc07399db4eb9185195f4c836ee154d5ff64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808635"
---
# <a name="adding-palette-message-handlers"></a>Agregar controladores de mensajes de paleta

En el ejemplo siguiente se muestran controladores de mensajes simples para los mensajes [**\_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette) En el ejemplo se usa [**la función DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para procesar el **mensaje WM \_ QUERYNEWPALETTE.**

La aplicación debe responder al mensaje [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando la ventana de destino para permitir que la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) vuelva a dibujar una imagen. Debe responder al mensaje [**\_ PALETTECHANGED de WM**](/windows/desktop/gdi/wm-palettechanged) mediante la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para realizar la paleta.


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DrawDib](using-drawdib.md)
</dt> </dl>

 

 