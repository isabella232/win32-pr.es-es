---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador R8G8B8A8 UNORM sRGB Format en XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact función)
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003862"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="33b35-105">D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto (función)</span><span class="sxs-lookup"><span data-stu-id="33b35-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="33b35-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador R8G8B8A8 UNORM sRGB Format en XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="33b35-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b35-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33b35-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="33b35-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33b35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b35-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="33b35-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="33b35-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="33b35-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b35-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33b35-111">Return value</span></span>

<span data-ttu-id="33b35-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="33b35-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b35-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33b35-113">Remarks</span></span>

<span data-ttu-id="33b35-114">Esta función usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="33b35-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="33b35-115">La función alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa una tabla de búsqueda almacenada en el sombreador para dar una conversión de sRGB a Float exacta.</span><span class="sxs-lookup"><span data-stu-id="33b35-115">The alternative function [**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b35-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33b35-116">Requirements</span></span>



| <span data-ttu-id="33b35-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33b35-117">Requirement</span></span> | <span data-ttu-id="33b35-118">Value</span><span class="sxs-lookup"><span data-stu-id="33b35-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b35-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33b35-119">Header</span></span><br/> | <dl> <span data-ttu-id="33b35-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="33b35-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33b35-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="33b35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b35-122">Funciones</span><span class="sxs-lookup"><span data-stu-id="33b35-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="33b35-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="33b35-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





