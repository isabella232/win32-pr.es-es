---
title: Cómo recortar con un Axis-Aligned rectángulo de recorte
description: Muestra cómo recortar una región con un rectángulo de recorte alineado con el eje.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559723"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="5c654-103">Cómo recortar con un Axis-Aligned rectángulo de recorte</span><span class="sxs-lookup"><span data-stu-id="5c654-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="5c654-104">En este tema se describe cómo recortar una imagen con un rectángulo de recorte alineado con el eje.</span><span class="sxs-lookup"><span data-stu-id="5c654-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="5c654-105">Este enfoque solo produce clips rectangulares, porque los límites del contenido se alinean con el eje del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5c654-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="5c654-106">Este enfoque es más eficaz que el uso de capas con los límites de contenido.</span><span class="sxs-lookup"><span data-stu-id="5c654-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="5c654-107">Para obtener más información, vea[información general sobre capas](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5c654-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="5c654-108">**Para recortar con un rectángulo de recorte alineado con el eje**</span><span class="sxs-lookup"><span data-stu-id="5c654-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="5c654-109">Cargar la imagen original desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="5c654-109">Load the original image from a resource.</span></span> <span data-ttu-id="5c654-110">Para obtener información sobre cómo cargar un mapa de bits, vea [Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="5c654-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="5c654-111">Llame a [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) para especificar un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5c654-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="5c654-112">Los comandos de representación se recortan al rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5c654-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="5c654-113">Pinte la imagen original.</span><span class="sxs-lookup"><span data-stu-id="5c654-113">Paint the original image.</span></span>
4.  <span data-ttu-id="5c654-114">Llame a [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para quitar el último clip alineado con el eje del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="5c654-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="5c654-115">Por ejemplo, en la siguiente ilustración, el mapa de bits original de la izquierda es 200 \* 130 píxeles.</span><span class="sxs-lookup"><span data-stu-id="5c654-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="5c654-116">El mapa de bits de la derecha es el que se recorta en el rectángulo de recorte alineado por el eje.</span><span class="sxs-lookup"><span data-stu-id="5c654-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="5c654-117">Las dimensiones son (20, 20) a (100, 100).</span><span class="sxs-lookup"><span data-stu-id="5c654-117">The dimensions are (20, 20) to (100, 100).</span></span>

![Ilustración de un mapa de bits de pez antes y después de recortar el mapa de bits](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="5c654-119">Para crear la imagen recortada, cree una estructura de rectángulo como área de recorte.</span><span class="sxs-lookup"><span data-stu-id="5c654-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="5c654-120">Llame a [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) con el área de recorte y dibuje la imagen original.</span><span class="sxs-lookup"><span data-stu-id="5c654-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="5c654-121">Llame a [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para quitar el clip del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="5c654-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="5c654-122">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5c654-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="5c654-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c654-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c654-124">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="5c654-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 