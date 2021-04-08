---
description: Agrega dos vectores 2D.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Función D3DXVec2Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003796"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="00468-103">D3DXVec2Add función)</span><span class="sxs-lookup"><span data-stu-id="00468-103">D3DXVec2Add function</span></span>

<span data-ttu-id="00468-104">Agrega dos vectores 2D.</span><span class="sxs-lookup"><span data-stu-id="00468-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="00468-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00468-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="00468-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00468-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00468-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="00468-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00468-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="00468-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="00468-109">Puntero a la estructura [**D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="00468-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="00468-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00468-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00468-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="00468-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="00468-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="00468-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="00468-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00468-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00468-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="00468-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="00468-115">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="00468-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00468-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00468-116">Return value</span></span>

<span data-ttu-id="00468-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="00468-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="00468-118">Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que es la suma de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="00468-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="00468-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00468-119">Remarks</span></span>

<span data-ttu-id="00468-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="00468-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="00468-121">De esta manera, la función **D3DXVec2Add** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="00468-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="00468-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00468-122">Requirements</span></span>



| <span data-ttu-id="00468-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="00468-123">Requirement</span></span> | <span data-ttu-id="00468-124">Value</span><span class="sxs-lookup"><span data-stu-id="00468-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00468-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00468-125">Header</span></span><br/>  | <dl> <span data-ttu-id="00468-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="00468-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="00468-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00468-127">Library</span></span><br/> | <dl> <span data-ttu-id="00468-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00468-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00468-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="00468-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00468-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="00468-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="00468-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="00468-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="00468-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="00468-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




