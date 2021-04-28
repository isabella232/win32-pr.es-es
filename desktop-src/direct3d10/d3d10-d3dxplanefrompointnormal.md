---
description: 'Función D3DXPlaneFromPointNormal (D3DX10Math.h): construye un plano a partir de un punto y un normal.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Función D3DXPlaneFromPointNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108843"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="bd734-103">Función D3DXPlaneFromPointNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bd734-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="bd734-104">Construye un plano a partir de un punto y un normal.</span><span class="sxs-lookup"><span data-stu-id="bd734-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd734-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd734-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="bd734-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd734-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd734-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd734-108">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd734-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bd734-109">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="bd734-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bd734-110">*pPoint* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd734-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd734-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd734-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bd734-112">Puntero a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), que define el punto utilizado para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="bd734-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="bd734-113">*pNormal* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bd734-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd734-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd734-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bd734-115">Puntero a una estructura D3DXVECTOR3, que define el normal utilizado para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="bd734-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd734-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd734-116">Return value</span></span>

<span data-ttu-id="bd734-117">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd734-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="bd734-118">Puntero a la estructura D3DXPLANE construida a partir del punto y el valor normal.</span><span class="sxs-lookup"><span data-stu-id="bd734-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd734-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd734-119">Remarks</span></span>

<span data-ttu-id="bd734-120">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="bd734-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bd734-121">De esta manera, la función D3DXPlaneFromPointNormal se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="bd734-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd734-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd734-122">Requirements</span></span>



| <span data-ttu-id="bd734-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd734-123">Requirement</span></span> | <span data-ttu-id="bd734-124">Value</span><span class="sxs-lookup"><span data-stu-id="bd734-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd734-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd734-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bd734-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd734-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bd734-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd734-127">Library</span></span><br/> | <dl> <span data-ttu-id="bd734-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd734-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd734-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd734-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd734-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bd734-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
