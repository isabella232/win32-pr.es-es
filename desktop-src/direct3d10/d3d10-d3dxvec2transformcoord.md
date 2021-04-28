---
description: 'Función D3DXVec2TransformCoord (D3DX10Math.h): transforma un vector 2D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.'
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Función D3DXVec2TransformCoord (D3DX10Math.h)
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
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108343"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="0672f-103">Función D3DXVec2TransformCoord (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="0672f-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="0672f-104">Transforma un vector 2D mediante una matriz determinada, proyectando el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="0672f-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="0672f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0672f-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0672f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0672f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0672f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0672f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0672f-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="0672f-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0672f-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="0672f-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0672f-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0672f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0672f-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="0672f-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0672f-112">Puntero a la estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="0672f-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="0672f-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0672f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0672f-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0672f-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0672f-115">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="0672f-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0672f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0672f-116">Return value</span></span>

<span data-ttu-id="0672f-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="0672f-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="0672f-118">Puntero a una estructura D3DXVECTOR2 que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="0672f-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="0672f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0672f-119">Remarks</span></span>

<span data-ttu-id="0672f-120">Esta función transforma el vector, pV (x, y, 0, 1), por la matriz, pM, proyectando el resultado de nuevo en w=1.</span><span class="sxs-lookup"><span data-stu-id="0672f-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="0672f-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="0672f-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0672f-122">De esta manera, la función D3DXVec2TransformCoord se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="0672f-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0672f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0672f-123">Requirements</span></span>



| <span data-ttu-id="0672f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0672f-124">Requirement</span></span> | <span data-ttu-id="0672f-125">Value</span><span class="sxs-lookup"><span data-stu-id="0672f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0672f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0672f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0672f-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0672f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0672f-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0672f-128">Library</span></span><br/> | <dl> <span data-ttu-id="0672f-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0672f-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0672f-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0672f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0672f-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0672f-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
