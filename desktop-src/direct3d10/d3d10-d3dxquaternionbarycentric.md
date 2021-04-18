---
description: Devuelve un cuaternión en coordenadas Barycentric.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Función D3DXQuaternionBaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f7cdfcf5b8e7052fcbea72f12123a0ea44422853
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678841"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="66f30-103">Función D3DXQuaternionBaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="66f30-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="66f30-104">Devuelve un cuaternión en coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="66f30-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66f30-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="66f30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66f30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f30-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="66f30-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f30-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66f30-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="66f30-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="66f30-110">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66f30-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f30-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66f30-112">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="66f30-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="66f30-113">*pQ2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66f30-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f30-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66f30-115">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="66f30-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="66f30-116">*pQ3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66f30-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="66f30-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66f30-118">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="66f30-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="66f30-119">*f* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="66f30-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f30-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f30-121">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="66f30-121">Weighting factor.</span></span> <span data-ttu-id="66f30-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="66f30-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="66f30-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66f30-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f30-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f30-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f30-125">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="66f30-125">Weighting factor.</span></span> <span data-ttu-id="66f30-126">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="66f30-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f30-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66f30-127">Return value</span></span>

<span data-ttu-id="66f30-128">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="66f30-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="66f30-129">Puntero a una estructura D3DXQUATERNION en coordenadas Barycentric.</span><span class="sxs-lookup"><span data-stu-id="66f30-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f30-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66f30-130">Remarks</span></span>

<span data-ttu-id="66f30-131">Para calcular las coordenadas Barycentric, la función D3DXQuaternionBaryCentric implementa la siguiente serie de operaciones de interpolación lineal esférica:</span><span class="sxs-lookup"><span data-stu-id="66f30-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="66f30-132">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="66f30-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="66f30-133">De esta manera, la función D3DXQuaternionBaryCentric se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="66f30-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="66f30-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="66f30-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="66f30-135">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="66f30-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="66f30-136">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="66f30-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="66f30-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f30-137">Requirements</span></span>



| <span data-ttu-id="66f30-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f30-138">Requirement</span></span> | <span data-ttu-id="66f30-139">Value</span><span class="sxs-lookup"><span data-stu-id="66f30-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f30-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66f30-140">Header</span></span><br/>  | <dl> <span data-ttu-id="66f30-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f30-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="66f30-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f30-142">Library</span></span><br/> | <dl> <span data-ttu-id="66f30-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f30-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="66f30-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="66f30-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f30-145">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="66f30-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
