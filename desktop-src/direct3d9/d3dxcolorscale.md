---
description: Escala un valor de color.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Función D3DXColorScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678825"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="73989-103">D3DXColorScale función)</span><span class="sxs-lookup"><span data-stu-id="73989-103">D3DXColorScale function</span></span>

<span data-ttu-id="73989-104">Escala un valor de color.</span><span class="sxs-lookup"><span data-stu-id="73989-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="73989-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73989-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="73989-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73989-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73989-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73989-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="73989-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="73989-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="73989-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="73989-110">*PC* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="73989-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73989-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="73989-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="73989-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="73989-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="73989-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="73989-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73989-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73989-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73989-115">Factor de escala.</span><span class="sxs-lookup"><span data-stu-id="73989-115">Scale factor.</span></span> <span data-ttu-id="73989-116">Escala el color y lo trata como un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="73989-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="73989-117">No hay ningún límite en el valor de s.</span><span class="sxs-lookup"><span data-stu-id="73989-117">There are no limits on the value of s.</span></span> <span data-ttu-id="73989-118">Si es 1, el color resultante es el color original.</span><span class="sxs-lookup"><span data-stu-id="73989-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73989-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73989-119">Return value</span></span>

<span data-ttu-id="73989-120">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="73989-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="73989-121">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el valor de color escalado.</span><span class="sxs-lookup"><span data-stu-id="73989-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73989-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73989-122">Remarks</span></span>

<span data-ttu-id="73989-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="73989-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="73989-124">De esta manera, la función **D3DXColorScale** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="73989-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="73989-125">Esta función calcula el valor de color escalado multiplicando los componentes de color de la estructura [**D3DXCOLOR**](d3dxcolor.md) por el factor de escala especificado, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="73989-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="73989-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73989-126">Requirements</span></span>



| <span data-ttu-id="73989-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="73989-127">Requirement</span></span> | <span data-ttu-id="73989-128">Value</span><span class="sxs-lookup"><span data-stu-id="73989-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73989-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73989-129">Header</span></span><br/>  | <dl> <span data-ttu-id="73989-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="73989-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="73989-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73989-131">Library</span></span><br/> | <dl> <span data-ttu-id="73989-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73989-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73989-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="73989-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73989-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="73989-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="73989-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="73989-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="73989-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="73989-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="73989-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="73989-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
