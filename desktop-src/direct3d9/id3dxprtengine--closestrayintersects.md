---
description: Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine:: ClosestRayIntersects (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280479"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="8ca32-103">ID3DXPRTEngine:: ClosestRayIntersects (método)</span><span class="sxs-lookup"><span data-stu-id="8ca32-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="8ca32-104">Usa el seguimiento de rayos eficaz en las simulaciones de transferencia de Radiance (PRT) precalculadas para determinar si un rayo forma una intersección con una malla.</span><span class="sxs-lookup"><span data-stu-id="8ca32-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="8ca32-105">Si se encuentra una intersección, el método devuelve el índice de la superficie de malla más cercana que el rayo y las coordenadas Barycentric del punto de intersección.</span><span class="sxs-lookup"><span data-stu-id="8ca32-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca32-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ca32-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="8ca32-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ca32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca32-108">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-109">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ca32-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ca32-110">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="8ca32-111">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-112">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ca32-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ca32-113">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección normalizada del rayo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8ca32-114">*pFaceIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca32-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ca32-116">Puntero al índice de la cara de la malla actual que se alcanza primero por el rayo dado, en función de la pila de todas las caras de la malla del bloqueador delante de la malla actual.</span><span class="sxs-lookup"><span data-stu-id="8ca32-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8ca32-117">*PU* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca32-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ca32-119">Puntero a una coordenada de posicionamiento de Barycentric, U, para el vértice 0 del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="8ca32-120">*PV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca32-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ca32-122">Puntero a una coordenada de posicionamiento de Barycentric, V, para el vértice 1 del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="8ca32-123">*pDist* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ca32-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca32-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca32-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ca32-125">Puntero a la distancia del punto de intersección a lo largo del rayo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca32-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ca32-126">Return value</span></span>

<span data-ttu-id="8ca32-127">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ca32-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ca32-128">Devuelve **true** si el rayo forma una intersección con la malla actual; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="8ca32-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca32-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ca32-129">Remarks</span></span>

<span data-ttu-id="8ca32-130">Use [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) para establecer las distancias mínima y máxima de intersección con el rayo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="8ca32-131">La coordenada Barycentric del tercer vértice (vértice 2) del triángulo es 1-(U + V).</span><span class="sxs-lookup"><span data-stu-id="8ca32-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="8ca32-132">Este método se ejecuta más lentamente que [**ID3DXPRTEngine:: ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="8ca32-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="8ca32-133">Use **ID3DXPRTEngine:: ShadowRayIntersects** si no se necesita la ubicación del punto de intersección.</span><span class="sxs-lookup"><span data-stu-id="8ca32-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="8ca32-134">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8ca32-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8ca32-135">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8ca32-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca32-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca32-136">Requirements</span></span>



| <span data-ttu-id="8ca32-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca32-137">Requirement</span></span> | <span data-ttu-id="8ca32-138">Value</span><span class="sxs-lookup"><span data-stu-id="8ca32-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca32-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca32-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8ca32-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca32-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8ca32-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ca32-141">Library</span></span><br/> | <dl> <span data-ttu-id="8ca32-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ca32-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ca32-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ca32-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca32-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="8ca32-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="8ca32-145">**ID3DXPRTEngine::ShadowRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="8ca32-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="8ca32-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="8ca32-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
