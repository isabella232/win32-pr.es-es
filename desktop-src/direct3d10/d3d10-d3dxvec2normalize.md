---
description: 'Función D3DXVec2Normalize (D3DX10Math.h): devuelve la versión normalizada de un vector 2D.'
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Función D3DXVec2Normalize (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108393"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="43818-103">Función D3DXVec2Normalize (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="43818-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="43818-104">Devuelve la versión normalizada de un vector 2D.</span><span class="sxs-lookup"><span data-stu-id="43818-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="43818-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43818-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="43818-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43818-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43818-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="43818-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43818-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="43818-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="43818-109">Puntero a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="43818-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="43818-110">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43818-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43818-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="43818-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="43818-112">Puntero a la estructura D3DXVECTOR2 de origen.</span><span class="sxs-lookup"><span data-stu-id="43818-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43818-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43818-113">Return value</span></span>

<span data-ttu-id="43818-114">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="43818-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="43818-115">Puntero a una estructura D3DXVECTOR2 que es la versión normalizada del vector.</span><span class="sxs-lookup"><span data-stu-id="43818-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="43818-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43818-116">Remarks</span></span>

<span data-ttu-id="43818-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="43818-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="43818-118">De esta manera, la función D3DXVec2Normalize se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="43818-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="43818-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43818-119">Requirements</span></span>



| <span data-ttu-id="43818-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="43818-120">Requirement</span></span> | <span data-ttu-id="43818-121">Value</span><span class="sxs-lookup"><span data-stu-id="43818-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43818-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43818-122">Header</span></span><br/>  | <dl> <span data-ttu-id="43818-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="43818-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="43818-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43818-124">Library</span></span><br/> | <dl> <span data-ttu-id="43818-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="43818-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43818-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="43818-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43818-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="43818-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
