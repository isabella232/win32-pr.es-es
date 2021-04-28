---
description: 'Función D3DXPlaneFromPoints (D3DX10Math.h): construye un plano a partir de tres puntos.'
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: Función D3DXPlaneFromPoints (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103323"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="991de-103">Función D3DXPlaneFromPoints (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="991de-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="991de-104">Construye un plano a partir de tres puntos.</span><span class="sxs-lookup"><span data-stu-id="991de-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="991de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="991de-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="991de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="991de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991de-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="991de-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="991de-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="991de-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="991de-109">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="991de-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="991de-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="991de-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="991de-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="991de-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="991de-112">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="991de-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="991de-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="991de-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="991de-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="991de-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="991de-115">Puntero a una estructura D3DXVECTOR3, que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="991de-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="991de-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="991de-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="991de-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="991de-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="991de-118">Puntero a una estructura D3DXVECTOR3, que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="991de-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991de-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="991de-119">Return value</span></span>

<span data-ttu-id="991de-120">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="991de-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="991de-121">Puntero a la estructura D3DXPLANE construida a partir de los puntos dados.</span><span class="sxs-lookup"><span data-stu-id="991de-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="991de-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="991de-122">Remarks</span></span>

<span data-ttu-id="991de-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="991de-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="991de-124">De esta manera, la función D3DXPlaneFromPoints se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="991de-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="991de-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991de-125">Requirements</span></span>



| <span data-ttu-id="991de-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="991de-126">Requirement</span></span> | <span data-ttu-id="991de-127">Value</span><span class="sxs-lookup"><span data-stu-id="991de-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="991de-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="991de-128">Header</span></span><br/>  | <dl> <span data-ttu-id="991de-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="991de-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="991de-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="991de-130">Library</span></span><br/> | <dl> <span data-ttu-id="991de-131"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="991de-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="991de-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="991de-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991de-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="991de-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
