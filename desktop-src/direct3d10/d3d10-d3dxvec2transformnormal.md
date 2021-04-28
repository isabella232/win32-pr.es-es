---
description: 'Función D3DXVec2TransformNormal (D3DX10Math.h): transforma el vector 2D normal por la matriz dada.'
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Función D3DXVec2TransformNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108303"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="95a2e-103">Función D3DXVec2TransformNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="95a2e-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="95a2e-104">Transforma el vector 2D normal por la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="95a2e-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95a2e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="95a2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95a2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a2e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="95a2e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2e-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="95a2e-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="95a2e-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="95a2e-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="95a2e-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95a2e-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2e-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="95a2e-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="95a2e-112">Puntero a la estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="95a2e-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="95a2e-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95a2e-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a2e-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="95a2e-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="95a2e-115">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="95a2e-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a2e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95a2e-116">Return value</span></span>

<span data-ttu-id="95a2e-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="95a2e-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="95a2e-118">Puntero a una estructura D3DXVECTOR2 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="95a2e-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="95a2e-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95a2e-119">Remarks</span></span>

<span data-ttu-id="95a2e-120">Esta función transforma el vector (pV->x, pV->y, 0, 0) por la matriz a la que apunta pM.</span><span class="sxs-lookup"><span data-stu-id="95a2e-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="95a2e-121">Si desea transformar un normal, la matriz que pase a esta función debe ser la transponer del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="95a2e-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="95a2e-122">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="95a2e-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="95a2e-123">De este modo, la **función D3DXVec2TransformNormal** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="95a2e-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a2e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a2e-124">Requirements</span></span>



| <span data-ttu-id="95a2e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a2e-125">Requirement</span></span> | <span data-ttu-id="95a2e-126">Value</span><span class="sxs-lookup"><span data-stu-id="95a2e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95a2e-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95a2e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="95a2e-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="95a2e-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="95a2e-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95a2e-129">Library</span></span><br/> | <dl> <span data-ttu-id="95a2e-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="95a2e-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95a2e-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95a2e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a2e-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="95a2e-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
