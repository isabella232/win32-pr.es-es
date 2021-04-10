---
description: Combina dos colores.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: Función D3DXColorModulate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280392"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="6c09a-103">D3DXColorModulate función)</span><span class="sxs-lookup"><span data-stu-id="6c09a-103">D3DXColorModulate function</span></span>

<span data-ttu-id="6c09a-104">Combina dos colores.</span><span class="sxs-lookup"><span data-stu-id="6c09a-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c09a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c09a-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="6c09a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c09a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c09a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c09a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c09a-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c09a-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6c09a-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6c09a-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6c09a-110">*pC1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c09a-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c09a-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c09a-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6c09a-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="6c09a-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6c09a-113">*pC2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c09a-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c09a-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c09a-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6c09a-115">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="6c09a-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c09a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c09a-116">Return value</span></span>

<span data-ttu-id="6c09a-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c09a-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="6c09a-118">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación de combinación.</span><span class="sxs-lookup"><span data-stu-id="6c09a-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c09a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c09a-119">Remarks</span></span>

<span data-ttu-id="6c09a-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="6c09a-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6c09a-121">De esta manera, la función **D3DXColorModulate** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="6c09a-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6c09a-122">Esta función combina dos colores multiplicando los componentes de color coincidentes, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6c09a-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="6c09a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c09a-123">Requirements</span></span>



| <span data-ttu-id="6c09a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c09a-124">Requirement</span></span> | <span data-ttu-id="6c09a-125">Value</span><span class="sxs-lookup"><span data-stu-id="6c09a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c09a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c09a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6c09a-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c09a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6c09a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c09a-128">Library</span></span><br/> | <dl> <span data-ttu-id="6c09a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c09a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c09a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c09a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c09a-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6c09a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6c09a-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="6c09a-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="6c09a-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="6c09a-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="6c09a-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="6c09a-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




