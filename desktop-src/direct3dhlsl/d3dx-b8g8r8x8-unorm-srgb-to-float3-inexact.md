---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact función)
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986785"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="275d9-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 \_ inexacto (función)</span><span class="sxs-lookup"><span data-stu-id="275d9-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="275d9-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="275d9-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="275d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="275d9-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="275d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="275d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="275d9-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="275d9-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="275d9-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="275d9-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="275d9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="275d9-111">Return value</span></span>

<span data-ttu-id="275d9-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="275d9-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="275d9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="275d9-113">Remarks</span></span>

<span data-ttu-id="275d9-114">Esta función usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="275d9-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="275d9-115">La función alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa una tabla de búsqueda almacenada en el sombreador para dar una conversión de sRGB a Float exacta.</span><span class="sxs-lookup"><span data-stu-id="275d9-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="275d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="275d9-116">Requirements</span></span>



| <span data-ttu-id="275d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="275d9-117">Requirement</span></span> | <span data-ttu-id="275d9-118">Value</span><span class="sxs-lookup"><span data-stu-id="275d9-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="275d9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="275d9-119">Header</span></span><br/> | <dl> <span data-ttu-id="275d9-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="275d9-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="275d9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="275d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="275d9-122">Funciones</span><span class="sxs-lookup"><span data-stu-id="275d9-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="275d9-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="275d9-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





