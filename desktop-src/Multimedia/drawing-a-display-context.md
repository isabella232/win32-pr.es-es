---
title: Dibujar un contexto de presentación
description: Dibujar un contexto de presentación
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib, contexto de dispositivo (DC)
- DrawDib,drawing DCs
- Función DrawDibRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f10d533fff97064ba3c6a081a2f1d0aaa9e1b72011f2baa1ac3a6bd1a81d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678725"
---
# <a name="drawing-a-display-context"></a>Dibujar un contexto de presentación

En el ejemplo siguiente se prepara un controlador de dominio DrawDib mediante la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) antes de mostrar varias imágenes en una secuencia de mapa de bits.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DrawDib](using-drawdib.md)
</dt> </dl>

 

 




