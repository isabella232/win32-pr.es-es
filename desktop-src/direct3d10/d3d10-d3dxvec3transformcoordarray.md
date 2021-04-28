---
description: 'Función D3DXVec3TransformCoordArray (D3DX10Math.h): transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.'
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Función D3DXVec3TransformCoordArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c4a1edfd89b127d0782d3bab23c2390775422c69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103113"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="14ea0-103">Función D3DXVec3TransformCoordArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="14ea0-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="14ea0-104">Transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="14ea0-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ea0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14ea0-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="14ea0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ea0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="14ea0-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="14ea0-109">Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="14ea0-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="14ea0-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14ea0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14ea0-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="14ea0-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="14ea0-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="14ea0-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="14ea0-115">Puntero a la matriz D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="14ea0-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="14ea0-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14ea0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14ea0-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="14ea0-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="14ea0-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="14ea0-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="14ea0-121">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="14ea0-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="14ea0-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="14ea0-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ea0-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14ea0-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14ea0-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="14ea0-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ea0-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14ea0-125">Return value</span></span>

<span data-ttu-id="14ea0-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="14ea0-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="14ea0-127">Puntero a una estructura D3DXVECTOR3 que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="14ea0-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ea0-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14ea0-128">Remarks</span></span>

<span data-ttu-id="14ea0-129">Esta función transforma la matriz pV (x, y, z, 1) mediante el pM de matriz, proyectando el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="14ea0-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="14ea0-130">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="14ea0-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="14ea0-131">De este modo, la [**función D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="14ea0-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ea0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14ea0-132">Requirements</span></span>



| <span data-ttu-id="14ea0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ea0-133">Requirement</span></span> | <span data-ttu-id="14ea0-134">Value</span><span class="sxs-lookup"><span data-stu-id="14ea0-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14ea0-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14ea0-135">Header</span></span><br/> | <dl> <span data-ttu-id="14ea0-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="14ea0-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ea0-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14ea0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ea0-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="14ea0-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
