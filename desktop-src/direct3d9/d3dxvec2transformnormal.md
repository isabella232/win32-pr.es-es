---
description: 'Función D3DXVec2TransformNormal (D3dx9math.h): transforma el vector 2D normal según la matriz especificada.'
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Función D3DXVec2TransformNormal (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097913"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="d0f13-103">Función D3DXVec2TransformNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d0f13-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="d0f13-104">Transforma el vector 2D normal según la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="d0f13-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f13-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0f13-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d0f13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0f13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f13-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d0f13-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f13-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0f13-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0f13-109">Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d0f13-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d0f13-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d0f13-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f13-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0f13-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0f13-112">Puntero a la estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="d0f13-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d0f13-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d0f13-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0f13-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d0f13-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d0f13-115">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="d0f13-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f13-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0f13-116">Return value</span></span>

<span data-ttu-id="d0f13-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0f13-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d0f13-118">Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="d0f13-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f13-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0f13-119">Remarks</span></span>

<span data-ttu-id="d0f13-120">Esta función transforma el vector *(pV-*>x, *pV-*>y, 0, 0) por la matriz a la que apunta *pM*.</span><span class="sxs-lookup"><span data-stu-id="d0f13-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="d0f13-121">Si desea transformar un normal, la matriz que pasa a esta función debe ser la transpuesta de la inversa de la matriz que usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="d0f13-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="d0f13-122">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="d0f13-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d0f13-123">De esta manera, la **función D3DXVec2TransformNormal** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="d0f13-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f13-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f13-124">Requirements</span></span>



| <span data-ttu-id="d0f13-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f13-125">Requirement</span></span> | <span data-ttu-id="d0f13-126">Value</span><span class="sxs-lookup"><span data-stu-id="d0f13-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f13-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0f13-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d0f13-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f13-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d0f13-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0f13-129">Library</span></span><br/> | <dl> <span data-ttu-id="d0f13-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0f13-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d0f13-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d0f13-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f13-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d0f13-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d0f13-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="d0f13-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="d0f13-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="d0f13-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




