---
description: Transforma un vector 4D por una matriz determinada.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Función D3DXVec4Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 56fc6b3041d799cda3e98d459b2523d4b171df10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914713"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="399ab-103">Función D3DXVec4Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="399ab-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="399ab-104">Transforma un vector 4D por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="399ab-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="399ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="399ab-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="399ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="399ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="399ab-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="399ab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="399ab-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="399ab-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="399ab-109">Puntero al [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="399ab-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="399ab-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="399ab-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="399ab-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="399ab-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="399ab-112">Puntero a la estructura de D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="399ab-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="399ab-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="399ab-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="399ab-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="399ab-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="399ab-115">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="399ab-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="399ab-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="399ab-116">Return value</span></span>

<span data-ttu-id="399ab-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="399ab-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="399ab-118">Puntero a una estructura D3DXVECTOR4 que es el vector 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="399ab-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="399ab-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="399ab-119">Remarks</span></span>

<span data-ttu-id="399ab-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="399ab-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="399ab-121">De esta manera, la función D3DXVec4Transform se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="399ab-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="399ab-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="399ab-122">Requirements</span></span>



| <span data-ttu-id="399ab-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="399ab-123">Requirement</span></span> | <span data-ttu-id="399ab-124">Value</span><span class="sxs-lookup"><span data-stu-id="399ab-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="399ab-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="399ab-125">Header</span></span><br/> | <dl> <span data-ttu-id="399ab-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="399ab-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="399ab-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="399ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399ab-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="399ab-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
