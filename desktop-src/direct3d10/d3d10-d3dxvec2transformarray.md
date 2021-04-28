---
description: 'Función D3DXVec2TransformArray (D3DX10Math.h): transforma una matriz (x, y, 0, 1) por una matriz determinada.'
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: Función D3DXVec2TransformArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cec42fcbe53d3a8aa160f6864af70cbf441a19ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108373"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="8dd89-103">Función D3DXVec2TransformArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8dd89-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="8dd89-104">Transforma una matriz (x, y, 0, 1) mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="8dd89-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dd89-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="8dd89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dd89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dd89-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd89-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8dd89-109">Puntero a la [**estructura D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8dd89-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8dd89-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dd89-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dd89-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="8dd89-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8dd89-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dd89-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8dd89-115">Puntero al [**D3DXVECTOR2 de origen.**](d3d10-d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="8dd89-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dd89-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dd89-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dd89-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8dd89-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8dd89-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dd89-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8dd89-121">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="8dd89-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8dd89-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8dd89-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd89-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dd89-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dd89-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8dd89-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dd89-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dd89-125">Return value</span></span>

<span data-ttu-id="8dd89-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dd89-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8dd89-127">Puntero a una estructura D3DXVECTOR4 que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="8dd89-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd89-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8dd89-128">Remarks</span></span>

<span data-ttu-id="8dd89-129">Esta función transforma la matriz pV (x, y, 0, 1) por el pM de matriz.</span><span class="sxs-lookup"><span data-stu-id="8dd89-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="8dd89-130">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="8dd89-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8dd89-131">De esta manera, la [**función D3DXVec2Transform**](d3d10-d3dxvec2transform.md) se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="8dd89-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd89-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dd89-132">Requirements</span></span>



| <span data-ttu-id="8dd89-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dd89-133">Requirement</span></span> | <span data-ttu-id="8dd89-134">Value</span><span class="sxs-lookup"><span data-stu-id="8dd89-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd89-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dd89-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8dd89-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8dd89-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8dd89-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dd89-137">Library</span></span><br/> | <dl> <span data-ttu-id="8dd89-138"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dd89-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8dd89-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8dd89-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd89-140">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8dd89-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
