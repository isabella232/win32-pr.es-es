---
description: Determina si un rayo forma una intersección con una malla.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Función D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707879"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="8dd8a-103">D3DXIntersect función)</span><span class="sxs-lookup"><span data-stu-id="8dd8a-103">D3DXIntersect function</span></span>

<span data-ttu-id="8dd8a-104">Determina si un rayo forma una intersección con una malla.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dd8a-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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



## <a name="parameters"></a><span data-ttu-id="8dd8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dd8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dd8a-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="8dd8a-109">Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa la malla que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-110">*pRayPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8dd8a-112">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica el punto en el que comienza el rayo.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-113">*pRayDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8dd8a-115">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que especifica la dirección del rayo.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-116">*pHit* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-118">Puntero a un BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-118">Pointer to a BOOL.</span></span> <span data-ttu-id="8dd8a-119">Si el rayo cruza una esfera triangular en la malla, este valor se establecerá en **true**.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="8dd8a-120">De lo contrario, este valor se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-121">*pFaceIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-123">Puntero a un valor de índice de la superficie más cercana al origen del rayo, si pHit es **true**.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-124">*PU* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-126">Puntero a una coordenada de posicionamiento de Barycentric, U.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-127">*PV* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-128">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-129">Puntero a una coordenada de posicionamiento de Barycentric, V.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-130">*pDist* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-131">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-132">Puntero a una distancia del parámetro de intersección de rayo.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-133">*ppAllHits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-134">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8dd8a-135">Puntero a un objeto [**ID3DXBuffer**](id3dxbuffer.md) que contiene una matriz de estructuras [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd8a-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="8dd8a-136">*pCountOfHits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8dd8a-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd8a-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd8a-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8dd8a-138">Puntero a un valor DWORD que contiene el número de entradas de la matriz ppAllHits.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dd8a-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dd8a-139">Return value</span></span>

<span data-ttu-id="8dd8a-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8dd8a-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8dd8a-141">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8dd8a-142">Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd8a-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8dd8a-143">Remarks</span></span>

<span data-ttu-id="8dd8a-144">La función **D3DXIntersect** proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="8dd8a-145">Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + U (V2-V1) + V (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="8dd8a-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="8dd8a-146">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (U, V).</span><span class="sxs-lookup"><span data-stu-id="8dd8a-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="8dd8a-147">El parámetro U controla la cantidad de v2 que se pondera en el resultado, y el parámetro V controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="8dd8a-148">Por último, el valor de \[ 1-(U + V) \] controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="8dd8a-149">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="8dd8a-150">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="8dd8a-151">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="8dd8a-152">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="8dd8a-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8dd8a-153">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="8dd8a-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd8a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dd8a-154">Requirements</span></span>



| <span data-ttu-id="8dd8a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dd8a-155">Requirement</span></span> | <span data-ttu-id="8dd8a-156">Value</span><span class="sxs-lookup"><span data-stu-id="8dd8a-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd8a-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dd8a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="8dd8a-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dd8a-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8dd8a-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dd8a-159">Library</span></span><br/> | <dl> <span data-ttu-id="8dd8a-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dd8a-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8dd8a-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dd8a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd8a-162">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="8dd8a-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
