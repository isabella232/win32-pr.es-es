---
description: 'Función D3DXVec4Transform (D3DX10Math.h): transforma un vector 4D mediante una matriz determinada.'
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Función D3DXVec4Transform (D3DX10Math.h)
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
ms.openlocfilehash: 737e1901a514a3940790ce83c7e9bc1f6f471371
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102923"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="8d007-103">Función D3DXVec4Transform (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8d007-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="8d007-104">Transforma un vector 4D mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="8d007-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d007-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d007-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8d007-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d007-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d007-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8d007-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d007-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d007-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8d007-109">Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8d007-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8d007-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8d007-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d007-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d007-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8d007-112">Puntero a la estructura D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="8d007-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="8d007-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8d007-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d007-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d007-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8d007-115">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="8d007-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d007-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d007-116">Return value</span></span>

<span data-ttu-id="8d007-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d007-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8d007-118">Puntero a una estructura D3DXVECTOR4 que es el vector 4D transformado.</span><span class="sxs-lookup"><span data-stu-id="8d007-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d007-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d007-119">Remarks</span></span>

<span data-ttu-id="8d007-120">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="8d007-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8d007-121">De esta manera, la función D3DXVec4Transform se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="8d007-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d007-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d007-122">Requirements</span></span>



| <span data-ttu-id="8d007-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d007-123">Requirement</span></span> | <span data-ttu-id="8d007-124">Value</span><span class="sxs-lookup"><span data-stu-id="8d007-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d007-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d007-125">Header</span></span><br/> | <dl> <span data-ttu-id="8d007-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8d007-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d007-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8d007-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d007-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8d007-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
