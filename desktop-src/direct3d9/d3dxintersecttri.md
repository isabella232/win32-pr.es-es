---
description: 'Función D3DXIntersectTri (D3DX9Mesh.h): calcula la intersección de un rayo y un triángulo.'
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Función D3DXIntersectTri (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098273"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="c60bd-103">Función D3DXIntersectTri (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="c60bd-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="c60bd-104">Calcula la intersección de un rayo y un triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c60bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c60bd-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c60bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c60bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60bd-107">*p0* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60bd-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60bd-109">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la primera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-110">*p1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60bd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60bd-112">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la segunda posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-113">*p2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60bd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60bd-115">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que describe la tercera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-116">*pRayPos* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60bd-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60bd-118">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando el punto donde comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-119">*pRayDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c60bd-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c60bd-121">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) especificando la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-122">*pU* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c60bd-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c60bd-124">Coordenadas de impacto centradas en barra, U.</span><span class="sxs-lookup"><span data-stu-id="c60bd-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-125">*pV* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c60bd-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c60bd-127">Coordenadas de impacto centradas en barra, V.</span><span class="sxs-lookup"><span data-stu-id="c60bd-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="c60bd-128">*pDist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c60bd-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c60bd-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c60bd-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c60bd-130">Distancia del parámetro de intersección de rayos.</span><span class="sxs-lookup"><span data-stu-id="c60bd-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60bd-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c60bd-131">Return value</span></span>

<span data-ttu-id="c60bd-132">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c60bd-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c60bd-133">Devuelve **TRUE** si el rayo forma una intersección con el área del triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="c60bd-134">De lo contrario, **devuelve FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c60bd-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c60bd-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c60bd-135">Remarks</span></span>

<span data-ttu-id="c60bd-136">La [**función D3DXIntersect**](d3dxintersect.md) proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="c60bd-137">Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + U(V2 - V1) + V(V3 - V1).</span><span class="sxs-lookup"><span data-stu-id="c60bd-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="c60bd-138">Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada centrada en barras (U,V).</span><span class="sxs-lookup"><span data-stu-id="c60bd-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="c60bd-139">El parámetro U controla la cantidad de V2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="c60bd-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="c60bd-140">Por último, el valor de 1 - (U + V) controla la cantidad de V1 que se \[ pondera en el \] resultado.</span><span class="sxs-lookup"><span data-stu-id="c60bd-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="c60bd-141">Las coordenadas barycéntricas son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="c60bd-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="c60bd-142">En este contexto, el uso de coordenadas baricéntricas representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="c60bd-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="c60bd-143">Lo que se aplica a las coordenadas cartesianas es true para las coordenadas barídricas.</span><span class="sxs-lookup"><span data-stu-id="c60bd-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="c60bd-144">Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="c60bd-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="c60bd-145">Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="c60bd-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="c60bd-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c60bd-146">Requirements</span></span>



| <span data-ttu-id="c60bd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c60bd-147">Requirement</span></span> | <span data-ttu-id="c60bd-148">Value</span><span class="sxs-lookup"><span data-stu-id="c60bd-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c60bd-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c60bd-149">Header</span></span><br/>  | <dl> <span data-ttu-id="c60bd-150"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="c60bd-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c60bd-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c60bd-151">Library</span></span><br/> | <dl> <span data-ttu-id="c60bd-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c60bd-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c60bd-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c60bd-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60bd-154">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="c60bd-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
