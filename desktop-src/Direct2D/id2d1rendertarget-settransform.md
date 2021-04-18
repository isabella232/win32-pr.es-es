---
title: Métodos ID2D1RenderTarget SetTransform
description: Aplica la transformación especificada al destino de representación, reemplazando la transformación existente. Todas las operaciones de dibujo posteriores se producen en el espacio transformado.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Métodos de SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661375"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="c869e-105">ID2D1RenderTarget:: SetTransform (métodos)</span><span class="sxs-lookup"><span data-stu-id="c869e-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="c869e-106">Aplica la transformación especificada al destino de representación, reemplazando la transformación existente.</span><span class="sxs-lookup"><span data-stu-id="c869e-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="c869e-107">Todas las operaciones de dibujo posteriores se producen en el espacio transformado.</span><span class="sxs-lookup"><span data-stu-id="c869e-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c869e-108">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="c869e-108">Overload list</span></span>



| <span data-ttu-id="c869e-109">Método</span><span class="sxs-lookup"><span data-stu-id="c869e-109">Method</span></span>                                                                                              | <span data-ttu-id="c869e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c869e-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c869e-111">[**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="c869e-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="c869e-112">Aplica la transformación especificada al destino de representación, reemplazando la transformación existente.</span><span class="sxs-lookup"><span data-stu-id="c869e-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="c869e-113">Todas las operaciones de dibujo posteriores se producen en el espacio transformado.</span><span class="sxs-lookup"><span data-stu-id="c869e-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="c869e-114">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="c869e-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="c869e-115">Aplica la transformación especificada al destino de representación, reemplazando la transformación existente.</span><span class="sxs-lookup"><span data-stu-id="c869e-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="c869e-116">Todas las operaciones de dibujo posteriores se producen en el espacio transformado.</span><span class="sxs-lookup"><span data-stu-id="c869e-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="c869e-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c869e-117">Examples</span></span>

<span data-ttu-id="c869e-118">En el ejemplo siguiente se usa el método **SetTransform** para aplicar un giro al destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c869e-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="c869e-119">Para obtener el ejemplo completo, consulte [cómo girar un objeto](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="c869e-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="c869e-120">Para obtener ejemplos adicionales que muestran cómo transformar un destino de representación, vea [Cómo escalar un objeto](how-to-scale.md), [Cómo sesgar un objeto](how-to-skew.md)y [Cómo trasladar un objeto](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="c869e-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c869e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c869e-121">Requirements</span></span>



| <span data-ttu-id="c869e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c869e-122">Requirement</span></span> | <span data-ttu-id="c869e-123">Value</span><span class="sxs-lookup"><span data-stu-id="c869e-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c869e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c869e-124">Library</span></span><br/> | <dl> <span data-ttu-id="c869e-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c869e-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="c869e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c869e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c869e-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c869e-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c869e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c869e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c869e-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="c869e-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="c869e-130">Información general sobre transformaciones</span><span class="sxs-lookup"><span data-stu-id="c869e-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="c869e-131">Cómo girar un objeto</span><span class="sxs-lookup"><span data-stu-id="c869e-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="c869e-132">Cómo escalar un objeto</span><span class="sxs-lookup"><span data-stu-id="c869e-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="c869e-133">Cómo sesgar un objeto</span><span class="sxs-lookup"><span data-stu-id="c869e-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="c869e-134">Cómo trasladar un objeto</span><span class="sxs-lookup"><span data-stu-id="c869e-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="c869e-135">Cómo aplicar varias transformaciones a un objeto</span><span class="sxs-lookup"><span data-stu-id="c869e-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

