---
description: 'Función D3DXColorAdjustSaturation (D3dx9math.h): ajusta el valor de saturación de un color.'
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Función D3DXColorAdjustSaturation (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115873"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="92fe1-103">Función D3DXColorAdjustSaturation (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="92fe1-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="92fe1-104">Ajusta el valor de saturación de un color.</span><span class="sxs-lookup"><span data-stu-id="92fe1-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fe1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92fe1-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="92fe1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92fe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fe1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92fe1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92fe1-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="92fe1-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="92fe1-109">Puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="92fe1-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="92fe1-110">*pC* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="92fe1-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fe1-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="92fe1-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="92fe1-112">Puntero a una estructura [**D3DXCOLOR de**](d3dxcolor.md) origen.</span><span class="sxs-lookup"><span data-stu-id="92fe1-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="92fe1-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="92fe1-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fe1-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92fe1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92fe1-115">Valor de saturación.</span><span class="sxs-lookup"><span data-stu-id="92fe1-115">Saturation value.</span></span> <span data-ttu-id="92fe1-116">Este parámetro interpola linealmente entre el color convertido en escala de grises y el color original, pC.</span><span class="sxs-lookup"><span data-stu-id="92fe1-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="92fe1-117">No hay límites en el valor de s.</span><span class="sxs-lookup"><span data-stu-id="92fe1-117">There are no limits on the value of s.</span></span> <span data-ttu-id="92fe1-118">Si s es 0, el color devuelto es el color de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="92fe1-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="92fe1-119">Si s es 1, el color devuelto es el color original.</span><span class="sxs-lookup"><span data-stu-id="92fe1-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fe1-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92fe1-120">Return value</span></span>

<span data-ttu-id="92fe1-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="92fe1-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="92fe1-122">Esta función devuelve un puntero a una [**estructura D3DXCOLOR**](d3dxcolor.md) que es el resultado del ajuste de saturación.</span><span class="sxs-lookup"><span data-stu-id="92fe1-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="92fe1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92fe1-123">Remarks</span></span>

<span data-ttu-id="92fe1-124">El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.</span><span class="sxs-lookup"><span data-stu-id="92fe1-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="92fe1-125">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="92fe1-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="92fe1-126">De esta manera, esta función se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="92fe1-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="92fe1-127">Esta función interpola los componentes de color rojo, verde y azul de una estructura [**D3DXCOLOR**](d3dxcolor.md) entre un color no saturado y un color, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="92fe1-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="92fe1-128">Si s es mayor que 0 y menor que 1, se reduce la saturación.</span><span class="sxs-lookup"><span data-stu-id="92fe1-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="92fe1-129">Si s es mayor que 1, se aumenta la saturación.</span><span class="sxs-lookup"><span data-stu-id="92fe1-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="92fe1-130">El color de escala de grises se calcula como:</span><span class="sxs-lookup"><span data-stu-id="92fe1-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="92fe1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92fe1-131">Requirements</span></span>



| <span data-ttu-id="92fe1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="92fe1-132">Requirement</span></span> | <span data-ttu-id="92fe1-133">Value</span><span class="sxs-lookup"><span data-stu-id="92fe1-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92fe1-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92fe1-134">Header</span></span><br/>  | <dl> <span data-ttu-id="92fe1-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="92fe1-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="92fe1-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92fe1-136">Library</span></span><br/> | <dl> <span data-ttu-id="92fe1-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="92fe1-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92fe1-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="92fe1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fe1-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="92fe1-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="92fe1-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="92fe1-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
