---
title: Cómo usar un mapa de bits como máscara de opacidad
description: Muestra cómo recortar una región con máscaras de mapa de bits.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163205"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Cómo usar un mapa de bits como máscara de opacidad

En este tema se describe cómo usar un mapa de bits como una máscara de opacidad llamando al [**método ID2D1Factory::FillOpacityMask.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) La máscara de opacidad es un mapa de bits que proporciona la información de cobertura representada por el canal alfa, que controla la transparencia del contenido representado. Este enfoque es más eficaz que usar capas con una máscara de opacidad. Para obtener más información, vea [Información general sobre capas.](direct2d-layers-overview.md)

**Para recortar una región**

1.  Cargue el mapa de bits original desde un recurso. Para obtener información sobre cómo cargar un mapa de bits, [vea How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).
2.  Cargue la máscara de mapa de bits desde un recurso.
3.  Cree un pincel de mapa de bits con el mapa de bits original. Para obtener información sobre cómo crear un pincel de mapa de bits, [vea How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).
4.  Llame [**a ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias en el destino de representación en D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED para que [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) funcione.
5.  Llame [**a FillOpacityMask con**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) la máscara de mapa de bits y el pincel de mapa de bits en el destino de representación para rellenar el clip.

En la ilustración siguiente se muestra el mapa de bits original a la izquierda, la máscara de mapa de bits en el centro y el mapa de bits recortado a la máscara de la derecha.

![ilustración de un mapa de bits goldfish, una máscara en forma de fondo que se crea a partir del mapa de bits y el mapa de bits resultante en forma de objeto después de la máscara](images/cliparegion-opacitymask.png)

El código siguiente muestra cómo recortar la región con la máscara que se muestra en la ilustración anterior. Primero carga el mapa de bits original y la máscara de mapa de bits. A continuación, crea un pincel de mapa de bits con el mapa de bits original.


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



A continuación, [**llama a SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias. Llame [**a FillOpacityMask para**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) usar una máscara de mapa de bits para recortar el mapa de bits original.


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



Para obtener más información sobre las máscaras de opacidad, vea [Información general sobre las máscaras de opacidad.](opacity-masks-overview.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 