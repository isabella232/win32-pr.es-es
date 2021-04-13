---
description: Resta dos vectores 3D.
ms.assetid: 09e2cede-a0a3-4a5e-a7e1-e7a98cdc433b
title: Función D3DXVec3Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17f41f2fd133db1064e2ba2778eacc139bab01ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280509"
---
# <a name="d3dxvec3subtract-function"></a><span data-ttu-id="a40cc-103">D3DXVec3Subtract función)</span><span class="sxs-lookup"><span data-stu-id="a40cc-103">D3DXVec3Subtract function</span></span>

<span data-ttu-id="a40cc-104">Resta dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="a40cc-104">Subtracts two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a40cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a40cc-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Subtract(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="a40cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a40cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40cc-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a40cc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a40cc-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a40cc-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a40cc-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a40cc-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a40cc-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a40cc-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40cc-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a40cc-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a40cc-112">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="a40cc-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a40cc-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a40cc-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40cc-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a40cc-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a40cc-115">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="a40cc-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40cc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a40cc-116">Return value</span></span>

<span data-ttu-id="a40cc-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a40cc-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a40cc-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es la diferencia de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="a40cc-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40cc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a40cc-119">Remarks</span></span>

<span data-ttu-id="a40cc-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="a40cc-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a40cc-121">De esta manera, la función **D3DXVec3Subtract** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="a40cc-121">In this way, the **D3DXVec3Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a40cc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a40cc-122">Requirements</span></span>



| <span data-ttu-id="a40cc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40cc-123">Requirement</span></span> | <span data-ttu-id="a40cc-124">Value</span><span class="sxs-lookup"><span data-stu-id="a40cc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a40cc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a40cc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a40cc-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a40cc-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a40cc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a40cc-127">Library</span></span><br/> | <dl> <span data-ttu-id="a40cc-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a40cc-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a40cc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a40cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40cc-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a40cc-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a40cc-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="a40cc-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="a40cc-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="a40cc-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




