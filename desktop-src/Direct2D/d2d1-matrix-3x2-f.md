---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Representa una matriz de 3 por 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676659"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="de545-104">D2D1 \_ Matrix \_ 3x2 \_ F</span><span class="sxs-lookup"><span data-stu-id="de545-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="de545-105">Representa una matriz de 3 por 2.</span><span class="sxs-lookup"><span data-stu-id="de545-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="de545-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de545-106">Remarks</span></span>

<span data-ttu-id="de545-107">**D2D1 \_ MATRIX \_ 3x2** es un nombre nuevo para la estructura de la [**matriz de D2D \_ \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="de545-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="de545-108">Para obtener una lista de los campos que proporciona la matriz, vea [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="de545-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="de545-109">Para simplificar las operaciones de matriz comunes, Direct2D proporciona la clase [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , que se deriva de la estructura 3x2 de la [**\_ matriz \_ D2D1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="de545-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="de545-110">La clase **Matrix3x2F** proporciona un conjunto de métodos auxiliares para realizar tareas comunes, como la creación de una matriz de traslación o sesgo.</span><span class="sxs-lookup"><span data-stu-id="de545-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="de545-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="de545-111">Examples</span></span>

<span data-ttu-id="de545-112">En el ejemplo siguiente se usa el método [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) para crear una matriz de rotación que gira un cuadrado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado y pasa la matriz al método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) del destino de representación (*m \_ pRenderTarget*).</span><span class="sxs-lookup"><span data-stu-id="de545-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="de545-113">En la ilustración siguiente se muestra el efecto de aplicar la transformación rotación anterior al cuadrado.</span><span class="sxs-lookup"><span data-stu-id="de545-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="de545-114">El cuadrado original es un contorno punteado y el cuadrado girado es un contorno sólido.</span><span class="sxs-lookup"><span data-stu-id="de545-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![Ilustración de un cuadrado girado en el sentido de las agujas del reloj 45 grados sobre el centro del cuadrado original](images/rotate-ovw.png)


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



<span data-ttu-id="de545-116">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="de545-116">Code has been omitted from this example.</span></span> <span data-ttu-id="de545-117">Para obtener más información sobre las transformaciones, vea [información general sobre transformaciones](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de545-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de545-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de545-118">Requirements</span></span>



| <span data-ttu-id="de545-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de545-119">Requirement</span></span> | <span data-ttu-id="de545-120">Value</span><span class="sxs-lookup"><span data-stu-id="de545-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de545-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de545-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de545-122">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="de545-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="de545-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de545-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de545-124">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="de545-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="de545-125">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de545-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="de545-126">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="de545-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="de545-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de545-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="de545-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="de545-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="de545-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="de545-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de545-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="de545-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="de545-131">Información general sobre transformaciones</span><span class="sxs-lookup"><span data-stu-id="de545-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="de545-132">Cómo girar un objeto</span><span class="sxs-lookup"><span data-stu-id="de545-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="de545-133">Cómo escalar un objeto</span><span class="sxs-lookup"><span data-stu-id="de545-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="de545-134">Cómo sesgar un objeto</span><span class="sxs-lookup"><span data-stu-id="de545-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="de545-135">Cómo trasladar un objeto</span><span class="sxs-lookup"><span data-stu-id="de545-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="de545-136">**D2D \_ Matrix \_ 3x2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="de545-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

