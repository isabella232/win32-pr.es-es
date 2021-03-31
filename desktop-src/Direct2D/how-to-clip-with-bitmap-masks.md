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
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="a09aa-103">Cómo usar un mapa de bits como máscara de opacidad</span><span class="sxs-lookup"><span data-stu-id="a09aa-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="a09aa-104">En este tema se describe cómo usar un mapa de bits como máscara opacty llamando al método [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) .</span><span class="sxs-lookup"><span data-stu-id="a09aa-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="a09aa-105">La máscara de opacidad es un mapa de bits que proporciona la información de cobertura que está representada por el canal alfa, que controla la transparencia del contenido que se representa.</span><span class="sxs-lookup"><span data-stu-id="a09aa-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="a09aa-106">Este enfoque es más eficaz que el uso de capas con una máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="a09aa-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="a09aa-107">Para obtener más información, vea [información general sobre capas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a09aa-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="a09aa-108">**Para recortar una región**</span><span class="sxs-lookup"><span data-stu-id="a09aa-108">**To clip a region**</span></span>

1.  <span data-ttu-id="a09aa-109">Cargar el mapa de bits original desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="a09aa-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="a09aa-110">Para obtener información sobre cómo cargar un mapa de bits, vea [Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="a09aa-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="a09aa-111">Carga de la máscara de mapa de bits desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="a09aa-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="a09aa-112">Cree un pincel de mapa de bits con el mapa de bits original.</span><span class="sxs-lookup"><span data-stu-id="a09aa-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="a09aa-113">Para obtener información sobre cómo crear un pincel de mapa de bits, vea [Cómo crear un pincel de mapa de bits](how-to-create-a-bitmap-brush.md).</span><span class="sxs-lookup"><span data-stu-id="a09aa-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="a09aa-114">Llame a [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias en el destino de representación en el \_ modo antialias D2D1 con \_ \_ alias para [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) para que funcione.</span><span class="sxs-lookup"><span data-stu-id="a09aa-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="a09aa-115">Llame a [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) con la máscara de mapa de bits y el pincel de mapa de bits en el destino de presentación para rellenar el clip.</span><span class="sxs-lookup"><span data-stu-id="a09aa-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="a09aa-116">En la ilustración siguiente se muestra el mapa de bits original de la izquierda, la máscara de mapa de bits en el centro y el mapa de bits que se recorta a la máscara de la derecha.</span><span class="sxs-lookup"><span data-stu-id="a09aa-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![Ilustración de un mapa de bits de pez, una máscara de forma de pescado que se crea a partir del mapa de bits y el mapa de bits resultante en forma de pez después de la máscara](images/cliparegion-opacitymask.png)

<span data-ttu-id="a09aa-118">En el código siguiente se muestra cómo recortar la región con la máscara que se muestra en la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="a09aa-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="a09aa-119">Primero carga el mapa de bits original y la máscara de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a09aa-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="a09aa-120">Y, a continuación, crea un pincel de mapa de bits con el mapa de bits original.</span><span class="sxs-lookup"><span data-stu-id="a09aa-120">And then creates a bitmap brush with the original bitmap.</span></span>


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



<span data-ttu-id="a09aa-121">A continuación, llama a [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para establecer el modo antialias.</span><span class="sxs-lookup"><span data-stu-id="a09aa-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="a09aa-122">Llame a [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) para usar una máscara de mapa de bits para recortar el mapa de bits original.</span><span class="sxs-lookup"><span data-stu-id="a09aa-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


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



<span data-ttu-id="a09aa-123">Para obtener más información sobre las máscaras de opacidad, consulte [información general](opacity-masks-overview.md)sobre las máscaras de opacidad.</span><span class="sxs-lookup"><span data-stu-id="a09aa-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a09aa-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a09aa-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a09aa-125">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="a09aa-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 