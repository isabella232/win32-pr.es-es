---
description: 'Función D3DXVec2Transform (D3dx9math.h): transforma un vector 2D mediante una matriz determinada.'
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Función D3DXVec2Transform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097953"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="601c6-103">Función D3DXVec2Transform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="601c6-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="601c6-104">Transforma un vector 2D mediante una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="601c6-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="601c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="601c6-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="601c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="601c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601c6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="601c6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="601c6-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="601c6-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="601c6-109">Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="601c6-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="601c6-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="601c6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601c6-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="601c6-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="601c6-112">Puntero a la estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="601c6-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="601c6-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="601c6-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601c6-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="601c6-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="601c6-115">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="601c6-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601c6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="601c6-116">Return value</span></span>

<span data-ttu-id="601c6-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="601c6-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="601c6-118">Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="601c6-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="601c6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="601c6-119">Remarks</span></span>

<span data-ttu-id="601c6-120">Esta función transforma el vector *pV* (x, y, 0, 1) por el *pM de matriz.*</span><span class="sxs-lookup"><span data-stu-id="601c6-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="601c6-121">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="601c6-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="601c6-122">De esta manera, la **función D3DXVec2Transform** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="601c6-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="601c6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="601c6-123">Requirements</span></span>



| <span data-ttu-id="601c6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="601c6-124">Requirement</span></span> | <span data-ttu-id="601c6-125">Value</span><span class="sxs-lookup"><span data-stu-id="601c6-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="601c6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="601c6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="601c6-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="601c6-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="601c6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="601c6-128">Library</span></span><br/> | <dl> <span data-ttu-id="601c6-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="601c6-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="601c6-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="601c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601c6-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="601c6-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="601c6-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="601c6-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="601c6-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="601c6-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




