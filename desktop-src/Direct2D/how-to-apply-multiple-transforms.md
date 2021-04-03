---
title: Cómo aplicar varias transformaciones a un objeto
description: Muestra cómo aplicar varias transformaciones a un objeto.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773897"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="3f35c-103">Cómo aplicar varias transformaciones a un objeto</span><span class="sxs-lookup"><span data-stu-id="3f35c-103">How to Apply Multiple Transforms to an Object</span></span>

<span data-ttu-id="3f35c-104">Para realizar varias transformaciones en un objeto significa combinar varias transformaciones en una.</span><span class="sxs-lookup"><span data-stu-id="3f35c-104">To perform multiple transforms on an object means to combine several transforms into one.</span></span> <span data-ttu-id="3f35c-105">Es decir, se toma la salida de cada matriz de transformación y se usa como entrada para el siguiente, con lo que se obtienen los efectos acumulativos de todas las transformaciones de matriz.</span><span class="sxs-lookup"><span data-stu-id="3f35c-105">That is, taking the output from each transformation matrix and using it as the input for the next, thereby getting the cumulative effects of all the matrix transformations.</span></span>

<span data-ttu-id="3f35c-106">Supongamos que se multiplican dos matrices de transformación, rotación y traslación.</span><span class="sxs-lookup"><span data-stu-id="3f35c-106">Suppose two transformation matrices, rotation and translation, are multiplied together.</span></span> <span data-ttu-id="3f35c-107">El resultado es una nueva matriz que realiza las funciones de giro y traslación.</span><span class="sxs-lookup"><span data-stu-id="3f35c-107">The result is a new matrix that performs the functions of both rotation and translation.</span></span> <span data-ttu-id="3f35c-108">Dado que la multiplicación de matrices no es conmutativa, una transformación de giro multiplicada por una transformación de traslación es diferente de la transformación de traslación multiplicada por la transformación de giro.</span><span class="sxs-lookup"><span data-stu-id="3f35c-108">Because matrix multiplication is not commutative, a rotation transformation multiplied by a translation transformation is different from the translation transformation multiplied by the rotation transformation.</span></span>

<span data-ttu-id="3f35c-109">En los siguientes ejemplos de código se muestra cómo aplicar la rotación seguido de la traducción y, a continuación, la traslación seguido de la rotación.</span><span class="sxs-lookup"><span data-stu-id="3f35c-109">The following code examples show how to apply rotation followed by translation, and then translation followed by rotation.</span></span> <span data-ttu-id="3f35c-110">Observe que los resultados de la representación son diferentes.</span><span class="sxs-lookup"><span data-stu-id="3f35c-110">Notice that the rendering results are different.</span></span>


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



<span data-ttu-id="3f35c-111">El código genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="3f35c-111">The code produces the output shown in the following illustration.</span></span>

![Ilustración de un rectángulo que se ha traducido y girado, y un rectángulo que se ha girado y convertido](images/multipletransforms.png)

## <a name="related-topics"></a><span data-ttu-id="3f35c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f35c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f35c-114">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3f35c-114">Direct2D Reference</span></span>](reference.md)
</dt> <dt>

[<span data-ttu-id="3f35c-115">Información general sobre transformaciones de Direct2D</span><span class="sxs-lookup"><span data-stu-id="3f35c-115">Direct2D Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> </dl>

 

 




