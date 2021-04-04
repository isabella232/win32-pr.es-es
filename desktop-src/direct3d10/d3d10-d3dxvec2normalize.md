---
description: Devuelve la versión normalizada de un vector 2D.
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Función D3DXVec2Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e2894a86c0aa0c2ef6b45a41664b2d0cca1427c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914785"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="d7beb-103">Función D3DXVec2Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d7beb-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="d7beb-104">Devuelve la versión normalizada de un vector 2D.</span><span class="sxs-lookup"><span data-stu-id="d7beb-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7beb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7beb-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="d7beb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7beb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d7beb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7beb-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7beb-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d7beb-109">Puntero al [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d7beb-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d7beb-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7beb-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7beb-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7beb-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d7beb-112">Puntero a la estructura de D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="d7beb-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7beb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7beb-113">Return value</span></span>

<span data-ttu-id="d7beb-114">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7beb-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="d7beb-115">Puntero a una estructura D3DXVECTOR2 que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="d7beb-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7beb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7beb-116">Remarks</span></span>

<span data-ttu-id="d7beb-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d7beb-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d7beb-118">De esta manera, la función D3DXVec2Normalize se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="d7beb-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7beb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7beb-119">Requirements</span></span>



| <span data-ttu-id="d7beb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7beb-120">Requirement</span></span> | <span data-ttu-id="d7beb-121">Value</span><span class="sxs-lookup"><span data-stu-id="d7beb-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7beb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7beb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d7beb-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7beb-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d7beb-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7beb-124">Library</span></span><br/> | <dl> <span data-ttu-id="d7beb-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7beb-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7beb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7beb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7beb-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d7beb-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
