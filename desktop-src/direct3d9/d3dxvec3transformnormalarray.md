---
description: Transforma una matriz (x, y, z, 0) por una matriz determinada.
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Función D3DXVec3TransformNormalArray (D3dx9math. h)
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
ms.openlocfilehash: 7a70893cc38d2f2fa04b3b89432aa0f887c5a352
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649446"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="e0d4c-103">Función D3DXVec3TransformNormalArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e0d4c-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="e0d4c-104">Transforma una matriz (x, y, z, 0) por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d4c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0d4c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e0d4c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0d4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d4c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0d4c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e0d4c-109">Puntero a la matriz [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e0d4c-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0d4c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0d4c-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e0d4c-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e0d4c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e0d4c-115">Puntero a la matriz de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="e0d4c-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0d4c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0d4c-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="e0d4c-119">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e0d4c-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e0d4c-121">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e0d4c-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0d4c-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d4c-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0d4c-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0d4c-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d4c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d4c-125">Return value</span></span>

<span data-ttu-id="e0d4c-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0d4c-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e0d4c-127">Puntero a una matriz [**D3DXVECTOR3**](d3dxvector3.md) que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d4c-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0d4c-128">Remarks</span></span>

<span data-ttu-id="e0d4c-129">Esta función transforma el vector (*PV*->x, *PV*->y, *PV*->z, 0) por la matriz a la que señala *PM*.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="e0d4c-130">Si desea transformar un normal, la matriz que se pasa a esta función debe ser la transformación del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="e0d4c-131">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="e0d4c-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e0d4c-132">De esta manera, la función **D3DXVec3TransformNormalArray** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e0d4c-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d4c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d4c-133">Requirements</span></span>



| <span data-ttu-id="e0d4c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d4c-134">Requirement</span></span> | <span data-ttu-id="e0d4c-135">Value</span><span class="sxs-lookup"><span data-stu-id="e0d4c-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d4c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0d4c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e0d4c-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d4c-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e0d4c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0d4c-138">Library</span></span><br/> | <dl> <span data-ttu-id="e0d4c-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0d4c-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0d4c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0d4c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d4c-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e0d4c-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
