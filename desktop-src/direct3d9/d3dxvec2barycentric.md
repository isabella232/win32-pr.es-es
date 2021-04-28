---
description: 'Función D3DXVec2BaryCentric (D3dx9math.h): devuelve un punto en coordenadas centradas en Barycentric, mediante los vectores 2D especificados.'
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: Función D3DXVec2BaryCentric (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3210624087a3d1d5a612ba1eb628e7d85ba4fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117793"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a><span data-ttu-id="e3b2e-103">Función D3DXVec2BaryCentric (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e3b2e-103">D3DXVec2BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="e3b2e-104">Devuelve un punto en coordenadas centradas en Barycentric, utilizando los vectores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3b2e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _Out_       D3DXVECTOR2 *pOut,
  _In_  const D3DXVECTOR2 *pV1,
  _In_  const D3DXVECTOR2 *pV2,
  _In_  const D3DXVECTOR2 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="e3b2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3b2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b2e-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3b2e-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e3b2e-109">Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3b2e-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b2e-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e3b2e-112">Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3b2e-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b2e-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e3b2e-115">Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3b2e-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-117">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b2e-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e3b2e-118">Puntero a una estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3b2e-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b2e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b2e-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-121">Weighting factor.</span></span> <span data-ttu-id="e3b2e-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e3b2e-123">*g* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e3b2e-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b2e-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b2e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b2e-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-125">Weighting factor.</span></span> <span data-ttu-id="e3b2e-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b2e-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3b2e-127">Return value</span></span>

<span data-ttu-id="e3b2e-128">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3b2e-128">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e3b2e-129">Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) en coordenadas centradas en baría.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-129">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b2e-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3b2e-130">Remarks</span></span>

<span data-ttu-id="e3b2e-131">La **función D3DXVec2BaryCentric** proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-131">The **D3DXVec2BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="e3b2e-132">Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="e3b2e-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="e3b2e-133">Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada Barycentric (f,g). El parámetro *f* controla la cantidad de V2 que se pondera en el resultado y el parámetro *g* controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result, and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="e3b2e-134">Por último, 1-f-g controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="e3b2e-135">Tenga en cuenta las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-135">Note the following relations.</span></span>

-   <span data-ttu-id="e3b2e-136">Si (f>=0 &, & g>=0 &, & 1-f-g>=0), el punto está dentro del triángulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="e3b2e-137">Si (f==0 &, & g>=0 &, & 1-f-g>=0), el punto está en la línea V1V3.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="e3b2e-138">Si (f>=0 &, & g==0 &, & 1-f-g>=0), el punto está en la línea V1V2.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="e3b2e-139">Si (f>=0 &, & g>=0 &, & 1-f-g==0), el punto está en la línea V2V3.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="e3b2e-140">Las coordenadas barycéntricas son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="e3b2e-141">En este contexto, el uso de coordenadas baricéntricas representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="e3b2e-142">Lo que se aplica a las coordenadas cartesianas es true para las coordenadas baríntricas.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="e3b2e-143">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="e3b2e-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e3b2e-144">De este modo, la **función D3DXVec2BaryCentric** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-144">In this way, the **D3DXVec2BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e3b2e-145">Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="e3b2e-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="e3b2e-146">Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="e3b2e-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span> <span data-ttu-id="e3b2e-147">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="e3b2e-147">(This resource may not be available in some languages and countries.)</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b2e-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b2e-148">Requirements</span></span>



| <span data-ttu-id="e3b2e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b2e-149">Requirement</span></span> | <span data-ttu-id="e3b2e-150">Value</span><span class="sxs-lookup"><span data-stu-id="e3b2e-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b2e-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b2e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b2e-152"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b2e-152"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b2e-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3b2e-153">Library</span></span><br/> | <dl> <span data-ttu-id="e3b2e-154"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b2e-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b2e-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3b2e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b2e-156">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e3b2e-156">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
