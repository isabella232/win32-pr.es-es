---
description: Transforma un vector 2D en una matriz determinada y proyecta el resultado de nuevo en w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Función D3DXVec2TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0d7e93c2b3a78160f2f1f1ad3342575b4369a057
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708007"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="2055d-103">Función D3DXVec2TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2055d-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="2055d-104">Transforma un vector 2D en una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="2055d-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="2055d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2055d-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2055d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2055d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2055d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2055d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2055d-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2055d-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2055d-109">Puntero al [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2055d-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2055d-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2055d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2055d-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2055d-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2055d-112">Puntero a la estructura de D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="2055d-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="2055d-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2055d-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2055d-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2055d-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2055d-115">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2055d-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2055d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2055d-116">Return value</span></span>

<span data-ttu-id="2055d-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="2055d-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="2055d-118">Puntero a una estructura D3DXVECTOR2 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="2055d-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2055d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2055d-119">Remarks</span></span>

<span data-ttu-id="2055d-120">Esta función transforma el vector, pV (x, y, 0, 1), por la matriz, pM, y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="2055d-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="2055d-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="2055d-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2055d-122">De esta manera, la función D3DXVec2TransformCoord se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="2055d-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2055d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2055d-123">Requirements</span></span>



| <span data-ttu-id="2055d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2055d-124">Requirement</span></span> | <span data-ttu-id="2055d-125">Value</span><span class="sxs-lookup"><span data-stu-id="2055d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2055d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2055d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2055d-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2055d-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2055d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2055d-128">Library</span></span><br/> | <dl> <span data-ttu-id="2055d-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2055d-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2055d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2055d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2055d-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2055d-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
