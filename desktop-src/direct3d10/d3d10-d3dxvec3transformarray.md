---
description: 'Función D3DXVec3TransformArray (D3DX10Math.h): transforma una matriz (x, y, z, 1) por una matriz determinada.'
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: Función D3DXVec3TransformArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: bc38f0ef634763d9a5be85795a897b483431aede
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108123"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="81099-103">Función D3DXVec3TransformArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="81099-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="81099-104">Transforma una matriz (x, y, z, 1) mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="81099-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="81099-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81099-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="81099-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81099-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81099-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="81099-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="81099-109">Puntero a la [**matriz D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="81099-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="81099-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="81099-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81099-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81099-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="81099-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="81099-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="81099-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="81099-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="81099-115">Puntero a la matriz [**D3DXVECTOR3 de**](d3d10-d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="81099-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="81099-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="81099-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81099-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81099-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="81099-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="81099-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="81099-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="81099-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="81099-121">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="81099-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="81099-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="81099-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81099-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81099-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81099-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="81099-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81099-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81099-125">Return value</span></span>

<span data-ttu-id="81099-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="81099-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="81099-127">Puntero a una [**matriz transformada D3DXVECTOR4.**](d3d10-d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="81099-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="81099-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81099-128">Remarks</span></span>

<span data-ttu-id="81099-129">Esta función transforma la matriz pV (x, y, z, 1) por el pM de matriz.</span><span class="sxs-lookup"><span data-stu-id="81099-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="81099-130">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="81099-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="81099-131">De este modo, la función D3DXVec3TransformArray se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="81099-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81099-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81099-132">Requirements</span></span>



| <span data-ttu-id="81099-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="81099-133">Requirement</span></span> | <span data-ttu-id="81099-134">Value</span><span class="sxs-lookup"><span data-stu-id="81099-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81099-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81099-135">Header</span></span><br/> | <dl> <span data-ttu-id="81099-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="81099-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81099-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81099-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81099-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="81099-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
