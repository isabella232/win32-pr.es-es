---
title: Cómo crear un pincel de mapa de bits
description: Muestra cómo crear un pincel de mapa de bits mediante Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676441"
---
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="9ba72-103">Cómo crear un pincel de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="9ba72-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="9ba72-104">Para crear un pincel de mapa de bits, use el método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique las propiedades de pincel de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="9ba72-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="9ba72-105">Algunas sobrecargas le permiten especificar las propiedades del pincel.</span><span class="sxs-lookup"><span data-stu-id="9ba72-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="9ba72-106">En el código siguiente se muestra cómo crear un pincel de mapa de bits para rellenar un cuadrado y un pincel negro sólido para dibujar el contorno del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="9ba72-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="9ba72-107">El código genera el resultado que se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9ba72-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="9ba72-108">A partir de Windows 8, puede usar el método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) de la interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para crear un [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) en lugar de un **ID2D1BitmapBrush**.</span><span class="sxs-lookup"><span data-stu-id="9ba72-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="9ba72-109">**ID2D1BitmapBrush1** agrega modos de escalado de alta calidad al pincel de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="9ba72-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![captura de pantalla de un cuadrado relleno con un mapa de bits de planta](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="9ba72-111">Declare una variable de tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="9ba72-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="9ba72-112">Cargar un mapa de bits desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="9ba72-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="9ba72-113">Para obtener más información, vea [Cómo cargar un mapa de bits desde un recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="9ba72-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  <span data-ttu-id="9ba72-114">Elija los modos de extensión [**( \_ \_ modo de extensión de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) y el modo de interpolación ([**\_ \_ \_ modo de interpolación de mapas de bits D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) del pincel de mapa de bits y, a continuación, llame al método [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para crear un pincel, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="9ba72-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9ba72-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ba72-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ba72-116">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="9ba72-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 