---
title: Dibujar un contexto de presentación
description: Dibujar un contexto de presentación
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- DrawDib, contexto de dispositivo (DC)
- DrawDib, dibujar controladores de DC
- DrawDibRealize función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075690"
---
# <a name="drawing-a-display-context"></a><span data-ttu-id="a367f-106">Dibujar un contexto de presentación</span><span class="sxs-lookup"><span data-stu-id="a367f-106">Drawing a Display Context</span></span>

<span data-ttu-id="a367f-107">En el ejemplo siguiente se prepara un controlador de dominio de DrawDib mediante la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) antes de mostrar varias imágenes en una secuencia de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a367f-107">The following example prepares a DrawDib DC by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function prior to displaying several images in a bitmap sequence.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a367f-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a367f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a367f-109">Usar DrawDib</span><span class="sxs-lookup"><span data-stu-id="a367f-109">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 




