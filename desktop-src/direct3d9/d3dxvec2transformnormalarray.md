---
description: 'Función D3DXVec2TransformNormalArray (D3dx9math.h): transforma una matriz (x, y, 0, 0) mediante una matriz determinada.'
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: Función D3DXVec2TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71706551e73ed9bd52b41aae127625cd09b6d7f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097902"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="41ac2-103">Función D3DXVec2TransformNormalArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="41ac2-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="41ac2-104">Transforma una matriz (x, y, 0, 0) mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="41ac2-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ac2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41ac2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="41ac2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41ac2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ac2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="41ac2-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="41ac2-109">Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="41ac2-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41ac2-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ac2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ac2-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="41ac2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="41ac2-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="41ac2-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="41ac2-115">Puntero a la matriz [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="41ac2-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="41ac2-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ac2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ac2-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="41ac2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="41ac2-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="41ac2-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41ac2-121">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="41ac2-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="41ac2-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="41ac2-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41ac2-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41ac2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41ac2-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="41ac2-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ac2-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41ac2-125">Return value</span></span>

<span data-ttu-id="41ac2-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="41ac2-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="41ac2-127">Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="41ac2-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ac2-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41ac2-128">Remarks</span></span>

<span data-ttu-id="41ac2-129">Esta función transforma el vector *(pV-*>x, *pV-*>y, 0, 0) por la matriz a la que apunta *pM.*</span><span class="sxs-lookup"><span data-stu-id="41ac2-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="41ac2-130">Si desea transformar un normal, la matriz que pase a esta función debe ser la transponer del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="41ac2-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="41ac2-131">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="41ac2-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="41ac2-132">De este modo, la **función D3DXVec2TransformNormalArray** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="41ac2-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ac2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ac2-133">Requirements</span></span>



| <span data-ttu-id="41ac2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ac2-134">Requirement</span></span> | <span data-ttu-id="41ac2-135">Value</span><span class="sxs-lookup"><span data-stu-id="41ac2-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41ac2-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41ac2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="41ac2-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="41ac2-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="41ac2-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41ac2-138">Library</span></span><br/> | <dl> <span data-ttu-id="41ac2-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="41ac2-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41ac2-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="41ac2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ac2-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="41ac2-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
