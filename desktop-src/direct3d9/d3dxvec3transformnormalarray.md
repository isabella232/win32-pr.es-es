---
description: 'Función D3DXVec3TransformNormalArray (D3dx9math.h): transforma una matriz (x, y, z, 0) por una matriz determinada.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Función D3DXVec3TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097733"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="cd327-103">Función D3DXVec3TransformNormalArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="cd327-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="cd327-104">Transforma una matriz (x, y, z, 0) mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="cd327-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd327-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd327-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="cd327-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd327-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd327-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd327-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd327-109">Puntero a la [**matriz D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cd327-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd327-110">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd327-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd327-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd327-112">Pasos entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="cd327-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="cd327-113">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd327-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd327-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd327-115">Puntero a la matriz [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="cd327-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="cd327-116">*VStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd327-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd327-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd327-118">Pasos entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd327-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="cd327-119">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd327-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="cd327-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cd327-121">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="cd327-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd327-122">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cd327-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd327-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd327-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd327-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cd327-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd327-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd327-125">Return value</span></span>

<span data-ttu-id="cd327-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd327-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="cd327-127">Puntero a una [**matriz D3DXVECTOR3**](d3dxvector3.md) que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="cd327-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd327-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd327-128">Remarks</span></span>

<span data-ttu-id="cd327-129">Esta función transforma el vector (*pV*->x, *pV*->y, *pV*->z, 0) por la matriz a la que apunta *pM*.</span><span class="sxs-lookup"><span data-stu-id="cd327-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="cd327-130">Si desea transformar un normal, la matriz que pasa a esta función debe ser la transpuesta de la inversa de la matriz que usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="cd327-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="cd327-131">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="cd327-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cd327-132">De esta manera, la **función D3DXVec3TransformNormalArray** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="cd327-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd327-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd327-133">Requirements</span></span>



| <span data-ttu-id="cd327-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd327-134">Requirement</span></span> | <span data-ttu-id="cd327-135">Value</span><span class="sxs-lookup"><span data-stu-id="cd327-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd327-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd327-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cd327-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="cd327-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cd327-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd327-138">Library</span></span><br/> | <dl> <span data-ttu-id="cd327-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd327-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd327-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd327-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd327-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="cd327-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
