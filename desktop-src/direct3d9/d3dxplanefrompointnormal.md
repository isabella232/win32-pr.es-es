---
description: 'Función D3DXPlaneFromPointNormal (D3dx9math.h): construye un plano a partir de un punto y un normal.'
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Función D3DXPlaneFromPointNormal (D3dx9math.h)
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
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098093"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="f31af-103">Función D3DXPlaneFromPointNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f31af-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="f31af-104">Construye un plano a partir de un punto y un normal.</span><span class="sxs-lookup"><span data-stu-id="f31af-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f31af-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="f31af-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f31af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31af-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f31af-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f31af-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f31af-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f31af-109">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f31af-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f31af-110">*pPoint* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f31af-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31af-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f31af-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f31af-112">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que define el punto utilizado para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="f31af-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="f31af-113">*pNormal* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f31af-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31af-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f31af-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f31af-115">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que define la normal usada para construir el plano.</span><span class="sxs-lookup"><span data-stu-id="f31af-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31af-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f31af-116">Return value</span></span>

<span data-ttu-id="f31af-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f31af-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f31af-118">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) construida a partir del punto y el normal.</span><span class="sxs-lookup"><span data-stu-id="f31af-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31af-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f31af-119">Remarks</span></span>

<span data-ttu-id="f31af-120">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="f31af-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f31af-121">De esta manera, la **función D3DXPlaneFromPointNormal** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="f31af-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31af-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f31af-122">Requirements</span></span>



| <span data-ttu-id="f31af-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31af-123">Requirement</span></span> | <span data-ttu-id="f31af-124">Value</span><span class="sxs-lookup"><span data-stu-id="f31af-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31af-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f31af-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f31af-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f31af-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f31af-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f31af-127">Library</span></span><br/> | <dl> <span data-ttu-id="f31af-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f31af-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f31af-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f31af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31af-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f31af-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f31af-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="f31af-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




