---
description: 'Función D3DXVec2TransformCoordArray (D3dx9math.h): transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.'
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: Función D3DXVec2TransformCoordArray (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 257cb77ba97396170f221cff1c512a73eb84179c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097943"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="aacad-103">Función D3DXVec2TransformCoordArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="aacad-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="aacad-104">Transforma una matriz (x, y, 0, 1) por una matriz determinada y proyecta el resultado en w = 1.</span><span class="sxs-lookup"><span data-stu-id="aacad-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aacad-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="aacad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aacad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aacad-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aacad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="aacad-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="aacad-109">Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="aacad-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aacad-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aacad-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aacad-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aacad-112">Paso entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="aacad-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aacad-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aacad-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="aacad-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="aacad-115">Puntero a la matriz [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="aacad-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="aacad-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aacad-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aacad-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aacad-118">Paso entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="aacad-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aacad-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="aacad-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="aacad-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aacad-121">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="aacad-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aacad-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="aacad-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacad-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aacad-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aacad-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="aacad-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aacad-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aacad-125">Return value</span></span>

<span data-ttu-id="aacad-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="aacad-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="aacad-127">Puntero a una [**matriz transformada D3DXVECTOR4.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="aacad-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="aacad-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aacad-128">Remarks</span></span>

<span data-ttu-id="aacad-129">Esta función transforma la matriz *pV* (x, y, 0, 1) mediante la matriz *pM*, proyectando el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="aacad-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="aacad-130">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="aacad-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="aacad-131">De esta manera, la **función D3DXVec2TransformCoordArray** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="aacad-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aacad-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aacad-132">Requirements</span></span>



| <span data-ttu-id="aacad-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aacad-133">Requirement</span></span> | <span data-ttu-id="aacad-134">Value</span><span class="sxs-lookup"><span data-stu-id="aacad-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aacad-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aacad-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aacad-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="aacad-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aacad-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aacad-137">Library</span></span><br/> | <dl> <span data-ttu-id="aacad-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="aacad-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aacad-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aacad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aacad-140">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="aacad-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
