---
title: Métodos ID2D1Factory CreateTransformedGeometry (D2d1. h)
description: Transforma la geometría especificada y almacena el resultado como un objeto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Métodos de CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679197"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="79050-104">ID2D1Factory:: CreateTransformedGeometry (métodos)</span><span class="sxs-lookup"><span data-stu-id="79050-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="79050-105">Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="79050-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="79050-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="79050-106">Overload list</span></span>



| <span data-ttu-id="79050-107">Método</span><span class="sxs-lookup"><span data-stu-id="79050-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="79050-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="79050-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79050-109">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79050-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="79050-110">Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="79050-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="79050-111">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="79050-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="79050-112">Transforma la geometría especificada y almacena el resultado como un objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="79050-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="79050-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79050-113">Remarks</span></span>

<span data-ttu-id="79050-114">Al igual que otros recursos, una geometría transformada hereda el espacio de recursos y la Directiva de subprocesos del generador que lo creó.</span><span class="sxs-lookup"><span data-stu-id="79050-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="79050-115">Este objeto es inmutable.</span><span class="sxs-lookup"><span data-stu-id="79050-115">This object is immutable.</span></span>

<span data-ttu-id="79050-116">Al trazar una geometría transformada con el método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , el ancho del trazo no se ve afectado por la transformación que se aplica a la geometría.</span><span class="sxs-lookup"><span data-stu-id="79050-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="79050-117">El ancho del trazo solo se ve afectado por la transformación del mundo.</span><span class="sxs-lookup"><span data-stu-id="79050-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="79050-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="79050-118">Examples</span></span>

<span data-ttu-id="79050-119">En el ejemplo siguiente se crea una [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))y, a continuación, se dibuja sin transformarla.</span><span class="sxs-lookup"><span data-stu-id="79050-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="79050-120">Genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="79050-120">It produces the output shown in the following illustration.</span></span>

![Ilustración de un rectángulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="79050-122">En el ejemplo siguiente se usa el destino de representación para escalar la geometría en un factor de 3 y, a continuación, se dibuja.</span><span class="sxs-lookup"><span data-stu-id="79050-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="79050-123">En la ilustración siguiente se muestra el resultado de dibujar el rectángulo sin la transformación y con la transformación; observa que el trazo es más grueso después de la transformación, aunque el grosor del trazo sea 1.</span><span class="sxs-lookup"><span data-stu-id="79050-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con un trazo más grueso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="79050-125">En el ejemplo siguiente se usa el método **CreateTransformedGeometry** para escalar la geometría en un factor de 3 y, a continuación, se dibuja.</span><span class="sxs-lookup"><span data-stu-id="79050-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="79050-126">Genera la salida que se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="79050-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="79050-127">Observe que, aunque el rectángulo es mayor, su trazo no ha aumentado.</span><span class="sxs-lookup"><span data-stu-id="79050-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con el mismo trazo](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="79050-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79050-129">Requirements</span></span>



| <span data-ttu-id="79050-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="79050-130">Requirement</span></span> | <span data-ttu-id="79050-131">Value</span><span class="sxs-lookup"><span data-stu-id="79050-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="79050-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79050-132">Header</span></span><br/>  | <dl> <span data-ttu-id="79050-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="79050-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="79050-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79050-134">Library</span></span><br/> | <dl> <span data-ttu-id="79050-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79050-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="79050-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79050-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="79050-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79050-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79050-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="79050-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79050-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="79050-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
