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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371858"
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

 

 




