---
description: Transforma una matriz (x, y, z, w) por una matriz determinada.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: Función D3DXVec4TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649431"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="26b85-103">Función D3DXVec4TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="26b85-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="26b85-104">Transforma una matriz (x, y, z, w) por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="26b85-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b85-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b85-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="26b85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b85-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26b85-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="26b85-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="26b85-109">Puntero a la matriz [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="26b85-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="26b85-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b85-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b85-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b85-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="26b85-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="26b85-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b85-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="26b85-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="26b85-115">Puntero a la matriz de D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="26b85-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="26b85-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b85-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b85-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b85-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="26b85-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="26b85-119">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b85-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="26b85-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26b85-121">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="26b85-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="26b85-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b85-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b85-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b85-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b85-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="26b85-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b85-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b85-125">Return value</span></span>

<span data-ttu-id="26b85-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="26b85-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="26b85-127">Puntero a una estructura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="26b85-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b85-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26b85-128">Remarks</span></span>

<span data-ttu-id="26b85-129">Esta función transforma la matriz pV (x, y, z, w) por la matriz pM.</span><span class="sxs-lookup"><span data-stu-id="26b85-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="26b85-130">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="26b85-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="26b85-131">De esta manera, la función **D3DXVec4TransformArray** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="26b85-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b85-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b85-132">Requirements</span></span>



| <span data-ttu-id="26b85-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b85-133">Requirement</span></span> | <span data-ttu-id="26b85-134">Value</span><span class="sxs-lookup"><span data-stu-id="26b85-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b85-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26b85-135">Header</span></span><br/> | <dl> <span data-ttu-id="26b85-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b85-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b85-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="26b85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b85-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="26b85-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
