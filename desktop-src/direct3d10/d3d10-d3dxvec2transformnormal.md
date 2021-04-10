---
description: Transforma el vector 2D normal de la matriz especificada.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Función D3DXVec2TransformNormal (D3DX10Math. h)
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
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003832"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="99bc6-103">Función D3DXVec2TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="99bc6-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="99bc6-104">Transforma el vector 2D normal de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="99bc6-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99bc6-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="99bc6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99bc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bc6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99bc6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc6-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bc6-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="99bc6-109">Puntero al [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="99bc6-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="99bc6-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99bc6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc6-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bc6-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="99bc6-112">Puntero a la estructura de D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="99bc6-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="99bc6-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99bc6-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bc6-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bc6-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99bc6-115">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="99bc6-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bc6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99bc6-116">Return value</span></span>

<span data-ttu-id="99bc6-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bc6-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="99bc6-118">Puntero a una estructura D3DXVECTOR2 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="99bc6-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bc6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99bc6-119">Remarks</span></span>

<span data-ttu-id="99bc6-120">Esta función transforma el vector (pV->x, pV->y, 0,0) por la matriz a la que apunta pM.</span><span class="sxs-lookup"><span data-stu-id="99bc6-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="99bc6-121">Si desea transformar un normal, la matriz que se pasa a esta función debe ser la transformación del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="99bc6-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="99bc6-122">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="99bc6-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="99bc6-123">De esta manera, la función **D3DXVec2TransformNormal** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="99bc6-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bc6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99bc6-124">Requirements</span></span>



| <span data-ttu-id="99bc6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="99bc6-125">Requirement</span></span> | <span data-ttu-id="99bc6-126">Value</span><span class="sxs-lookup"><span data-stu-id="99bc6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99bc6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99bc6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="99bc6-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99bc6-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="99bc6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99bc6-129">Library</span></span><br/> | <dl> <span data-ttu-id="99bc6-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99bc6-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99bc6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="99bc6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bc6-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="99bc6-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
