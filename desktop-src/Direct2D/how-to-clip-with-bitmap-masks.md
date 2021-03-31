---
title: Cómo usar un mapa de bits como máscara de opacidad
description: Muestra cómo recortar una región con máscaras de mapa de bits.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995499"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Cómo usar un mapa de bits como máscara de opacidad

En este tema se describe cómo usar un mapa de bits como máscara opacty llamando al método [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) . La máscara de opacidad es un mapa de bits que proporciona la información de cobertura que está representada por el canal alfa, que controla la transparencia del contenido que se representa. Este enfoque es más eficaz que el uso de capas con una máscara de opacidad. Para obtener más información, vea [información general sobre capas](direct2d-layers-overview.md).

**Para recortar una región**

1.  Cargar el mapa de bits original desde un recurso. Para obtener información sobre cómo cargar un mapa de bits, vea [Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md).
2.  Carga de la máscara de mapa de bits desde un recurso.
3.  Cree un pincel de mapa de bits con el mapa de bits original. Para obtener información sobre cómo crear un pincel de mapa de bits, vea [Cómo crear un pincel de mapa de bits](how-to-create-a-bitmap-brush.md).
4.  Llame a [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias en el destino de representación en el \_ modo antialias D2D1 con \_ \_ alias para [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) para que funcione.
5.  Llame a [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) con la máscara de mapa de bits y el pincel de mapa de bits en el destino de presentación para rellenar el clip.

En la ilustración siguiente se muestra el mapa de bits original de la izquierda, la máscara de mapa de bits en el centro y el mapa de bits que se recorta a la máscara de la derecha.

![Ilustración de un mapa de bits de pez, una máscara de forma de pescado que se crea a partir del mapa de bits y el mapa de bits resultante en forma de pez después de la máscara](images/cliparegion-opacitymask.png)

En el código siguiente se muestra cómo recortar la región con la máscara que se muestra en la ilustración anterior. Primero carga el mapa de bits original y la máscara de mapa de bits. Y, a continuación, crea un pincel de mapa de bits con el mapa de bits original.


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



A continuación, llama a [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias. Llame a [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) para usar una máscara de mapa de bits para recortar el mapa de bits original.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Para obtener más información sobre las máscaras de opacidad, consulte [información general](opacity-masks-overview.md)sobre las máscaras de opacidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 