---
title: Dibujar un contexto de presentación
description: Dibujar un contexto de presentación
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib,device context (DC)
- DrawDib,drawing DCs
- Función DrawDibRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476853"
---
# <a name="drawing-a-display-context"></a>Dibujar un contexto de presentación

En el ejemplo siguiente se prepara un controlador de dominio DrawDib mediante la [**función DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) antes de mostrar varias imágenes en una secuencia de mapa de bits.


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

 

 




