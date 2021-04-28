---
description: 'Función D3DXVec4TransformArray (D3dx9math.h): transforma una matriz (x, y, 0, 1) por una matriz determinada.'
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: Función D3DXVec4TransformArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f5435b7e88a5424db9457fac077495fcfd8828a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097633"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a><span data-ttu-id="ea870-103">Función D3DXVec4TransformArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ea870-103">D3DXVec4TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="ea870-104">Transforma una matriz (x, y, 0, 1) mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="ea870-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea870-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea870-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ea870-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea870-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea870-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ea870-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea870-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ea870-109">Puntero a la [**matriz D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ea870-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ea870-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea870-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea870-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea870-112">Pasos entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="ea870-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="ea870-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea870-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea870-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ea870-115">Puntero a la matriz [**D3DXVECTOR4 de**](d3dxvector4.md) origen.</span><span class="sxs-lookup"><span data-stu-id="ea870-115">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="ea870-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea870-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea870-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea870-118">Pasos entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea870-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="ea870-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea870-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea870-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ea870-121">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="ea870-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ea870-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ea870-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea870-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea870-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea870-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ea870-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea870-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea870-125">Return value</span></span>

<span data-ttu-id="ea870-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea870-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ea870-127">Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="ea870-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea870-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea870-128">Remarks</span></span>

<span data-ttu-id="ea870-129">Esta función transforma la matriz *pV* (x, y, 0, 1) mediante la matriz *pM*.</span><span class="sxs-lookup"><span data-stu-id="ea870-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="ea870-130">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="ea870-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ea870-131">De esta manera, la **función D3DXVec4TransformArray** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="ea870-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea870-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea870-132">Requirements</span></span>



| <span data-ttu-id="ea870-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea870-133">Requirement</span></span> | <span data-ttu-id="ea870-134">Value</span><span class="sxs-lookup"><span data-stu-id="ea870-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea870-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea870-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ea870-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea870-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ea870-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea870-137">Library</span></span><br/> | <dl> <span data-ttu-id="ea870-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea870-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea870-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea870-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea870-140">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="ea870-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
