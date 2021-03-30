---
description: Transforma un vector 2D por una matriz determinada.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Función D3DXVec2Transform (D3dx9math. h)
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
ms.openlocfilehash: 71dd9c0fee853afe0aee3a514308142241655835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280297"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="8dfd2-103">Función D3DXVec2Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8dfd2-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="8dfd2-104">Transforma un vector 2D por una matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfd2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dfd2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8dfd2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8dfd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dfd2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8dfd2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfd2-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dfd2-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8dfd2-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8dfd2-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8dfd2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfd2-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dfd2-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8dfd2-112">Puntero a la estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8dfd2-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8dfd2-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dfd2-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8dfd2-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8dfd2-115">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dfd2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dfd2-116">Return value</span></span>

<span data-ttu-id="8dfd2-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dfd2-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8dfd2-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfd2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8dfd2-119">Remarks</span></span>

<span data-ttu-id="8dfd2-120">Esta función transforma el vector *PV* (x, y, 0, 1) de la matriz *PM*.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="8dfd2-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="8dfd2-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8dfd2-122">De esta manera, la función **D3DXVec2Transform** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="8dfd2-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfd2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dfd2-123">Requirements</span></span>



| <span data-ttu-id="8dfd2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dfd2-124">Requirement</span></span> | <span data-ttu-id="8dfd2-125">Value</span><span class="sxs-lookup"><span data-stu-id="8dfd2-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfd2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dfd2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8dfd2-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dfd2-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8dfd2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dfd2-128">Library</span></span><br/> | <dl> <span data-ttu-id="8dfd2-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dfd2-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8dfd2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dfd2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfd2-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8dfd2-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8dfd2-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="8dfd2-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="8dfd2-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="8dfd2-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




