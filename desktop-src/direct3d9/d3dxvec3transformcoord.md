---
description: Transforma un vector 3D por una matriz determinada y proyecta el resultado de nuevo en w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: Función D3DXVec3TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4bcf1a78f9da4cf5fb2a5f67360a1659182c7ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362791"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="61187-103">Función D3DXVec3TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="61187-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="61187-104">Transforma un vector 3D por una matriz determinada y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="61187-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="61187-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61187-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="61187-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61187-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61187-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61187-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61187-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="61187-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="61187-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="61187-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="61187-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61187-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61187-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="61187-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="61187-112">Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="61187-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="61187-113">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61187-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61187-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="61187-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="61187-115">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="61187-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61187-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61187-116">Return value</span></span>

<span data-ttu-id="61187-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="61187-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="61187-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el vector transformado.</span><span class="sxs-lookup"><span data-stu-id="61187-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="61187-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61187-119">Remarks</span></span>

<span data-ttu-id="61187-120">Esta función transforma el vector, *PV* (x, y, z, 1), por la matriz, *PM*, y proyecta el resultado de nuevo en w = 1.</span><span class="sxs-lookup"><span data-stu-id="61187-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="61187-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="61187-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="61187-122">De esta manera, la función **D3DXVec3TransformCoord** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="61187-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="61187-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61187-123">Requirements</span></span>



| <span data-ttu-id="61187-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="61187-124">Requirement</span></span> | <span data-ttu-id="61187-125">Value</span><span class="sxs-lookup"><span data-stu-id="61187-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61187-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61187-126">Header</span></span><br/>  | <dl> <span data-ttu-id="61187-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="61187-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="61187-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61187-128">Library</span></span><br/> | <dl> <span data-ttu-id="61187-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61187-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="61187-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="61187-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61187-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="61187-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="61187-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="61187-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="61187-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="61187-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




