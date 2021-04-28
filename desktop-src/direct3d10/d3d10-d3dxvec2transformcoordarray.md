---
description: 'Función D3DXVec2TransformCoordArray (D3DX10Math.h): transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.'
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: Función D3DXVec2TransformCoordArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f36b5fb5a5263f83c42ac66cc5f606fa1c4b75ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108333"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="37a2b-103">Función D3DXVec2TransformCoordArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="37a2b-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="37a2b-104">Transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado en w = 1.</span><span class="sxs-lookup"><span data-stu-id="37a2b-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37a2b-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="37a2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a2b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="37a2b-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="37a2b-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="37a2b-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37a2b-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37a2b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37a2b-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="37a2b-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="37a2b-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="37a2b-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="37a2b-115">Puntero a la matriz D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="37a2b-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="37a2b-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37a2b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37a2b-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="37a2b-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="37a2b-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="37a2b-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="37a2b-121">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="37a2b-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="37a2b-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="37a2b-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37a2b-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37a2b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37a2b-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="37a2b-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a2b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37a2b-125">Return value</span></span>

<span data-ttu-id="37a2b-126">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="37a2b-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="37a2b-127">Puntero a una [**matriz transformada D3DXVECTOR4.**](d3d10-d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="37a2b-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a2b-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37a2b-128">Remarks</span></span>

<span data-ttu-id="37a2b-129">Esta función transforma la matriz pV (x, y, 0, 1) mediante el pM de matriz, proyectando el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="37a2b-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="37a2b-130">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="37a2b-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="37a2b-131">De esta manera, la función D3DXVec2TransformCoordArray se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="37a2b-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a2b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37a2b-132">Requirements</span></span>



| <span data-ttu-id="37a2b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a2b-133">Requirement</span></span> | <span data-ttu-id="37a2b-134">Value</span><span class="sxs-lookup"><span data-stu-id="37a2b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37a2b-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37a2b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="37a2b-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="37a2b-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="37a2b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37a2b-137">Library</span></span><br/> | <dl> <span data-ttu-id="37a2b-138"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="37a2b-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37a2b-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37a2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a2b-140">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="37a2b-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
