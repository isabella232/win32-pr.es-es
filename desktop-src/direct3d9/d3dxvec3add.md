---
description: Agrega dos vectores 3D.
ms.assetid: 2979e291-786b-4bc9-b584-421f08db949a
title: Función D3DXVec3Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16fb06c5e7b32506a94a5828fe7f5e1305afff7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698352"
---
# <a name="d3dxvec3add-function"></a><span data-ttu-id="5bd01-103">D3DXVec3Add función)</span><span class="sxs-lookup"><span data-stu-id="5bd01-103">D3DXVec3Add function</span></span>

<span data-ttu-id="5bd01-104">Agrega dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="5bd01-104">Adds two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd01-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bd01-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Add(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="5bd01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bd01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd01-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5bd01-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd01-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5bd01-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5bd01-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5bd01-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5bd01-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bd01-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd01-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5bd01-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5bd01-112">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="5bd01-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5bd01-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5bd01-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd01-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5bd01-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5bd01-115">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="5bd01-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd01-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bd01-116">Return value</span></span>

<span data-ttu-id="5bd01-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5bd01-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5bd01-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la suma de los dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="5bd01-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the sum of the two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd01-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bd01-119">Remarks</span></span>

<span data-ttu-id="5bd01-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="5bd01-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5bd01-121">De esta manera, la función **D3DXVec3Add** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="5bd01-121">In this way, the **D3DXVec3Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bd01-122">Requirements</span></span>



| <span data-ttu-id="5bd01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd01-123">Requirement</span></span> | <span data-ttu-id="5bd01-124">Value</span><span class="sxs-lookup"><span data-stu-id="5bd01-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd01-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bd01-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5bd01-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bd01-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5bd01-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bd01-127">Library</span></span><br/> | <dl> <span data-ttu-id="5bd01-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bd01-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5bd01-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bd01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd01-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="5bd01-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5bd01-131">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="5bd01-131">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> <dt>

[<span data-ttu-id="5bd01-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="5bd01-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




