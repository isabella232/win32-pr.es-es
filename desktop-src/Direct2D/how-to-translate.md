---
title: Cómo trasladar un objeto
description: Muestra cómo trasladar un objeto.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359291"
---
# <a name="how-to-translate-an-object"></a><span data-ttu-id="30d0b-103">Cómo trasladar un objeto</span><span class="sxs-lookup"><span data-stu-id="30d0b-103">How to Translate an Object</span></span>

<span data-ttu-id="30d0b-104">Para traducir un objeto 2D, mueva el objeto a lo largo del eje x, el eje y o ambos.</span><span class="sxs-lookup"><span data-stu-id="30d0b-104">To translate a 2-D object is to move the object along the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="30d0b-105">Puede llamar a uno de los dos métodos siguientes para crear una transformación de traslación.</span><span class="sxs-lookup"><span data-stu-id="30d0b-105">You can call either one of the following two methods to create a translation transformation.</span></span>

-   <span data-ttu-id="30d0b-106">[**Translation (D2D1 \_ tamaño \_ F tamaño)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): toma un par ordenado que define la distancia que se va a trasladar a lo largo del eje x y el eje y.</span><span class="sxs-lookup"><span data-stu-id="30d0b-106">[**Translation(D2D1\_SIZE\_F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): takes an ordered pair that defines the distance to translate along the x-axis and the y-axis.</span></span>
-   <span data-ttu-id="30d0b-107">[**Translation (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): toma la distancia de la traslación a lo largo del eje x y la distancia que se va a trasladar a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="30d0b-107">[**Translation(float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): takes the distance to translate along the x-axis and the distance to translate along the y-axis.</span></span>

<span data-ttu-id="30d0b-108">El código siguiente crea una matriz de transformación de traslación que mueve las 20 unidades cuadradas a la derecha a lo largo del eje x y 10 unidades hacia abajo a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="30d0b-108">The following code creates a translation transformation matrix that moves the square 20 units to the right along the x-axis and 10 units downward along the y-axis.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="30d0b-109">En la ilustración siguiente se muestra el efecto de aplicar la transformación traslación al cuadrado, donde el cuadrado original es un contorno punteado y el cuadrado traducido es un contorno sólido.</span><span class="sxs-lookup"><span data-stu-id="30d0b-109">The following illustration shows the effect of applying the translation transformation to the square, where the original square is a dotted outline and the translated square is a solid outline.</span></span>

![la ilustración de un cuadrado ha desplazado 20 unidades a la derecha a lo largo del eje x y 10 unidades hacia abajo a lo largo del eje y.](images/translation-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="30d0b-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30d0b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30d0b-112">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="30d0b-112">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="30d0b-113">Información general sobre transformaciones de Direct2D</span><span class="sxs-lookup"><span data-stu-id="30d0b-113">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 