---
description: 'Función D3DXVec2Normalize (D3dx9math.h): devuelve la versión normalizada de un vector 2D.'
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: Función D3DXVec2Normalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097973"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="32cec-103">Función D3DXVec2Normalize (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="32cec-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="32cec-104">Devuelve la versión normalizada de un vector 2D.</span><span class="sxs-lookup"><span data-stu-id="32cec-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="32cec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32cec-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="32cec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32cec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32cec-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32cec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32cec-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="32cec-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32cec-109">Puntero a la [**estructura D3DXVECTOR2**](d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="32cec-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32cec-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="32cec-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32cec-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="32cec-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32cec-112">Puntero a la estructura [**D3DXVECTOR2 de**](d3dxvector2.md) origen.</span><span class="sxs-lookup"><span data-stu-id="32cec-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32cec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32cec-113">Return value</span></span>

<span data-ttu-id="32cec-114">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="32cec-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32cec-115">Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="32cec-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="32cec-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="32cec-116">Remarks</span></span>

<span data-ttu-id="32cec-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="32cec-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32cec-118">De este modo, la **función D3DXVec2Normalize** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="32cec-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32cec-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32cec-119">Requirements</span></span>



| <span data-ttu-id="32cec-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32cec-120">Requirement</span></span> | <span data-ttu-id="32cec-121">Value</span><span class="sxs-lookup"><span data-stu-id="32cec-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32cec-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32cec-122">Header</span></span><br/>  | <dl> <span data-ttu-id="32cec-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="32cec-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32cec-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32cec-124">Library</span></span><br/> | <dl> <span data-ttu-id="32cec-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="32cec-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32cec-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="32cec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32cec-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="32cec-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




