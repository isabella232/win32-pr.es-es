---
title: Cómo recortar con un rectángulo Axis-Aligned clip
description: Muestra cómo recortar una región con un rectángulo de recorte alineado con el eje.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163206"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Cómo recortar con un rectángulo Axis-Aligned clip

En este tema se describe cómo recortar una imagen con un rectángulo de recorte alineado con el eje. Este enfoque genera solo clips rectangulares, ya que los límites de contenido se alinean con el eje del rectángulo. Este enfoque es más eficaz que usar capas con los límites de contenido. Para obtener más información, vea[Información general sobre capas.](direct2d-layers-overview.md)

**Para recortar con un rectángulo de recorte alineado con el eje**

1.  Cargue la imagen original desde un recurso. Para obtener información sobre cómo cargar un mapa de bits, [vea How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).
2.  Llame [**a ID2D1RenderTarget::P ushAxisAlignedClip para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) especificar un rectángulo. Los comandos de representación se recortan al rectángulo.

3.  Paint la imagen original.
4.  Llame [**a ID2D1RenderTarget::P opAxisAlignedClip para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) quitar el último clip alineado con el eje del destino de representación.

Por ejemplo, en la ilustración siguiente, el mapa de bits original de la izquierda es de 200 \* 130 píxeles. El mapa de bits de la derecha es el mapa de bits original recortado al rectángulo de recorte alineado con el eje. Las dimensiones son (20, 20) a (100, 100).

![ilustración de un mapa de bits goldfish antes y después de recortar el mapa de bits](images/cliparegion-axisalignedclip.png)

Para crear la imagen recortada, cree una estructura de rectángulo como área de recorte. Llame [**a PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) con el área de recorte y pinte la imagen original. Llame [**a PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para quitar el clip del destino de representación. El código siguiente muestra cómo hacerlo.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 