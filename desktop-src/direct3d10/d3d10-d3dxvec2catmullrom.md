---
description: Realiza una interpolación Catmull-Rom, utilizando los vectores 2D especificados.
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: Función D3DXVec2CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71f499313a31c200b5cc657664b10b43dde47ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698336"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a><span data-ttu-id="1835b-103">Función D3DXVec2CatmullRom (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1835b-103">D3DXVec2CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="1835b-104">Realiza una interpolación Catmull-Rom, utilizando los vectores 2D especificados.</span><span class="sxs-lookup"><span data-stu-id="1835b-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1835b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1835b-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="1835b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1835b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1835b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1835b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="1835b-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-109">Puntero al [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1835b-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1835b-110">*pV0* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1835b-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1835b-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-112">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="1835b-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1835b-113">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1835b-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1835b-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-115">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="1835b-115">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1835b-116">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1835b-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1835b-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-118">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="1835b-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1835b-119">*pV3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1835b-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1835b-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-121">Puntero a una estructura D3DXVECTOR2 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="1835b-121">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="1835b-122">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1835b-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1835b-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1835b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1835b-124">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="1835b-124">Weighting factor.</span></span> <span data-ttu-id="1835b-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1835b-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1835b-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1835b-126">Return value</span></span>

<span data-ttu-id="1835b-127">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="1835b-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="1835b-128">Puntero a una estructura D3DXVECTOR2 que es el resultado de la interpolación Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="1835b-128">Pointer to a D3DXVECTOR2 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1835b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1835b-129">Remarks</span></span>

<span data-ttu-id="1835b-130">Dados cuatro puntos (P1, P2, P3, P4), buscar una función Q (s) de modo que:</span><span class="sxs-lookup"><span data-stu-id="1835b-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="1835b-131">La spline Catmull-Rom se puede derivar de la spline Hermite estableciendo:</span><span class="sxs-lookup"><span data-stu-id="1835b-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="1835b-132">donde:</span><span class="sxs-lookup"><span data-stu-id="1835b-132">where:</span></span>

<span data-ttu-id="1835b-133">V1 es el contenido de pV0.</span><span class="sxs-lookup"><span data-stu-id="1835b-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="1835b-134">V2 es el contenido de pV1.</span><span class="sxs-lookup"><span data-stu-id="1835b-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="1835b-135">P3 es el contenido de pV2.</span><span class="sxs-lookup"><span data-stu-id="1835b-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="1835b-136">P4 es el contenido de pV3.</span><span class="sxs-lookup"><span data-stu-id="1835b-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="1835b-137">Usar la ecuación de spline Hermite:</span><span class="sxs-lookup"><span data-stu-id="1835b-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="1835b-138">y sustituir v1, V2, T1, T2 produce:</span><span class="sxs-lookup"><span data-stu-id="1835b-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="1835b-139">Esto se puede reorganizar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1835b-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="1835b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1835b-140">Requirements</span></span>



| <span data-ttu-id="1835b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1835b-141">Requirement</span></span> | <span data-ttu-id="1835b-142">Value</span><span class="sxs-lookup"><span data-stu-id="1835b-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1835b-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1835b-143">Header</span></span><br/>  | <dl> <span data-ttu-id="1835b-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1835b-144"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1835b-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1835b-145">Library</span></span><br/> | <dl> <span data-ttu-id="1835b-146"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1835b-146"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1835b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1835b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1835b-148">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="1835b-148">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
