---
description: Transforma un vector 3D por una matriz determinada y proyecta el resultado de nuevo en w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Función D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a8fc7c7a00133e036921eabaa145dca01a12f042
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362593"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="e2f8f-103">Función D3DXVec3TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e2f8f-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="e2f8f-104">Transforma un vector 3D por una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2f8f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e2f8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2f8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f8f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2f8f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f8f-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2f8f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e2f8f-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e2f8f-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2f8f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f8f-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2f8f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e2f8f-112">Puntero a la estructura de D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2f8f-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2f8f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f8f-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2f8f-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e2f8f-115">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f8f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f8f-116">Return value</span></span>

<span data-ttu-id="e2f8f-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2f8f-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e2f8f-118">Puntero a una estructura D3DXVECTOR3 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f8f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2f8f-119">Remarks</span></span>

<span data-ttu-id="e2f8f-120">Esta función transforma el vector, pV (x, y, z, 1), por la matriz, pM, y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="e2f8f-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e2f8f-122">De esta manera, la función D3DXVec3TransformCoord se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f8f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f8f-123">Requirements</span></span>



| <span data-ttu-id="e2f8f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f8f-124">Requirement</span></span> | <span data-ttu-id="e2f8f-125">Value</span><span class="sxs-lookup"><span data-stu-id="e2f8f-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f8f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2f8f-126">Header</span></span><br/> | <dl> <span data-ttu-id="e2f8f-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f8f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f8f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2f8f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f8f-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e2f8f-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
