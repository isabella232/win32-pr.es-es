---
description: Calcula la intersección de un rayo y un triángulo.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Función D3DXIntersectTri (D3DX10math. h)
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
ms.openlocfilehash: af96d25b4f13995d60e7926ec5da2d15ff86f282
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698276"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="8d27f-103">Función D3DXIntersectTri (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="8d27f-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="8d27f-104">Calcula la intersección de un rayo y un triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d27f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d27f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8d27f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d27f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d27f-107">*P0* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d27f-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8d27f-109">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la primera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-110">*P1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d27f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8d27f-112">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la segunda posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-113">*P2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d27f-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8d27f-115">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que describe la tercera posición del vértice del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-116">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d27f-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8d27f-118">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-119">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d27f-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8d27f-121">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-122">*PU* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-123">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d27f-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d27f-124">Barycentric coordenadas de aciertos, U.</span><span class="sxs-lookup"><span data-stu-id="8d27f-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-125">*PV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-126">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d27f-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d27f-127">Barycentric coordenadas de aciertos, V.</span><span class="sxs-lookup"><span data-stu-id="8d27f-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="8d27f-128">*pDist* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8d27f-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d27f-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d27f-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8d27f-130">Distancia del parámetro de intersección de rayo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d27f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d27f-131">Return value</span></span>

<span data-ttu-id="8d27f-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d27f-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d27f-133">Devuelve **true** si el rayo forma una intersección con el área del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="8d27f-134">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="8d27f-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d27f-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d27f-135">Remarks</span></span>

<span data-ttu-id="8d27f-136">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="8d27f-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="8d27f-137">El parámetro U controla la cantidad de v2 que se pondera en el resultado, y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="8d27f-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="8d27f-138">Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="8d27f-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="8d27f-139">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="8d27f-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="8d27f-140">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="8d27f-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="8d27f-141">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="8d27f-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="8d27f-142">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8d27f-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8d27f-143">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8d27f-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d27f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d27f-144">Requirements</span></span>



| <span data-ttu-id="8d27f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d27f-145">Requirement</span></span> | <span data-ttu-id="8d27f-146">Value</span><span class="sxs-lookup"><span data-stu-id="8d27f-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d27f-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d27f-147">Header</span></span><br/>  | <dl> <span data-ttu-id="8d27f-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d27f-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="8d27f-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d27f-149">Library</span></span><br/> | <dl> <span data-ttu-id="8d27f-150"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d27f-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d27f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d27f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d27f-152">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="8d27f-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
