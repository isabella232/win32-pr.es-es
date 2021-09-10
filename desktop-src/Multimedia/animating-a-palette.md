---
title: Animar una paleta
description: Animar una paleta
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib,palettes
- Función DrawDibRealize
- Función DrawDibDraw
- Función DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371857"
---
# <a name="animating-a-palette"></a>Animar una paleta

En el ejemplo siguiente se anima una paleta mediante las funciones [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)y [**DrawDibDraw.**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)

Puede cambiar los colores de un mapa de bits mediante la [**función DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) en combinación con [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette). En primer lugar, para permitir cambios en la paleta, especifique la marca \_ DDF ANIMATE en la llamada a **DrawDibBegin**. En segundo lugar, establezca los valores de la tabla de colores de las entradas de la paleta mediante **DrawDibChangePalette**.

Por ejemplo, si *lppe* es una dirección de la matriz [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) que contiene los nuevos colores y *lpbi* es la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) usada en [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) o [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), el fragmento siguiente actualiza la tabla de colores DIB.


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DrawDib](using-drawdib.md)
</dt> </dl>

 

 