---
description: Construye un plano a partir de un punto y un normal.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Función D3DXPlaneFromPointNormal (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717551"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="eddcd-103">Función D3DXPlaneFromPointNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="eddcd-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="eddcd-104">Construye un plano a partir de un punto y un normal.</span><span class="sxs-lookup"><span data-stu-id="eddcd-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddcd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eddcd-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="eddcd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eddcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddcd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eddcd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eddcd-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="eddcd-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="eddcd-109">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eddcd-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eddcd-110">*PPoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eddcd-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eddcd-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eddcd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eddcd-112">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define el punto usado para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="eddcd-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="eddcd-113">*pNormal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eddcd-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eddcd-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eddcd-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eddcd-115">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) , que define el uso normal para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="eddcd-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddcd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eddcd-116">Return value</span></span>

<span data-ttu-id="eddcd-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="eddcd-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="eddcd-118">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) construida a partir del punto y el normal.</span><span class="sxs-lookup"><span data-stu-id="eddcd-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="eddcd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eddcd-119">Remarks</span></span>

<span data-ttu-id="eddcd-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="eddcd-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eddcd-121">De esta manera, la función **D3DXPlaneFromPointNormal** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="eddcd-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eddcd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eddcd-122">Requirements</span></span>



| <span data-ttu-id="eddcd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eddcd-123">Requirement</span></span> | <span data-ttu-id="eddcd-124">Value</span><span class="sxs-lookup"><span data-stu-id="eddcd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eddcd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eddcd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eddcd-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eddcd-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eddcd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eddcd-127">Library</span></span><br/> | <dl> <span data-ttu-id="eddcd-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eddcd-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eddcd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="eddcd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddcd-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="eddcd-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eddcd-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="eddcd-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




