---
description: Devuelve un punto en coordenadas de Barycentric, usando los vectores 2D especificados.
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: Función D3DXVec2BaryCentric (D3dx9math. h)
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
ms.openlocfilehash: 8feb2f999ccc3628419c986ec0263d0e7e167d67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157168"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a><span data-ttu-id="f2a4d-103">Función D3DXVec2BaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f2a4d-103">D3DXVec2BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="f2a4d-104">Devuelve un punto en coordenadas de Barycentric, usando los vectores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2a4d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f2a4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a4d-107">*pOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2a4d-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2a4d-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f2a4d-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2a4d-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2a4d-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2a4d-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2a4d-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2a4d-115">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2a4d-116">*pV3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-117">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2a4d-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2a4d-118">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f2a4d-119">*f* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2a4d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2a4d-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-121">Weighting factor.</span></span> <span data-ttu-id="f2a4d-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f2a4d-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2a4d-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a4d-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2a4d-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2a4d-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-125">Weighting factor.</span></span> <span data-ttu-id="f2a4d-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a4d-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2a4d-127">Return value</span></span>

<span data-ttu-id="f2a4d-128">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2a4d-128">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f2a4d-129">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) en coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-129">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a4d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2a4d-130">Remarks</span></span>

<span data-ttu-id="f2a4d-131">La función **D3DXVec2BaryCentric** proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-131">The **D3DXVec2BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="f2a4d-132">Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + f (V2-V1) + g (V3-V1).</span><span class="sxs-lookup"><span data-stu-id="f2a4d-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="f2a4d-133">Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (f, g). El parámetro *f* controla la cantidad de v2 que se pondera en el resultado y el parámetro *g* controla la cantidad de V3 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result, and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="f2a4d-134">Por último, 1-f-g controla la cantidad de la versión 1 que se pondera en el resultado.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="f2a4d-135">Tenga en cuenta las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-135">Note the following relations.</span></span>

-   <span data-ttu-id="f2a4d-136">Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), el punto está dentro del triángulo V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="f2a4d-137">Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V3.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="f2a4d-138">Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V2.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="f2a4d-139">Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), el punto se encuentra en la línea V2V3.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="f2a4d-140">Las coordenadas de Barycentric son una forma de coordenadas generales.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="f2a4d-141">En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="f2a4d-142">Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="f2a4d-143">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="f2a4d-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f2a4d-144">De esta manera, la función **D3DXVec2BaryCentric** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-144">In this way, the **D3DXVec2BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f2a4d-145">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="f2a4d-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f2a4d-146">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="f2a4d-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span> <span data-ttu-id="f2a4d-147">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="f2a4d-147">(This resource may not be available in some languages and countries.)</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a4d-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2a4d-148">Requirements</span></span>



| <span data-ttu-id="f2a4d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2a4d-149">Requirement</span></span> | <span data-ttu-id="f2a4d-150">Value</span><span class="sxs-lookup"><span data-stu-id="f2a4d-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a4d-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2a4d-151">Header</span></span><br/>  | <dl> <span data-ttu-id="f2a4d-152"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2a4d-152"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f2a4d-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2a4d-153">Library</span></span><br/> | <dl> <span data-ttu-id="f2a4d-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2a4d-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2a4d-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2a4d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a4d-156">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f2a4d-156">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
