---
title: D3DX_SRGB_to_FLOAT_inexact función)
description: Convierte un valor SRGB en FLOAT. | D3DX_SRGB_to_FLOAT_inexact función)
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986881"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="c8a36-105">D3DX \_ sRGB \_ a \_ float \_ inexacto (función)</span><span class="sxs-lookup"><span data-stu-id="c8a36-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="c8a36-106">Convierte un valor SRGB en FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c8a36-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a36-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8a36-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="c8a36-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8a36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a36-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="c8a36-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="c8a36-110">Valor SRGB que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="c8a36-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a36-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8a36-111">Return value</span></span>

<span data-ttu-id="c8a36-112">Valor SRGB convertido.</span><span class="sxs-lookup"><span data-stu-id="c8a36-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a36-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8a36-113">Remarks</span></span>

<span data-ttu-id="c8a36-114">Esta función no tiene una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="c8a36-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="c8a36-115">La función alternativa de [**D3DX \_ sRGB \_ a \_ float**](d3dx-srgb-to-float.md) usa una tabla de búsqueda para proporcionar una conversión de sRGB a Float exacta.</span><span class="sxs-lookup"><span data-stu-id="c8a36-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a36-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a36-116">Requirements</span></span>



| <span data-ttu-id="c8a36-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a36-117">Requirement</span></span> | <span data-ttu-id="c8a36-118">Value</span><span class="sxs-lookup"><span data-stu-id="c8a36-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a36-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8a36-119">Header</span></span><br/> | <dl> <span data-ttu-id="c8a36-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="c8a36-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a36-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8a36-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a36-122">Funciones</span><span class="sxs-lookup"><span data-stu-id="c8a36-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c8a36-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="c8a36-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





