---
title: Agregar controladores de mensajes de paleta
description: Agregar controladores de mensajes de paleta
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, paletas
- DrawDibRealize función)
- DrawDibDraw función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420676"
---
# <a name="adding-palette-message-handlers"></a>Agregar controladores de mensajes de paleta

En el ejemplo siguiente se muestran los controladores de mensajes simples para los mensajes de [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) y [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) . En el ejemplo se usa la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para procesar el mensaje de **\_ QUERYNEWPALETTE de WM** .

La aplicación debe responder al mensaje [**de \_ QUERYNEWPALETTE de WM**](/windows/desktop/gdi/wm-querynewpalette) invalidando la ventana de destino para permitir que la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) vuelva a dibujar una imagen. Debe responder al mensaje de [**\_ PALETTECHANGED de WM**](/windows/desktop/gdi/wm-palettechanged) mediante la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para obtener la paleta.


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

[Usar DrawDib](using-drawdib.md)
</dt> </dl>

 

 