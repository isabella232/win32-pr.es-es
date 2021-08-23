---
description: Una región de recorte es uno de los objetos gráficos que una aplicación puede seleccionar en un contexto de dispositivo (DC).
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Regiones de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0647d44d82e289b702e9111b62c5a138c8a0fa059428a6173af36f4eeca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105920"
---
# <a name="clipping-regions"></a>Regiones de recorte

Una región de recorte es uno de los objetos gráficos que una aplicación puede seleccionar en un contexto de dispositivo (DC). Normalmente es rectangular. Algunos contextos de dispositivo proporcionan una región de recorte predefinida o predeterminada, mientras que otros no. Por ejemplo, si obtiene un identificador de contexto de dispositivo de la función [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) el controlador de dominio contiene una región de recorte rectangular predefinida que corresponde al rectángulo no válido que requiere volver a dibujar. Sin embargo, cuando se obtiene un identificador de contexto de dispositivo llamando a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) con un parámetro _hWnd_ **NULL** o llamando a la [**función CreateDC,**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) el controlador de dominio no contiene una región de recorte predeterminada. Para obtener más información sobre los contextos de dispositivo devueltos por **la función BeginPaint,** vea [Pintar y dibujar](painting-and-drawing.md) . Para obtener más información sobre los contextos de dispositivo devueltos por las funciones **CreateDC** y **GetDC,** vea [Contextos de dispositivo.](device-contexts.md)

Las aplicaciones pueden realizar diversas operaciones en regiones de recorte. Algunas de estas operaciones requieren un identificador que identifique la región y otras no. Por ejemplo, una aplicación puede realizar las siguientes operaciones directamente en la región de recorte de un contexto de dispositivo.

-   Determine si la salida de gráficos aparece dentro de los bordes de la región pasando las coordenadas de la línea, el arco, el mapa de bits, el texto o la forma rellena correspondientes a la [**función PtVisible.**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)
-   Determine si parte del área de cliente forma una intersección con una región mediante una llamada a [**la función RectVisible.**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)
-   Mueva la región existente por un desplazamiento especificado llamando a la [**función OffsetClipRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)
-   Excluya una parte rectangular del área de cliente de la región de recorte actual mediante una llamada a [**la función ExcludeClipRect.**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)
-   Combine una parte rectangular del área de cliente con la región de recorte actual mediante una llamada a la [**función IntersectClipRect.**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect)

Después de obtener un identificador que identifique la región de recorte, una aplicación puede realizar cualquier operación que sea común con regiones, como:

-   Combinar una copia de la región de recorte actual con una segunda región mediante una llamada a la [**función CombineRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)
-   Compare una copia de la región de recorte actual con una segunda región mediante una llamada a la [**función EqualRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)
-   Determine si un punto se encuentra dentro del interior de una copia de la región de recorte actual llamando a la [**función PtInRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)

 

 



