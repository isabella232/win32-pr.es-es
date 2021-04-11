---
description: Resta dos vectores 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Función D3DXVec4Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362826"
---
# <a name="d3dxvec4subtract-function"></a><span data-ttu-id="2d89b-103">D3DXVec4Subtract función)</span><span class="sxs-lookup"><span data-stu-id="2d89b-103">D3DXVec4Subtract function</span></span>

<span data-ttu-id="2d89b-104">Resta dos vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="2d89b-104">Subtracts two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d89b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d89b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2d89b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d89b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d89b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2d89b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d89b-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d89b-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2d89b-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2d89b-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d89b-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d89b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d89b-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d89b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2d89b-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2d89b-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2d89b-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d89b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d89b-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d89b-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2d89b-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="2d89b-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d89b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d89b-116">Return value</span></span>

<span data-ttu-id="2d89b-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d89b-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2d89b-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la diferencia de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="2d89b-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d89b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d89b-119">Remarks</span></span>

<span data-ttu-id="2d89b-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="2d89b-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2d89b-121">De esta manera, la función **D3DXVec4Subtract** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="2d89b-121">In this way, the **D3DXVec4Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d89b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d89b-122">Requirements</span></span>



| <span data-ttu-id="2d89b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d89b-123">Requirement</span></span> | <span data-ttu-id="2d89b-124">Value</span><span class="sxs-lookup"><span data-stu-id="2d89b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d89b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d89b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2d89b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d89b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d89b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d89b-127">Library</span></span><br/> | <dl> <span data-ttu-id="2d89b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d89b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d89b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d89b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d89b-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2d89b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2d89b-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="2d89b-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="2d89b-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="2d89b-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




