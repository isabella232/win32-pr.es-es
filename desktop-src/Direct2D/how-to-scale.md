---
title: Cómo escalar un objeto
description: Muestra cómo escalar un objeto.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488078"
---
# <a name="how-to-scale-an-object"></a><span data-ttu-id="3b30e-103">Cómo escalar un objeto</span><span class="sxs-lookup"><span data-stu-id="3b30e-103">How to Scale an Object</span></span>

<span data-ttu-id="3b30e-104">En este tema se describe cómo escalar un objeto mediante la clase [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="3b30e-104">This topic describes how to scale an object by using the [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="3b30e-105">Para escalar un objeto significa que el objeto sea más grande o más pequeño.</span><span class="sxs-lookup"><span data-stu-id="3b30e-105">To scale an object means to make the object larger or smaller.</span></span> <span data-ttu-id="3b30e-106">Puede llamar a uno de los dos métodos siguientes para escalar un objeto.</span><span class="sxs-lookup"><span data-stu-id="3b30e-106">You can call one of the following two methods to scale an object.</span></span>

-   <span data-ttu-id="3b30e-107">**Matrix3x2F:: Scale (D2D1 \_ size \_ F SCALEFACTOR, D2D1 \_ Point \_ 2F CenterPoint)**</span><span class="sxs-lookup"><span data-stu-id="3b30e-107">**Matrix3x2F::Scale(D2D1\_SIZE\_F scalefactor, D2D1\_POINT\_2F centerpoint)**</span></span>
-   <span data-ttu-id="3b30e-108">**Matrix3x2F:: Scale (float scaleX, Float scaleY, D2D1 \_ Point \_ 2F CenterPoint)**</span><span class="sxs-lookup"><span data-stu-id="3b30e-108">**Matrix3x2F::Scale(float scalex, float scaley, D2D1\_POINT\_2F centerpoint)**</span></span>

<span data-ttu-id="3b30e-109">El primer método almacena *scaleX* y *scaleY* como un par ordenado de valores de punto flotante en la estructura de [**tamaño de D2D1 \_ \_ F**](/windows/desktop/Direct2D/d2d1-size-f) .</span><span class="sxs-lookup"><span data-stu-id="3b30e-109">The first method stores *scalex* and *scaley* as an ordered pair of floating-point values in the [**D2D1\_SIZE\_F**](/windows/desktop/Direct2D/d2d1-size-f) structure.</span></span> <span data-ttu-id="3b30e-110">El segundo método define *scaleX* y *scaleY* como parámetros individuales.</span><span class="sxs-lookup"><span data-stu-id="3b30e-110">The second method defines *scalex* and *scaley* as individual parameters.</span></span>

<span data-ttu-id="3b30e-111">Independientemente del método que use, debe especificar los factores de *scaleX* y de *escalado* .</span><span class="sxs-lookup"><span data-stu-id="3b30e-111">Regardless of which method that you use, you must specify both *scalex* and *scaley* factors.</span></span> <span data-ttu-id="3b30e-112">El valor *scaleX* es el factor de escala en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="3b30e-112">The *scalex* value is the scale factor in the x direction.</span></span> <span data-ttu-id="3b30e-113">Por ejemplo, un valor de *scaleX* de 1,5 ajusta el objeto a 150 por ciento a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="3b30e-113">For example, a *scalex* value of 1.5 stretches the object to 150 percent along the x-axis.</span></span> <span data-ttu-id="3b30e-114">Del mismo modo, el valor de *escalado* es el factor de escala en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="3b30e-114">Similarly, the *scaley* value is the scale factor in the y direction.</span></span> <span data-ttu-id="3b30e-115">Por ejemplo, un valor de *escalado* de 0,5 reduce la altura del objeto en un 50 por ciento a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="3b30e-115">For example, a *scaley* value of 0.5 shrinks the height of the object by 50 percent along the y-axis.</span></span>

<span data-ttu-id="3b30e-116">Para especificar un punto como centro de la operación de escalado, use el parámetro *CenterPoint* .</span><span class="sxs-lookup"><span data-stu-id="3b30e-116">To specify a point as the center of the scaling operation, use the *centerpoint* parameter.</span></span> <span data-ttu-id="3b30e-117">De forma predeterminada, un objeto se centra en su origen (0,0).</span><span class="sxs-lookup"><span data-stu-id="3b30e-117">By default, an object is centered about its origin (0,0).</span></span>

<span data-ttu-id="3b30e-118">En el ejemplo de código siguiente se crea una transformación de escala para aumentar el tamaño de un cuadrado al 130% de su tamaño original.</span><span class="sxs-lookup"><span data-stu-id="3b30e-118">The following example code creates a scale transformation to increase the size of a square to 130% of its original size.</span></span> <span data-ttu-id="3b30e-119">El valor de *CenterPoint* se establece en la esquina superior izquierda del cuadrado original.</span><span class="sxs-lookup"><span data-stu-id="3b30e-119">The *centerpoint* is set to be the upper-left corner of the original square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="3b30e-120">En la ilustración siguiente se muestra el efecto de aplicar la transformación de escala al cuadrado.</span><span class="sxs-lookup"><span data-stu-id="3b30e-120">The following illustration shows the effect of applying the scale transformation to the square.</span></span> <span data-ttu-id="3b30e-121">El cuadrado original es un contorno punteado y el cuadrado en escala es un contorno sólido.</span><span class="sxs-lookup"><span data-stu-id="3b30e-121">The original square is a dotted outline and the scaled square is a solid outline.</span></span>

![Ilustración de tamaño cuadrado cambiado al 130% de su tamaño original](images/scale-ovw.png)

## <a name="related-topics"></a><span data-ttu-id="3b30e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b30e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b30e-124">Información general sobre transformaciones de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3b30e-124">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="3b30e-125">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3b30e-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 