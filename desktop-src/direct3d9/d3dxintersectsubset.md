---
description: Forma una intersección con el rayo especificado con el subconjunto de malla dado. Esto proporciona una funcionalidad similar a D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Función D3DXIntersectSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280315"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="9f876-104">D3DXIntersectSubset función)</span><span class="sxs-lookup"><span data-stu-id="9f876-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="9f876-105">Forma una intersección con el rayo especificado con el subconjunto de malla dado.</span><span class="sxs-lookup"><span data-stu-id="9f876-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="9f876-106">Esto proporciona una funcionalidad similar a [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="9f876-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f876-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f876-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="9f876-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f876-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f876-109">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f876-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-110">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9f876-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="9f876-111">Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="9f876-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="9f876-112">La malla debe estar ordenada por atributo.</span><span class="sxs-lookup"><span data-stu-id="9f876-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-113">*AttribId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f876-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f876-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f876-115">Identificador de atributo del subconjunto con el que se va a formar una intersección.</span><span class="sxs-lookup"><span data-stu-id="9f876-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-116">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f876-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f876-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9f876-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="9f876-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-119">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f876-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-120">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f876-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9f876-121">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="9f876-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-122">*pHit* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-123">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-124">Puntero a un BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="9f876-124">Pointer to a BOOL.</span></span> <span data-ttu-id="9f876-125">Si el rayo cruza una esfera triangular en la malla, este valor se establecerá en **true**.</span><span class="sxs-lookup"><span data-stu-id="9f876-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="9f876-126">De lo contrario, este valor se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="9f876-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-127">*pFaceIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-129">Puntero a un valor de índice de la superficie más cercana al origen del rayo, si pHit es **true**.</span><span class="sxs-lookup"><span data-stu-id="9f876-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-130">*PU* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-132">Puntero a una coordenada de posicionamiento de Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="9f876-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-133">*PV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-134">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-135">Puntero a una coordenada de posicionamiento de Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="9f876-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-136">*pDist* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-137">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-138">Puntero a una distancia del parámetro de intersección de rayo.</span><span class="sxs-lookup"><span data-stu-id="9f876-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-139">*ppAllHits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9f876-141">Matriz de estructuras [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) que representan todos los resultados, no solo los resultados más cercanos.</span><span class="sxs-lookup"><span data-stu-id="9f876-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="9f876-142">*pCountOfHits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9f876-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f876-143">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f876-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f876-144">Número de elementos de la matriz devueltos por ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="9f876-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f876-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f876-145">Return value</span></span>

<span data-ttu-id="9f876-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f876-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f876-147">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f876-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f876-148">Si se produce un error en la función, el valor devuelto puede ser el siguiente: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9f876-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f876-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f876-149">Remarks</span></span>

<span data-ttu-id="9f876-150">La función **D3DXIntersectSubset** proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="9f876-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="9f876-151">Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="9f876-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="9f876-152">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="9f876-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="9f876-153">El parámetro U controla la cantidad de v2 que se pondera en el resultado y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="9f876-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="9f876-154">Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="9f876-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="9f876-155">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="9f876-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="9f876-156">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="9f876-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="9f876-157">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="9f876-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="9f876-158">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="9f876-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="9f876-159">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="9f876-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f876-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f876-160">Requirements</span></span>



| <span data-ttu-id="9f876-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f876-161">Requirement</span></span> | <span data-ttu-id="9f876-162">Value</span><span class="sxs-lookup"><span data-stu-id="9f876-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f876-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f876-163">Header</span></span><br/>  | <dl> <span data-ttu-id="9f876-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f876-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f876-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f876-165">Library</span></span><br/> | <dl> <span data-ttu-id="9f876-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f876-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f876-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f876-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f876-168">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="9f876-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
