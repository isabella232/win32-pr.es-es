---
description: Transforma el vector 2D normal de la matriz especificada.
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Función D3DXVec2TransformNormal (D3dx9math. h)
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
ms.openlocfilehash: 154268b272f6cac00acb1d770d3c919cf65d6297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003842"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="02e0a-103">Función D3DXVec2TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="02e0a-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="02e0a-104">Transforma el vector 2D normal de la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="02e0a-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02e0a-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="02e0a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02e0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e0a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="02e0a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02e0a-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="02e0a-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="02e0a-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="02e0a-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="02e0a-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02e0a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e0a-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="02e0a-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="02e0a-112">Puntero a la estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="02e0a-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="02e0a-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02e0a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e0a-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="02e0a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="02e0a-115">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="02e0a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e0a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02e0a-116">Return value</span></span>

<span data-ttu-id="02e0a-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="02e0a-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="02e0a-118">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="02e0a-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e0a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02e0a-119">Remarks</span></span>

<span data-ttu-id="02e0a-120">Esta función transforma el vector (*PV-*>x, *PV-*>y, 0,0) por la matriz a la que apunta *PM*.</span><span class="sxs-lookup"><span data-stu-id="02e0a-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="02e0a-121">Si desea transformar un normal, la matriz que se pasa a esta función debe ser la transformación del inverso de la matriz que se usaría para transformar un punto.</span><span class="sxs-lookup"><span data-stu-id="02e0a-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="02e0a-122">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="02e0a-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="02e0a-123">De esta manera, la función **D3DXVec2TransformNormal** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="02e0a-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e0a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e0a-124">Requirements</span></span>



| <span data-ttu-id="02e0a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e0a-125">Requirement</span></span> | <span data-ttu-id="02e0a-126">Value</span><span class="sxs-lookup"><span data-stu-id="02e0a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e0a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02e0a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="02e0a-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e0a-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="02e0a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02e0a-129">Library</span></span><br/> | <dl> <span data-ttu-id="02e0a-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02e0a-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02e0a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="02e0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e0a-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="02e0a-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="02e0a-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="02e0a-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="02e0a-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="02e0a-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




