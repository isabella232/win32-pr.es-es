---
description: 'Función D3DXVec4Cross (D3DX10Math.h): determina el producto cruzado en cuatro dimensiones.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Función D3DXVec4Cross (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102953"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="3d467-103">Función D3DXVec4Cross (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="3d467-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="3d467-104">Determina el producto cruzado en cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3d467-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d467-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d467-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="3d467-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d467-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d467-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d467-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d467-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d467-109">Puntero a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3d467-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3d467-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3d467-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d467-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d467-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d467-112">Puntero a una estructura D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="3d467-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d467-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3d467-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d467-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d467-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d467-115">Puntero a una estructura D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="3d467-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d467-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3d467-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d467-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d467-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d467-118">Puntero a una estructura D3DXVECTOR4 de origen.</span><span class="sxs-lookup"><span data-stu-id="3d467-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d467-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d467-119">Return value</span></span>

<span data-ttu-id="3d467-120">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d467-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="3d467-121">Puntero a una estructura D3DXVECTOR4 que es el producto cruzado.</span><span class="sxs-lookup"><span data-stu-id="3d467-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d467-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d467-122">Remarks</span></span>

<span data-ttu-id="3d467-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3d467-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3d467-124">De este modo, la función D3DXVec4Cross se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="3d467-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d467-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d467-125">Requirements</span></span>



| <span data-ttu-id="3d467-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d467-126">Requirement</span></span> | <span data-ttu-id="3d467-127">Value</span><span class="sxs-lookup"><span data-stu-id="3d467-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d467-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d467-128">Header</span></span><br/> | <dl> <span data-ttu-id="3d467-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3d467-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d467-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3d467-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d467-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3d467-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
