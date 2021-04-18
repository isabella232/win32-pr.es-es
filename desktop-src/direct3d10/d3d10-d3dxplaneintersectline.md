---
description: Busca la intersección entre un plano y una línea.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Función D3DXPlaneIntersectLine (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721518"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="bfc93-103">Función D3DXPlaneIntersectLine (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bfc93-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="bfc93-104">Busca la intersección entre un plano y una línea.</span><span class="sxs-lookup"><span data-stu-id="bfc93-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc93-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfc93-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="bfc93-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfc93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc93-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bfc93-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc93-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bfc93-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bfc93-109">Puntero a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que identifica la intersección entre el plano y la línea especificados.</span><span class="sxs-lookup"><span data-stu-id="bfc93-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="bfc93-110">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfc93-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc93-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfc93-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bfc93-112">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md)de origen.</span><span class="sxs-lookup"><span data-stu-id="bfc93-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfc93-113">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfc93-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc93-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfc93-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bfc93-115">Puntero a una estructura de D3DXVECTOR3 de origen, que define un punto de inicio de línea.</span><span class="sxs-lookup"><span data-stu-id="bfc93-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="bfc93-116">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfc93-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc93-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bfc93-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bfc93-118">Puntero a una estructura D3DXVECTOR3 de origen que define un punto final de línea.</span><span class="sxs-lookup"><span data-stu-id="bfc93-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc93-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfc93-119">Return value</span></span>

<span data-ttu-id="bfc93-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bfc93-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bfc93-121">Puntero a una estructura D3DXVECTOR3 que es la intersección entre el plano y la línea especificados.</span><span class="sxs-lookup"><span data-stu-id="bfc93-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfc93-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfc93-122">Remarks</span></span>

<span data-ttu-id="bfc93-123">Si la línea es paralela al plano, se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="bfc93-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="bfc93-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="bfc93-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bfc93-125">De esta manera, la función D3DXPlaneIntersectLine se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="bfc93-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfc93-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc93-126">Requirements</span></span>



| <span data-ttu-id="bfc93-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc93-127">Requirement</span></span> | <span data-ttu-id="bfc93-128">Value</span><span class="sxs-lookup"><span data-stu-id="bfc93-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc93-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfc93-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bfc93-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc93-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bfc93-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfc93-131">Library</span></span><br/> | <dl> <span data-ttu-id="bfc93-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfc93-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfc93-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfc93-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc93-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bfc93-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
