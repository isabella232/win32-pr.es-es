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
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371852"
---
# <a name="adding-palette-message-handlers"></a>Agregar controladores de mensajes de paleta

En el ejemplo siguiente se muestran controladores de mensajes simples para los mensajes [**\_ WM PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette) En el ejemplo se usa [**la función DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para procesar el **mensaje WM \_ QUERYNEWPALETTE.**

La aplicación debe responder al mensaje [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando la ventana de destino para permitir que la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) vuelva a dibujar una imagen. Debe responder al mensaje [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) mediante la [**función DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para realizar la paleta.


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

 

 