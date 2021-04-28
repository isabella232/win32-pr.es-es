---
description: 'Función D3DXVec3TransformNormal (D3dx9math.h): transforma el vector 3D normal según la matriz especificada.'
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Función D3DXVec3TransformNormal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115623"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="c437c-103">Función D3DXVec3TransformNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c437c-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="c437c-104">Transforma el vector 3D normal según la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="c437c-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c437c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c437c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c437c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c437c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c437c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c437c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c437c-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c437c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c437c-109">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c437c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c437c-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c437c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c437c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c437c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c437c-112">Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.</span><span class="sxs-lookup"><span data-stu-id="c437c-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c437c-113">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c437c-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c437c-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c437c-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c437c-115">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="c437c-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c437c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c437c-116">Return value</span></span>

<span data-ttu-id="c437c-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c437c-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c437c-118">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="c437c-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c437c-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c437c-119">Remarks</span></span>

<span data-ttu-id="c437c-120">Esta función transforma el vector (*pV*->x, *pV*->y, *pV*->z, 0) por la matriz a la que apunta *pM*.</span><span class="sxs-lookup"><span data-stu-id="c437c-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="c437c-121">Si desea transformar un normal, la matriz que pasa a esta función debe ser la transpuesta de la inversa de la matriz que usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="c437c-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="c437c-122">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="c437c-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c437c-123">De esta manera, la **función D3DXVec3TransformNormal** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c437c-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c437c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c437c-124">Requirements</span></span>



| <span data-ttu-id="c437c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c437c-125">Requirement</span></span> | <span data-ttu-id="c437c-126">Value</span><span class="sxs-lookup"><span data-stu-id="c437c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c437c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c437c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c437c-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c437c-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c437c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c437c-129">Library</span></span><br/> | <dl> <span data-ttu-id="c437c-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c437c-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c437c-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c437c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c437c-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c437c-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




