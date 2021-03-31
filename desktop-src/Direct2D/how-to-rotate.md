---
title: Cómo girar un objeto
description: Muestra cómo girar un objeto.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995452"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="812fc-103">Cómo girar un objeto</span><span class="sxs-lookup"><span data-stu-id="812fc-103">How to Rotate an Object</span></span>

<span data-ttu-id="812fc-104">En este tema se describe cómo girar un objeto sobre un punto especificado.</span><span class="sxs-lookup"><span data-stu-id="812fc-104">This topic describes how to rotate an object about a specified point.</span></span> <span data-ttu-id="812fc-105">Para girar un objeto, llame al método [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) .</span><span class="sxs-lookup"><span data-stu-id="812fc-105">To rotate an object, call [**Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method.</span></span> <span data-ttu-id="812fc-106">Este método toma dos parámetros, el ángulo especificado y el punto central.</span><span class="sxs-lookup"><span data-stu-id="812fc-106">This method takes two parameters, the specified angle and the center point.</span></span> <span data-ttu-id="812fc-107">El ángulo es un ángulo de rotación en el sentido de las agujas del reloj, en grados, y el punto central es el punto sobre el que gira el objeto.</span><span class="sxs-lookup"><span data-stu-id="812fc-107">The angle is a clockwise rotation angle in degrees, and the center point is the point about which the object rotates.</span></span> <span data-ttu-id="812fc-108">El punto central se expresa en el sistema de coordenadas del objeto que se transforma.</span><span class="sxs-lookup"><span data-stu-id="812fc-108">The center point is expressed in the coordinate system of the object that is transformed.</span></span>

<span data-ttu-id="812fc-109">Por ejemplo, en el código siguiente se gira un cuadrado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado.</span><span class="sxs-lookup"><span data-stu-id="812fc-109">For example, the following code rotates a square clockwise 45 degrees about the center of the square.</span></span>


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="812fc-110">En la ilustración siguiente se muestra el efecto de aplicar la transformación rotación anterior al cuadrado.</span><span class="sxs-lookup"><span data-stu-id="812fc-110">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="812fc-111">El cuadrado original es un contorno punteado y el cuadrado girado es un contorno sólido.</span><span class="sxs-lookup"><span data-stu-id="812fc-111">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado original](images/rotate-ovw.png)

<span data-ttu-id="812fc-113">En la ilustración siguiente se muestra el efecto de girar en el mismo ángulo sobre un punto central diferente.</span><span class="sxs-lookup"><span data-stu-id="812fc-113">The following illustration shows the effect of rotating by the same angle about a different center point.</span></span> <span data-ttu-id="812fc-114">Observe que los objetos girados se encuentran en posiciones diferentes en relación con el original.</span><span class="sxs-lookup"><span data-stu-id="812fc-114">Notice that the rotated objects are in different positions relative to the original.</span></span> <span data-ttu-id="812fc-115">El cuadrado de la izquierda es el resultado de girar sobre el centro del cuadrado original y el cuadrado de la derecha es el resultado de girar sobre la esquina superior izquierda del cuadrado original.</span><span class="sxs-lookup"><span data-stu-id="812fc-115">The left outlined square is the result of rotating about the center of the original square, and the right outlined square is the result of rotating about the upper-left corner of the original square.</span></span>

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre un punto central diferente](images/translate-rotationcompare.png)

## <a name="related-topics"></a><span data-ttu-id="812fc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="812fc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="812fc-118">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="812fc-118">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="812fc-119">Información general sobre transformaciones de Direct2D</span><span class="sxs-lookup"><span data-stu-id="812fc-119">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 