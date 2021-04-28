---
description: 'Función D3DXVec3CatmullRom (D3DX10Math.h): realiza una interpolación Catmull-Rom mediante los vectores 3D especificados.'
ms.assetid: 324bd4b5-b0df-4dd3-b370-3c365c9f2db1
title: Función D3DXVec3CatmullRom (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a09d61e9c43624f441975eca1a131a82f8092587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108223"
---
# <a name="d3dxvec3catmullrom-function-d3dx10mathh"></a><span data-ttu-id="19d42-103">Función D3DXVec3CatmullRom (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="19d42-103">D3DXVec3CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="19d42-104">Realiza una Catmull-Rom interpolación mediante los vectores 3D especificados.</span><span class="sxs-lookup"><span data-stu-id="19d42-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19d42-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="19d42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19d42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d42-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="19d42-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="19d42-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-109">Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="19d42-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="19d42-110">*pV0* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="19d42-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19d42-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-112">Puntero a una estructura D3DXVECTOR3 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="19d42-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="19d42-113">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="19d42-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19d42-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-115">Puntero a una estructura D3DXVECTOR3 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="19d42-115">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="19d42-116">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="19d42-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19d42-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-118">Puntero a una estructura D3DXVECTOR3 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="19d42-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="19d42-119">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="19d42-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="19d42-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-121">Puntero a una estructura D3DXVECTOR3 de origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="19d42-121">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="19d42-122">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="19d42-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d42-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19d42-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19d42-124">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="19d42-124">Weighting factor.</span></span> <span data-ttu-id="19d42-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="19d42-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d42-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19d42-126">Return value</span></span>

<span data-ttu-id="19d42-127">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="19d42-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="19d42-128">Puntero a una estructura D3DXVECTOR3 que es el resultado de la Catmull-Rom interpolación.</span><span class="sxs-lookup"><span data-stu-id="19d42-128">Pointer to a D3DXVECTOR3 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d42-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19d42-129">Remarks</span></span>

<span data-ttu-id="19d42-130">Dados cuatro puntos (p1, p2, p3, p4), busque una función Q(s) de modo que:</span><span class="sxs-lookup"><span data-stu-id="19d42-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="19d42-131">La Catmull-Rom spline se puede derivar de la spline Hermite estableciendo:</span><span class="sxs-lookup"><span data-stu-id="19d42-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="19d42-132">donde:</span><span class="sxs-lookup"><span data-stu-id="19d42-132">where:</span></span>

<span data-ttu-id="19d42-133">v1 es el contenido de pV0.</span><span class="sxs-lookup"><span data-stu-id="19d42-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="19d42-134">v2 es el contenido de pV1.</span><span class="sxs-lookup"><span data-stu-id="19d42-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="19d42-135">p3 es el contenido de pV2.</span><span class="sxs-lookup"><span data-stu-id="19d42-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="19d42-136">p4 es el contenido de pV3.</span><span class="sxs-lookup"><span data-stu-id="19d42-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="19d42-137">Uso de la ecuación spline hermite:</span><span class="sxs-lookup"><span data-stu-id="19d42-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="19d42-138">y sustituir por v1, v2, t1, t2 produce:</span><span class="sxs-lookup"><span data-stu-id="19d42-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="19d42-139">Esto se puede reorganizar como:</span><span class="sxs-lookup"><span data-stu-id="19d42-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="19d42-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19d42-140">Requirements</span></span>



| <span data-ttu-id="19d42-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="19d42-141">Requirement</span></span> | <span data-ttu-id="19d42-142">Value</span><span class="sxs-lookup"><span data-stu-id="19d42-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d42-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19d42-143">Header</span></span><br/> | <dl> <span data-ttu-id="19d42-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="19d42-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d42-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="19d42-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d42-146">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="19d42-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
