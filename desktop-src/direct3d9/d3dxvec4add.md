---
description: Agrega dos vectores 4D.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: Función D3DXVec4Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649445"
---
# <a name="d3dxvec4add-function"></a><span data-ttu-id="b3b65-103">D3DXVec4Add función)</span><span class="sxs-lookup"><span data-stu-id="b3b65-103">D3DXVec4Add function</span></span>

<span data-ttu-id="b3b65-104">Agrega dos vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="b3b65-104">Adds two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b65-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3b65-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="b3b65-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3b65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3b65-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3b65-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b65-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3b65-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="b3b65-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b3b65-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3b65-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3b65-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b65-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3b65-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="b3b65-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="b3b65-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3b65-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3b65-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b65-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3b65-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="b3b65-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="b3b65-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3b65-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3b65-116">Return value</span></span>

<span data-ttu-id="b3b65-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3b65-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="b3b65-118">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la suma de los dos vectores.</span><span class="sxs-lookup"><span data-stu-id="b3b65-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b65-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3b65-119">Remarks</span></span>

<span data-ttu-id="b3b65-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="b3b65-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b3b65-121">De esta manera, la función **D3DXVec4Add** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="b3b65-121">In this way, the **D3DXVec4Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b65-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b65-122">Requirements</span></span>



| <span data-ttu-id="b3b65-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b65-123">Requirement</span></span> | <span data-ttu-id="b3b65-124">Value</span><span class="sxs-lookup"><span data-stu-id="b3b65-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b65-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3b65-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b3b65-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b65-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3b65-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3b65-127">Library</span></span><br/> | <dl> <span data-ttu-id="b3b65-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3b65-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3b65-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3b65-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b65-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b3b65-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b3b65-131">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="b3b65-131">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> <dt>

[<span data-ttu-id="b3b65-132">**D3DXVec4Scale**</span><span class="sxs-lookup"><span data-stu-id="b3b65-132">**D3DXVec4Scale**</span></span>](d3dxvec4scale.md)
</dt> </dl>

 

 




