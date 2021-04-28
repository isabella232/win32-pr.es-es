---
description: 'Función D3DXVec3TransformCoord (D3DX10Math.h): transforma un vector 3D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.'
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Función D3DXVec3TransformCoord (D3DX10Math.h)
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
ms.openlocfilehash: 5b3e763d87503f9ca71911ad40ccf3c6ae9ca722
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108103"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="b31d0-103">Función D3DXVec3TransformCoord (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b31d0-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="b31d0-104">Transforma un vector 3D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="b31d0-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="b31d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b31d0-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b31d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b31d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31d0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b31d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b31d0-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b31d0-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b31d0-109">Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b31d0-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b31d0-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b31d0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b31d0-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b31d0-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b31d0-112">Puntero a la estructura D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="b31d0-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b31d0-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b31d0-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b31d0-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b31d0-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b31d0-115">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="b31d0-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b31d0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b31d0-116">Return value</span></span>

<span data-ttu-id="b31d0-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b31d0-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b31d0-118">Puntero a una estructura D3DXVECTOR3 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="b31d0-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31d0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b31d0-119">Remarks</span></span>

<span data-ttu-id="b31d0-120">Esta función transforma el vector, pV (x, y, z, 1), por la matriz, pM, proyectando el resultado de nuevo en w=1.</span><span class="sxs-lookup"><span data-stu-id="b31d0-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="b31d0-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b31d0-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b31d0-122">De esta manera, la función D3DXVec3TransformCoord se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="b31d0-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b31d0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b31d0-123">Requirements</span></span>



| <span data-ttu-id="b31d0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b31d0-124">Requirement</span></span> | <span data-ttu-id="b31d0-125">Value</span><span class="sxs-lookup"><span data-stu-id="b31d0-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b31d0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b31d0-126">Header</span></span><br/> | <dl> <span data-ttu-id="b31d0-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b31d0-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b31d0-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b31d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b31d0-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b31d0-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
