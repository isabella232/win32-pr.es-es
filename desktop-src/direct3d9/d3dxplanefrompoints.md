---
description: 'Función D3DXPlaneFromPoints (D3dx9math.h): construye un plano a partir de tres puntos.'
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Función D3DXPlaneFromPoints (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d945dff9c124f4c66cea4f9d61c490c6eaf7a66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094163"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="2b3ba-103">Función D3DXPlaneFromPoints (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2b3ba-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="2b3ba-104">Construye un plano a partir de tres puntos.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b3ba-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="2b3ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b3ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b3ba-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2b3ba-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b3ba-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b3ba-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2b3ba-109">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2b3ba-110">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b3ba-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b3ba-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b3ba-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b3ba-112">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="2b3ba-113">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b3ba-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b3ba-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b3ba-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b3ba-115">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="2b3ba-116">*pV3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b3ba-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b3ba-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b3ba-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b3ba-118">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b3ba-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b3ba-119">Return value</span></span>

<span data-ttu-id="2b3ba-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b3ba-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2b3ba-121">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) construida a partir de los puntos dados.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b3ba-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b3ba-122">Remarks</span></span>

<span data-ttu-id="2b3ba-123">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="2b3ba-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2b3ba-124">De esta manera, la **función D3DXPlaneFromPoints** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="2b3ba-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3ba-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b3ba-125">Requirements</span></span>



| <span data-ttu-id="2b3ba-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b3ba-126">Requirement</span></span> | <span data-ttu-id="2b3ba-127">Value</span><span class="sxs-lookup"><span data-stu-id="2b3ba-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3ba-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b3ba-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2b3ba-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b3ba-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b3ba-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b3ba-130">Library</span></span><br/> | <dl> <span data-ttu-id="2b3ba-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b3ba-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b3ba-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2b3ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3ba-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="2b3ba-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2b3ba-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="2b3ba-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




