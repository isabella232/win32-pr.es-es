---
description: Determina el producto cruzado de dos vectores 3D.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Función D3DXVec3Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707872"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="41fbd-103">D3DXVec3Cross función)</span><span class="sxs-lookup"><span data-stu-id="41fbd-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="41fbd-104">Determina el producto cruzado de dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="41fbd-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fbd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41fbd-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="41fbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41fbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fbd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="41fbd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41fbd-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="41fbd-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="41fbd-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="41fbd-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41fbd-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41fbd-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fbd-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="41fbd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="41fbd-112">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="41fbd-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="41fbd-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41fbd-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41fbd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="41fbd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="41fbd-115">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="41fbd-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fbd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41fbd-116">Return value</span></span>

<span data-ttu-id="41fbd-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="41fbd-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="41fbd-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el producto cruzado de dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="41fbd-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="41fbd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41fbd-119">Remarks</span></span>

<span data-ttu-id="41fbd-120">Esta función determina el producto cruzado con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="41fbd-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="41fbd-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="41fbd-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="41fbd-122">De esta manera, la función **D3DXVec3Cross** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="41fbd-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41fbd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41fbd-123">Requirements</span></span>



| <span data-ttu-id="41fbd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fbd-124">Requirement</span></span> | <span data-ttu-id="41fbd-125">Value</span><span class="sxs-lookup"><span data-stu-id="41fbd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41fbd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41fbd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="41fbd-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fbd-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="41fbd-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41fbd-128">Library</span></span><br/> | <dl> <span data-ttu-id="41fbd-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41fbd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41fbd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="41fbd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fbd-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="41fbd-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="41fbd-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="41fbd-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




