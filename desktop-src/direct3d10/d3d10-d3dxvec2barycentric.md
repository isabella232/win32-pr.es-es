---
description: 'Función D3DXVec2BaryCentric (D3DX10Math.h): devuelve un punto en coordenadas baricéntricas, mediante los vectores 2D especificados.'
ms.assetid: 8eceb2c0-26a0-4a7f-9830-85327dcb31ab
title: Función D3DXVec2BaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b78d08c67fed04af9ef0d54d0c6895106b99208
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108446"
---
# <a name="d3dxvec2barycentric-function-d3dx10mathh"></a><span data-ttu-id="45bc2-103">Función D3DXVec2BaryCentric (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="45bc2-103">D3DXVec2BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="45bc2-104">Devuelve un punto en coordenadas baricéntricas, utilizando los vectores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="45bc2-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="45bc2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45bc2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _In_       D3DXVECTOR2 *pOut,
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2,
  _In_ const D3DXVECTOR2 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="45bc2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45bc2-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="45bc2-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="45bc2-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="45bc2-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="45bc2-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="45bc2-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="45bc2-112">Puntero a una estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="45bc2-112">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="45bc2-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="45bc2-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="45bc2-115">Puntero a una estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="45bc2-115">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="45bc2-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="45bc2-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="45bc2-118">Puntero a una estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="45bc2-118">Pointer to a source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="45bc2-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45bc2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45bc2-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="45bc2-121">Weighting factor.</span></span> <span data-ttu-id="45bc2-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="45bc2-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="45bc2-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45bc2-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45bc2-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45bc2-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45bc2-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="45bc2-125">Weighting factor.</span></span> <span data-ttu-id="45bc2-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="45bc2-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45bc2-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45bc2-127">Return value</span></span>

<span data-ttu-id="45bc2-128">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="45bc2-128">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="45bc2-129">Puntero a una estructura D3DXVECTOR2 en coordenadas centradas en Bary.</span><span class="sxs-lookup"><span data-stu-id="45bc2-129">Pointer to a D3DXVECTOR2 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="45bc2-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="45bc2-130">Remarks</span></span>

<span data-ttu-id="45bc2-131">La función D3DXVec2BaryCentric proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="45bc2-131">The D3DXVec2BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="45bc2-132">Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="45bc2-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="45bc2-133">Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada Barycentric (f,g). El parámetro f controla la cantidad de V2 que se pondera en el resultado y el parámetro g controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="45bc2-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result, and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="45bc2-134">Por último, 1-f-g controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="45bc2-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="45bc2-135">Tenga en cuenta las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="45bc2-135">Note the following relations.</span></span>

-   <span data-ttu-id="45bc2-136">Si (f>=0 &, & g>=0 &, & 1-f-g>=0), el punto está dentro del triángulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="45bc2-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="45bc2-137">Si (f==0 &, & g>=0 &, & 1-f-g>=0), el punto está en la línea V1V3.</span><span class="sxs-lookup"><span data-stu-id="45bc2-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="45bc2-138">Si (f>=0 &, & g==0 &, & 1-f-g>=0), el punto está en la línea V1V2.</span><span class="sxs-lookup"><span data-stu-id="45bc2-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="45bc2-139">Si (f>=0 &, & g>=0 &, & 1-f-g==0), el punto está en la línea V2V3.</span><span class="sxs-lookup"><span data-stu-id="45bc2-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="45bc2-140">Las coordenadas centradas en barras son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="45bc2-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="45bc2-141">En este contexto, el uso de coordenadas centradas en Bary representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="45bc2-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="45bc2-142">Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barícéntricas.</span><span class="sxs-lookup"><span data-stu-id="45bc2-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="45bc2-143">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="45bc2-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="45bc2-144">De esta manera, la función D3DXVec2BaryCentric se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="45bc2-144">In this way, the D3DXVec2BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="45bc2-145">Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="45bc2-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="45bc2-146">Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="45bc2-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="45bc2-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45bc2-147">Requirements</span></span>



| <span data-ttu-id="45bc2-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="45bc2-148">Requirement</span></span> | <span data-ttu-id="45bc2-149">Value</span><span class="sxs-lookup"><span data-stu-id="45bc2-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45bc2-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45bc2-150">Header</span></span><br/>  | <dl> <span data-ttu-id="45bc2-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="45bc2-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="45bc2-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45bc2-152">Library</span></span><br/> | <dl> <span data-ttu-id="45bc2-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="45bc2-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45bc2-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45bc2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45bc2-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="45bc2-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
