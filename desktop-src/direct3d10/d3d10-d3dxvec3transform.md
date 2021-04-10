---
description: Transforma el vector (x, y, z, 1) por una matriz determinada.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Función D3DXVec3Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 6db2e2ad4279863ba68f709f02f86796552e0463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003905"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="91638-103">Función D3DXVec3Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="91638-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="91638-104">Transforma el vector (x, y, z, 1) por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="91638-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="91638-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91638-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="91638-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91638-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="91638-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91638-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="91638-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="91638-109">Puntero a la estructura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="91638-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="91638-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91638-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91638-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="91638-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="91638-112">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md)de origen.</span><span class="sxs-lookup"><span data-stu-id="91638-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="91638-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91638-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91638-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="91638-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91638-115">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="91638-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91638-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91638-116">Return value</span></span>

<span data-ttu-id="91638-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="91638-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="91638-118">Puntero a una estructura D3DXVECTOR4 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="91638-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="91638-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91638-119">Remarks</span></span>

<span data-ttu-id="91638-120">Esta función transforma el vector, pV (x, y, z, 1), por la matriz pM.</span><span class="sxs-lookup"><span data-stu-id="91638-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="91638-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="91638-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="91638-122">De esta manera, la función D3DXVec3Transform se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="91638-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="91638-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91638-123">Requirements</span></span>



| <span data-ttu-id="91638-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="91638-124">Requirement</span></span> | <span data-ttu-id="91638-125">Value</span><span class="sxs-lookup"><span data-stu-id="91638-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91638-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91638-126">Header</span></span><br/> | <dl> <span data-ttu-id="91638-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="91638-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91638-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="91638-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91638-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="91638-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
