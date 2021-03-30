---
title: Cómo sesgar un objeto
description: Muestra cómo sesgar un objeto.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904757"
---
# <a name="how-to-skew-an-object"></a><span data-ttu-id="3829f-103">Cómo sesgar un objeto</span><span class="sxs-lookup"><span data-stu-id="3829f-103">How to Skew an Object</span></span>

<span data-ttu-id="3829f-104">Para sesgar (o distorsionar) un objeto significa distorsionar un objeto en un ángulo especificado desde el eje x, el eje y o ambos.</span><span class="sxs-lookup"><span data-stu-id="3829f-104">To skew (or shear) an object means to distort an object by a specified angle from the x-axis, the y-axis, or both.</span></span> <span data-ttu-id="3829f-105">Por ejemplo, al sesgar un cuadrado, se convierte en un paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="3829f-105">For example, when you skew a square, it becomes a parallelogram.</span></span>

<span data-ttu-id="3829f-106">El método [**Matrix3x2F:: Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) toma 3 parámetros:</span><span class="sxs-lookup"><span data-stu-id="3829f-106">The [**Matrix3x2F::Skew**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) method takes 3 parameters:</span></span>

-   <span data-ttu-id="3829f-107">*angleX*: ángulo de sesgado del eje x, que se mide en grados en sentido contrario a las agujas del reloj desde el eje y.</span><span class="sxs-lookup"><span data-stu-id="3829f-107">*angleX*: The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.</span></span>
-   <span data-ttu-id="3829f-108">*ánguloy*: el ángulo de sesgado del eje y, que se mide en grados en el sentido de las agujas del reloj desde el eje x.</span><span class="sxs-lookup"><span data-stu-id="3829f-108">*angleY*: The y-axis skew angle, which is measured in degrees clockwise from the x-axis.</span></span>
-   <span data-ttu-id="3829f-109">*centerPoint*: el punto sobre el que se realiza el sesgo.</span><span class="sxs-lookup"><span data-stu-id="3829f-109">*centerPoint*: The point about which the skew is performed.</span></span>

<span data-ttu-id="3829f-110">Para predecir el efecto de una transformación de sesgo, tenga en cuenta que *angleX* es el ángulo de sesgo medido en grados en sentido contrario a las agujas del reloj desde el eje y.</span><span class="sxs-lookup"><span data-stu-id="3829f-110">To predict the effect of a skew transformation, consider that *angleX* is the skew angle measured in degrees counterclockwise from the y-axis.</span></span> <span data-ttu-id="3829f-111">Por ejemplo, si *angleX* se establece en 30, el objeto sesga 30 grados en sentido contrario a las agujas del reloj a lo largo del eje y sobre *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="3829f-111">For example, if *angleX* is set to 30, the object skews 30 degrees counterclockwise along the y-axis about the *centerPoint*.</span></span> <span data-ttu-id="3829f-112">En la ilustración siguiente se muestra un cuadrado sesgado horizontalmente 30 grados sobre la esquina superior izquierda del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="3829f-112">The following illustration shows a square skewed horizontally 30 degrees about the upper-left corner of the square.</span></span>

![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y](images/skewx.png)

<span data-ttu-id="3829f-114">Del mismo modo, el *ángulo* es un ángulo de sesgo medido en grados en el sentido de las agujas del reloj desde el eje x.</span><span class="sxs-lookup"><span data-stu-id="3829f-114">Similarly, *angleY* is a skew angle measured in degrees clockwise from the x-axis.</span></span> <span data-ttu-id="3829f-115">Por ejemplo, si el *ángulo* está establecido en 30, el objeto sesga 30 grados en el sentido de las agujas del reloj a lo largo del eje x sobre el *centerPoint*.</span><span class="sxs-lookup"><span data-stu-id="3829f-115">For example, if *angleY* is set to 30, the object skews 30 degrees clockwise along the x-axis about the *centerPoint*.</span></span> <span data-ttu-id="3829f-116">En la ilustración siguiente se muestra un cuadrado sesgado en vertical 30 grados sobre la esquina superior izquierda del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="3829f-116">The following illustration shows a square skewed vertically 30 degrees about the upper-left corner of the square.</span></span>

![Ilustración de un cuadrado sesgado de 30 grados en el sentido de las agujas del reloj desde el eje x](images/skewy.png)

<span data-ttu-id="3829f-118">Si establece tanto *angleX* como *angular* en 30 grados y el *centerPoint* en la esquina superior izquierda del cuadrado, verá el cuadrado sesgado siguiente (con un contorno sólido).</span><span class="sxs-lookup"><span data-stu-id="3829f-118">If you set both *angleX* and *angleY* to 30 degrees, and the *centerPoint* to the upper-left corner of the square, you will see the following skewed square (solid outlined).</span></span> <span data-ttu-id="3829f-119">Observe que el cuadrado sesgado está sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y y 30 grados en el sentido de las agujas del reloj desde el eje x.</span><span class="sxs-lookup"><span data-stu-id="3829f-119">Notice that the skewed square is skewed 30 degrees counterclockwise from the y-axis and 30 degrees clockwise from the x-axis.</span></span>

![Ilustración de un cuadrado sesgado de 30 grados en sentido contrario a las agujas del reloj desde el eje y y 30 grados en el sentido de las agujas del reloj desde el eje x](images/skewxy.png)

<span data-ttu-id="3829f-121">En el ejemplo de código siguiente se sesga el cuadrado 45 grados horizontalmente sobre la esquina superior izquierda del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="3829f-121">The following code example skews the square 45 degrees horizontally about the upper-left corner of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="3829f-122">En la ilustración siguiente se muestra el efecto de aplicar la transformación sesgado al cuadrado, donde el cuadrado original es un contorno punteado y el objeto sesgado (paralelogramo) es un contorno sólido.</span><span class="sxs-lookup"><span data-stu-id="3829f-122">The following illustration shows the effect of applying the skew transformation to the square, where the original square is a dotted outline and the skewed object (parallelogram) is a solid outline.</span></span> <span data-ttu-id="3829f-123">Observe que el ángulo de sesgo es de 45 grados en sentido contrario a las agujas del reloj desde el eje y.</span><span class="sxs-lookup"><span data-stu-id="3829f-123">Notice that the skew angle is 45 degrees counterclockwise from the y-axis.</span></span>

![Ilustración de un cuadrado sesgado de 45 grados en sentido contrario a las agujas del reloj desde el eje y](images/skew-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="3829f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3829f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3829f-126">Información general sobre transformaciones de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3829f-126">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="3829f-127">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3829f-127">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 