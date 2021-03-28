---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact función)
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998304"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="41e32-105">D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ inexacto (función)</span><span class="sxs-lookup"><span data-stu-id="41e32-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="41e32-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="41e32-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e32-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41e32-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="41e32-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41e32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e32-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="41e32-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="41e32-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="41e32-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e32-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41e32-111">Return value</span></span>

<span data-ttu-id="41e32-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="41e32-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e32-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41e32-113">Remarks</span></span>

<span data-ttu-id="41e32-114">Esta función usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta.</span><span class="sxs-lookup"><span data-stu-id="41e32-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="41e32-115">La función alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa una tabla de búsqueda almacenada en el sombreador para dar una conversión de sRGB a Float exacta.</span><span class="sxs-lookup"><span data-stu-id="41e32-115">The alternative function [**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e32-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41e32-116">Requirements</span></span>



| <span data-ttu-id="41e32-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e32-117">Requirement</span></span> | <span data-ttu-id="41e32-118">Value</span><span class="sxs-lookup"><span data-stu-id="41e32-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e32-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41e32-119">Header</span></span><br/> | <dl> <span data-ttu-id="41e32-120"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="41e32-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e32-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="41e32-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e32-122">Funciones</span><span class="sxs-lookup"><span data-stu-id="41e32-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="41e32-123">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="41e32-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





