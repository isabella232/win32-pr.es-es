---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 función)
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998311"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a><span data-ttu-id="141e3-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ a \_ FLOAT3 función</span><span class="sxs-lookup"><span data-stu-id="141e3-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3 function</span></span>

<span data-ttu-id="141e3-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8X8 UNORM sRGB Format en XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="141e3-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="141e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="141e3-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="141e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="141e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141e3-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="141e3-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="141e3-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="141e3-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141e3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="141e3-111">Return value</span></span>

<span data-ttu-id="141e3-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="141e3-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="141e3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="141e3-113">Requirements</span></span>



| <span data-ttu-id="141e3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="141e3-114">Requirement</span></span> | <span data-ttu-id="141e3-115">Value</span><span class="sxs-lookup"><span data-stu-id="141e3-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141e3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="141e3-116">Header</span></span><br/> | <dl> <span data-ttu-id="141e3-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="141e3-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="141e3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="141e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141e3-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="141e3-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="141e3-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="141e3-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





