---
description: 'Función D3DXVec4CatmullRom (D3dx9math.h): realiza una interpolación Catmull-Rom, mediante los vectores 4D especificados.'
ms.assetid: 24c26e70-b02c-4621-8b7e-db16f99dddb5
title: Función D3DXVec4CatmullRom (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 06ba24374ee2ad4e6fd008d90c55d2990dc166f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115533"
---
# <a name="d3dxvec4catmullrom-function-d3dx9mathh"></a><span data-ttu-id="65b55-103">Función D3DXVec4CatmullRom (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="65b55-103">D3DXVec4CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="65b55-104">Realiza una Catmull-Rom interpolación mediante los vectores 4D especificados.</span><span class="sxs-lookup"><span data-stu-id="65b55-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65b55-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="65b55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65b55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b55-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="65b55-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="65b55-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-109">Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="65b55-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="65b55-110">*pV0* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65b55-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="65b55-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-112">Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="65b55-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="65b55-113">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65b55-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="65b55-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-115">Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="65b55-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="65b55-116">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65b55-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="65b55-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-118">Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="65b55-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="65b55-119">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="65b55-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-120">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="65b55-120">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-121">Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.</span><span class="sxs-lookup"><span data-stu-id="65b55-121">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="65b55-122">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="65b55-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b55-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65b55-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65b55-124">Factor de ponderación.</span><span class="sxs-lookup"><span data-stu-id="65b55-124">Weighting factor.</span></span> <span data-ttu-id="65b55-125">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="65b55-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b55-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65b55-126">Return value</span></span>

<span data-ttu-id="65b55-127">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="65b55-127">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="65b55-128">Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado del Catmull-Rom interpolación.</span><span class="sxs-lookup"><span data-stu-id="65b55-128">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="65b55-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65b55-129">Remarks</span></span>

<span data-ttu-id="65b55-130">Dados cuatro puntos (p1, p2, p3, p4), busque una función Q(s) de modo que:</span><span class="sxs-lookup"><span data-stu-id="65b55-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="65b55-131">El Catmull-Rom spline se puede derivar de la spline Hermite estableciendo:</span><span class="sxs-lookup"><span data-stu-id="65b55-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="65b55-132">donde:</span><span class="sxs-lookup"><span data-stu-id="65b55-132">where:</span></span>

<span data-ttu-id="65b55-133">v1 es el contenido de pV0.</span><span class="sxs-lookup"><span data-stu-id="65b55-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="65b55-134">v2 en el contenido de pV1.</span><span class="sxs-lookup"><span data-stu-id="65b55-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="65b55-135">p3 es el contenido de pV2.</span><span class="sxs-lookup"><span data-stu-id="65b55-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="65b55-136">p4 es el contenido de pV3.</span><span class="sxs-lookup"><span data-stu-id="65b55-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="65b55-137">Uso de la ecuación spline hermite:</span><span class="sxs-lookup"><span data-stu-id="65b55-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="65b55-138">y sustituir por v1, v2, t1, t2 produce:</span><span class="sxs-lookup"><span data-stu-id="65b55-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="65b55-139">Esto se puede reorganizar como:</span><span class="sxs-lookup"><span data-stu-id="65b55-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="65b55-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b55-140">Requirements</span></span>



| <span data-ttu-id="65b55-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b55-141">Requirement</span></span> | <span data-ttu-id="65b55-142">Value</span><span class="sxs-lookup"><span data-stu-id="65b55-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b55-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65b55-143">Header</span></span><br/>  | <dl> <span data-ttu-id="65b55-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="65b55-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="65b55-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65b55-145">Library</span></span><br/> | <dl> <span data-ttu-id="65b55-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="65b55-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65b55-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="65b55-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b55-148">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="65b55-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="65b55-149">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="65b55-149">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
</dt> <dt>

[<span data-ttu-id="65b55-150">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="65b55-150">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
</dt> </dl>

 

 
