---
description: 'Función D3DXIntersectTri (D3DX10math.h): calcula la intersección de un rayo y un triángulo.'
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Función D3DXIntersectTri (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113243"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="434e3-103">Función D3DXIntersectTri (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="434e3-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="434e3-104">Calcula la intersección de un rayo y un triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="434e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="434e3-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="434e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="434e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434e3-107">*p0* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="434e3-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e3-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="434e3-109">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la primera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-110">*p1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="434e3-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e3-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="434e3-112">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la segunda posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-113">*p2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="434e3-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e3-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="434e3-115">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) que describe la tercera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-116">*pRayPos* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="434e3-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e3-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="434e3-118">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando el punto donde comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="434e3-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-119">*pRayDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="434e3-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="434e3-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="434e3-121">Puntero a una [**estructura D3DXVECTOR3,**](d3d10-d3dxvector3.md) especificando la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="434e3-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-122">*pU* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="434e3-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="434e3-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="434e3-124">Coordenadas de impacto centradas en barras, U.</span><span class="sxs-lookup"><span data-stu-id="434e3-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-125">*pV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="434e3-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="434e3-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="434e3-127">Coordenadas de impacto centradas en barras, V.</span><span class="sxs-lookup"><span data-stu-id="434e3-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="434e3-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="434e3-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434e3-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="434e3-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="434e3-130">Distancia del parámetro de intersección de rayos.</span><span class="sxs-lookup"><span data-stu-id="434e3-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434e3-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="434e3-131">Return value</span></span>

<span data-ttu-id="434e3-132">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="434e3-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="434e3-133">Devuelve **TRUE** si el rayo forma una intersección con el área del triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="434e3-134">De lo contrario, **devuelve FALSE**.</span><span class="sxs-lookup"><span data-stu-id="434e3-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="434e3-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="434e3-135">Remarks</span></span>

<span data-ttu-id="434e3-136">Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada centrada en barras (U,V).</span><span class="sxs-lookup"><span data-stu-id="434e3-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="434e3-137">El parámetro U controla la cantidad de V2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="434e3-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="434e3-138">Por último, el valor de 1 - (U + V) controla la cantidad de V1 que se \[ pondera en el \] resultado.</span><span class="sxs-lookup"><span data-stu-id="434e3-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="434e3-139">Las coordenadas centradas en barras son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="434e3-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="434e3-140">En este contexto, el uso de coordenadas centradas en barras representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="434e3-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="434e3-141">Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barídricas.</span><span class="sxs-lookup"><span data-stu-id="434e3-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="434e3-142">Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="434e3-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="434e3-143">Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="434e3-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="434e3-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="434e3-144">Requirements</span></span>



| <span data-ttu-id="434e3-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="434e3-145">Requirement</span></span> | <span data-ttu-id="434e3-146">Value</span><span class="sxs-lookup"><span data-stu-id="434e3-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="434e3-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="434e3-147">Header</span></span><br/>  | <dl> <span data-ttu-id="434e3-148"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="434e3-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="434e3-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="434e3-149">Library</span></span><br/> | <dl> <span data-ttu-id="434e3-150"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="434e3-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="434e3-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="434e3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434e3-152">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="434e3-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
