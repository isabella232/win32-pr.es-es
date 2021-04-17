---
description: Construye un plano a partir de tres puntos.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Función D3DXPlaneFromPoints (D3dx9math. h)
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
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717552"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="64ba9-103">Función D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="64ba9-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="64ba9-104">Construye un plano a partir de tres puntos.</span><span class="sxs-lookup"><span data-stu-id="64ba9-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ba9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64ba9-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="64ba9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64ba9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64ba9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64ba9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64ba9-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="64ba9-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="64ba9-109">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="64ba9-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="64ba9-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64ba9-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ba9-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="64ba9-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="64ba9-112">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="64ba9-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="64ba9-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64ba9-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ba9-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="64ba9-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="64ba9-115">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="64ba9-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="64ba9-116">*pV3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64ba9-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ba9-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="64ba9-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="64ba9-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define uno de los puntos usados para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="64ba9-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64ba9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64ba9-119">Return value</span></span>

<span data-ttu-id="64ba9-120">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="64ba9-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="64ba9-121">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) construida a partir de los puntos especificados.</span><span class="sxs-lookup"><span data-stu-id="64ba9-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ba9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64ba9-122">Remarks</span></span>

<span data-ttu-id="64ba9-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="64ba9-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="64ba9-124">De esta manera, la función **D3DXPlaneFromPoints** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="64ba9-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ba9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64ba9-125">Requirements</span></span>



| <span data-ttu-id="64ba9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="64ba9-126">Requirement</span></span> | <span data-ttu-id="64ba9-127">Value</span><span class="sxs-lookup"><span data-stu-id="64ba9-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64ba9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64ba9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="64ba9-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="64ba9-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="64ba9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64ba9-130">Library</span></span><br/> | <dl> <span data-ttu-id="64ba9-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64ba9-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64ba9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="64ba9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ba9-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="64ba9-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="64ba9-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="64ba9-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




