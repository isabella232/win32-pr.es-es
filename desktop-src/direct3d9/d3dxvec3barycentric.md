---
description: 'Función D3DXVec3BaryCentric (D3dx9math.h): devuelve un punto en coordenadas baricéntricas, mediante los vectores 3D especificados.'
ms.assetid: ecbabc76-9936-4f31-adec-1ec807984787
title: Función D3DXVec3BaryCentric (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c966eeabe78deabefb2877405f649f3d162f9d73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097903"
---
# <a name="d3dxvec3barycentric-function-d3dx9mathh"></a><span data-ttu-id="9c2b7-103">Función D3DXVec3BaryCentric (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="9c2b7-103">D3DXVec3BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="9c2b7-104">Devuelve un punto en coordenadas baricéntricas, utilizando los vectores 3D especificados.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c2b7-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _Out_       D3DXVECTOR3 *pOut,
  _In_  const D3DXVECTOR3 *pV1,
  _In_  const D3DXVECTOR3 *pV2,
  _In_  const D3DXVECTOR3 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="9c2b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c2b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c2b7-107">*pOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c2b7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c2b7-109">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c2b7-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c2b7-112">Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c2b7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c2b7-115">Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c2b7-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c2b7-118">Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c2b7-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-121">Weighting factor.</span></span> <span data-ttu-id="9c2b7-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2b7-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c2b7-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-125">Weighting factor.</span></span> <span data-ttu-id="9c2b7-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c2b7-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c2b7-127">Return value</span></span>

<span data-ttu-id="9c2b7-128">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c2b7-128">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9c2b7-129">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) en coordenadas centradas en Bary.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-129">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c2b7-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c2b7-130">Remarks</span></span>

<span data-ttu-id="9c2b7-131">La **función D3DXVec3BaryCentric** proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-131">The **D3DXVec3BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="9c2b7-132">Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + f(V2-V1) + g(V3-V1).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="9c2b7-133">Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada Barycentric (f,g). El parámetro *f* controla la cantidad de V2 que se pondera en el resultado y el parámetro *g* controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="9c2b7-134">Por último, 1-f-g controla la cantidad de V1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="9c2b7-135">Tenga en cuenta las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-135">Note the following relations.</span></span>

-   <span data-ttu-id="9c2b7-136">Si (f>=0 &, & g>=0 &, & 1-f-g>=0), el punto está dentro del triángulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="9c2b7-137">Si (f==0 &, & g>=0 &, & 1-f-g>=0), el punto está en la línea V1V3.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="9c2b7-138">Si (f>=0 &, & g==0 &, & 1-f-g>=0), el punto está en la línea V1V2.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="9c2b7-139">Si (f>=0 &, & g>=0 &, & 1-f-g==0), el punto está en la línea V2V3.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="9c2b7-140">Las coordenadas centradas en barras son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="9c2b7-141">En este contexto, el uso de coordenadas centradas en Bary representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="9c2b7-142">Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barícéntricas.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="9c2b7-143">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="9c2b7-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9c2b7-144">De esta manera, la **función D3DXVec3BaryCentric** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-144">In this way, the **D3DXVec3BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9c2b7-145">Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="9c2b7-146">Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2b7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c2b7-147">Requirements</span></span>



| <span data-ttu-id="9c2b7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c2b7-148">Requirement</span></span> | <span data-ttu-id="9c2b7-149">Value</span><span class="sxs-lookup"><span data-stu-id="9c2b7-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2b7-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c2b7-150">Header</span></span><br/>  | <dl> <span data-ttu-id="9c2b7-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9c2b7-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9c2b7-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c2b7-152">Library</span></span><br/> | <dl> <span data-ttu-id="9c2b7-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c2b7-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c2b7-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9c2b7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2b7-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="9c2b7-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
