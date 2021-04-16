---
description: Crea el valor de color negativo de un valor de color.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Función D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678815"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="d4034-103">D3DXColorNegative función)</span><span class="sxs-lookup"><span data-stu-id="d4034-103">D3DXColorNegative function</span></span>

<span data-ttu-id="d4034-104">Crea el valor de color negativo de un valor de color.</span><span class="sxs-lookup"><span data-stu-id="d4034-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4034-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4034-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="d4034-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4034-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4034-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d4034-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4034-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4034-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d4034-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d4034-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4034-110">*PC* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d4034-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4034-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4034-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d4034-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="d4034-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4034-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4034-113">Return value</span></span>

<span data-ttu-id="d4034-114">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4034-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d4034-115">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el valor de color negativo del valor de color.</span><span class="sxs-lookup"><span data-stu-id="d4034-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4034-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4034-116">Remarks</span></span>

<span data-ttu-id="d4034-117">El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.</span><span class="sxs-lookup"><span data-stu-id="d4034-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="d4034-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d4034-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d4034-119">De esta manera, la función **D3DXColorNegative** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="d4034-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d4034-120">Esta función devuelve el valor de color negativo restando 1,0 de los componentes de color de la estructura [**D3DXCOLOR**](d3dxcolor.md) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4034-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="d4034-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4034-121">Requirements</span></span>



| <span data-ttu-id="d4034-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4034-122">Requirement</span></span> | <span data-ttu-id="d4034-123">Value</span><span class="sxs-lookup"><span data-stu-id="d4034-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4034-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4034-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4034-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4034-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4034-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4034-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4034-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4034-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4034-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4034-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4034-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d4034-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d4034-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="d4034-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="d4034-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="d4034-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="d4034-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="d4034-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




