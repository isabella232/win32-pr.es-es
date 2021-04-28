---
description: 'Función D3DXVec3TransformNormal (D3DX10Math.h): transforma el vector 3D normal por la matriz dada.'
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Función D3DXVec3TransformNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 0fc1456b89f3e11f2076a8e7b6b960d15e9c7083
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103063"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="beed1-103">Función D3DXVec3TransformNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="beed1-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="beed1-104">Transforma el vector 3D normal por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="beed1-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="beed1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beed1-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="beed1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beed1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="beed1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="beed1-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="beed1-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="beed1-109">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="beed1-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="beed1-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="beed1-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beed1-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="beed1-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="beed1-112">Puntero a la estructura D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="beed1-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="beed1-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="beed1-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beed1-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="beed1-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="beed1-115">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="beed1-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beed1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beed1-116">Return value</span></span>

<span data-ttu-id="beed1-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="beed1-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="beed1-118">Puntero a una estructura D3DXVECTOR3 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="beed1-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="beed1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="beed1-119">Remarks</span></span>

<span data-ttu-id="beed1-120">Esta función transforma el vector (pV->x, pV->y, pV->z, 0) por la matriz a la que apunta pM.</span><span class="sxs-lookup"><span data-stu-id="beed1-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="beed1-121">Si desea transformar un normal, la matriz que pase a esta función debe ser la transponer del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="beed1-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="beed1-122">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="beed1-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="beed1-123">De este modo, la **función D3DXVec3TransformNormal** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="beed1-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="beed1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beed1-124">Requirements</span></span>



| <span data-ttu-id="beed1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="beed1-125">Requirement</span></span> | <span data-ttu-id="beed1-126">Value</span><span class="sxs-lookup"><span data-stu-id="beed1-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beed1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beed1-127">Header</span></span><br/> | <dl> <span data-ttu-id="beed1-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="beed1-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beed1-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="beed1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beed1-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="beed1-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
