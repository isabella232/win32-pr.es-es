---
description: Devuelve un punto en coordenadas de Barycentric, usando los vectores 4D especificados.
ms.assetid: 80d73232-76bf-4f40-add2-dd1bdcc5cd98
title: Función D3DXVec4BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75f0d068d1545f1b8b55dc3b976d3585e6f9bc88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649415"
---
# <a name="d3dxvec4barycentric-function-d3dx9mathh"></a><span data-ttu-id="fcf9c-103">Función D3DXVec4BaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fcf9c-103">D3DXVec4BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="fcf9c-104">Devuelve un punto en coordenadas de Barycentric, usando los vectores 4D especificados.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-104">Returns a point in Barycentric coordinates, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcf9c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcf9c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4BaryCentric(
  _Out_       D3DXVECTOR4 *pOut,
  _In_  const D3DXVECTOR4 *pV1,
  _In_  const D3DXVECTOR4 *pV2,
  _In_  const D3DXVECTOR4 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="fcf9c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcf9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf9c-107">*pOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcf9c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcf9c-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fcf9c-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcf9c-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcf9c-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fcf9c-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcf9c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcf9c-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fcf9c-116">*pV3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcf9c-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcf9c-118">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fcf9c-119">*f* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcf9c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcf9c-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-121">Weighting factor.</span></span> <span data-ttu-id="fcf9c-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fcf9c-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcf9c-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf9c-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcf9c-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcf9c-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-125">Weighting factor.</span></span> <span data-ttu-id="fcf9c-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf9c-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcf9c-127">Return value</span></span>

<span data-ttu-id="fcf9c-128">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcf9c-128">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fcf9c-129">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) en coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-129">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf9c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcf9c-130">Remarks</span></span>

<span data-ttu-id="fcf9c-131">La función **D3DXVec4BaryCentric** proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-131">The **D3DXVec4BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="fcf9c-132">Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + f (V2-V1) + g (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="fcf9c-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="fcf9c-133">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (f, g). El parámetro *f* controla la cantidad de v2 que se pondera en el resultado y el parámetro *g* controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="fcf9c-134">Por último, 1-f-g controla la cantidad de la versión 1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="fcf9c-135">Tenga en cuenta las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-135">Note the following relations.</span></span>

-   <span data-ttu-id="fcf9c-136">Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), el punto está dentro del triángulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="fcf9c-137">Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V3.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="fcf9c-138">Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V2.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="fcf9c-139">Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), el punto se encuentra en la línea V2V3.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="fcf9c-140">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="fcf9c-141">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="fcf9c-142">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="fcf9c-143">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="fcf9c-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fcf9c-144">De esta manera, la función **D3DXVec4BaryCentric** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-144">In this way, the **D3DXVec4BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fcf9c-145">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="fcf9c-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="fcf9c-146">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="fcf9c-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf9c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcf9c-147">Requirements</span></span>



| <span data-ttu-id="fcf9c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf9c-148">Requirement</span></span> | <span data-ttu-id="fcf9c-149">Value</span><span class="sxs-lookup"><span data-stu-id="fcf9c-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf9c-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcf9c-150">Header</span></span><br/>  | <dl> <span data-ttu-id="fcf9c-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf9c-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fcf9c-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcf9c-152">Library</span></span><br/> | <dl> <span data-ttu-id="fcf9c-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcf9c-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcf9c-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcf9c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf9c-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fcf9c-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
