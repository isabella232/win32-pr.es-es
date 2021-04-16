---
description: Determina si un rayo forma una intersección con esta malla.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Método ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649411"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="b7ef4-103">ID3DX10Mesh:: Intersect (método)</span><span class="sxs-lookup"><span data-stu-id="b7ef4-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="b7ef4-104">Determina si un rayo forma una intersección con esta malla.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ef4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7ef4-105">Syntax</span></span>


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="b7ef4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7ef4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ef4-107">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b7ef4-109">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-110">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-111">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b7ef4-112">Puntero a una estructura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-113">*pHitCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b7ef4-115">Número de veces que el rayo intersecó con la malla.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-116">*pFaceIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b7ef4-118">Puntero a un valor de índice de la superficie más cercana al origen del rayo, si pHit es **true**.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-119">*PU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-120">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-120">Type: **float\***</span></span>

<span data-ttu-id="b7ef4-121">Puntero a una coordenada de posicionamiento de Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-122">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-123">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-123">Type: **float\***</span></span>

<span data-ttu-id="b7ef4-124">Puntero a una coordenada de posicionamiento de Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-125">*pDist* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-126">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-126">Type: **float\***</span></span>

<span data-ttu-id="b7ef4-127">Puntero a una distancia del parámetro de intersección de rayo.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef4-128">*ppAllHits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b7ef4-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7ef4-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b7ef4-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b7ef4-130">Puntero a una [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene una matriz de estructuras de [**\_ \_ información de intersección D3DX10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ef4-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="b7ef4-131">Esta es una lista de todos los aciertos que se produjeron en la prueba de intersección.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7ef4-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7ef4-132">Return value</span></span>

<span data-ttu-id="b7ef4-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7ef4-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7ef4-134">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b7ef4-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7ef4-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7ef4-135">Remarks</span></span>

<span data-ttu-id="b7ef4-136">Esta API proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="b7ef4-137">Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="b7ef4-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="b7ef4-138">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="b7ef4-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="b7ef4-139">El parámetro U controla la cantidad de v2 que se pondera en el resultado, y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="b7ef4-140">Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="b7ef4-141">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="b7ef4-142">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="b7ef4-143">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="b7ef4-144">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="b7ef4-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="b7ef4-145">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="b7ef4-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ef4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7ef4-146">Requirements</span></span>



| <span data-ttu-id="b7ef4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ef4-147">Requirement</span></span> | <span data-ttu-id="b7ef4-148">Value</span><span class="sxs-lookup"><span data-stu-id="b7ef4-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ef4-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7ef4-149">Header</span></span><br/>  | <dl> <span data-ttu-id="b7ef4-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ef4-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7ef4-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7ef4-151">Library</span></span><br/> | <dl> <span data-ttu-id="b7ef4-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7ef4-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ef4-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7ef4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ef4-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="b7ef4-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="b7ef4-155">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b7ef4-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
