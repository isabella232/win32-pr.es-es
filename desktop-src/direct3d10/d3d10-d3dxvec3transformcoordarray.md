---
description: Transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Función D3DXVec3TransformCoordArray (D3DX10Math. h)
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
ms.openlocfilehash: b0b7ca3c2898e07dc8b5e9ced0117e642bfdfb41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003848"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="abfe7-103">Función D3DXVec3TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="abfe7-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="abfe7-104">Transforma una matriz (x, y, z, 1) por una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="abfe7-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfe7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abfe7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="abfe7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abfe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfe7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="abfe7-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="abfe7-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="abfe7-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="abfe7-110">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abfe7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abfe7-112">Intervalo entre vectores en el flujo de datos de salida.</span><span class="sxs-lookup"><span data-stu-id="abfe7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="abfe7-113">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="abfe7-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="abfe7-115">Puntero a la matriz de D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="abfe7-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="abfe7-116">*VStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abfe7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abfe7-118">Intervalo entre vectores en el flujo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="abfe7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="abfe7-119">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="abfe7-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="abfe7-121">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="abfe7-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="abfe7-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abfe7-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfe7-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abfe7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abfe7-124">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="abfe7-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfe7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abfe7-125">Return value</span></span>

<span data-ttu-id="abfe7-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="abfe7-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="abfe7-127">Puntero a una estructura D3DXVECTOR3 que es la matriz transformada.</span><span class="sxs-lookup"><span data-stu-id="abfe7-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="abfe7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abfe7-128">Remarks</span></span>

<span data-ttu-id="abfe7-129">Esta función transforma la matriz pV (x, y, z, 1) de la matriz pM y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="abfe7-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="abfe7-130">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="abfe7-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="abfe7-131">De esta manera, la función [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="abfe7-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="abfe7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abfe7-132">Requirements</span></span>



| <span data-ttu-id="abfe7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="abfe7-133">Requirement</span></span> | <span data-ttu-id="abfe7-134">Value</span><span class="sxs-lookup"><span data-stu-id="abfe7-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abfe7-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abfe7-135">Header</span></span><br/> | <dl> <span data-ttu-id="abfe7-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="abfe7-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfe7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="abfe7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfe7-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="abfe7-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
