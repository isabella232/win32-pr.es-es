---
title: Métodos ID2D1Geometry ComputeArea
description: Calcula el área de la geometría.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Métodos de ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681207"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="78e5f-104">ID2D1Geometry:: ComputeArea (métodos)</span><span class="sxs-lookup"><span data-stu-id="78e5f-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="78e5f-105">Calcula el área de la geometría.</span><span class="sxs-lookup"><span data-stu-id="78e5f-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="78e5f-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="78e5f-106">Overload list</span></span>



| <span data-ttu-id="78e5f-107">Método</span><span class="sxs-lookup"><span data-stu-id="78e5f-107">Method</span></span>                                                                                                                      | <span data-ttu-id="78e5f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="78e5f-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e5f-109">[**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="78e5f-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="78e5f-110">Calcula el área de la geometría una vez transformada por la matriz especificada y plana con la tolerancia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="78e5f-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="78e5f-111">[**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="78e5f-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="78e5f-112">Calcula el área de la geometría una vez transformada por la matriz especificada y plana con la tolerancia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="78e5f-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="78e5f-113">[**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="78e5f-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="78e5f-114">Calcula el área de la geometría una vez transformada por la matriz especificada y plana con la tolerancia especificada.</span><span class="sxs-lookup"><span data-stu-id="78e5f-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="78e5f-115">[**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , Float, Float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="78e5f-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="78e5f-116">Calcula el área de la geometría una vez transformada por la matriz especificada y plana con la tolerancia especificada.</span><span class="sxs-lookup"><span data-stu-id="78e5f-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="78e5f-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="78e5f-117">Examples</span></span>

<span data-ttu-id="78e5f-118">En el ejemplo de código siguiente se usa **ComputeArea** para calcular el área de un círculo especificado (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="78e5f-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="78e5f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78e5f-119">Requirements</span></span>



| <span data-ttu-id="78e5f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78e5f-120">Requirement</span></span> | <span data-ttu-id="78e5f-121">Value</span><span class="sxs-lookup"><span data-stu-id="78e5f-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78e5f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78e5f-122">Library</span></span><br/> | <dl> <span data-ttu-id="78e5f-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78e5f-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="78e5f-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78e5f-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="78e5f-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e5f-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78e5f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="78e5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e5f-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="78e5f-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

