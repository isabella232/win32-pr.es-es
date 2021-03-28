---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 función)
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91311bb83aa034410361bea631aa79f86737ff65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362459"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="f21fb-105">D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 (función)</span><span class="sxs-lookup"><span data-stu-id="f21fb-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="f21fb-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador B8G8R8A8 UNORM sRGB Format en XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="f21fb-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21fb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f21fb-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f21fb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f21fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21fb-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="f21fb-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f21fb-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="f21fb-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21fb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f21fb-111">Return value</span></span>

<span data-ttu-id="f21fb-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="f21fb-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21fb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f21fb-113">Requirements</span></span>



| <span data-ttu-id="f21fb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f21fb-114">Requirement</span></span> | <span data-ttu-id="f21fb-115">Value</span><span class="sxs-lookup"><span data-stu-id="f21fb-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21fb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f21fb-116">Header</span></span><br/> | <dl> <span data-ttu-id="f21fb-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="f21fb-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f21fb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f21fb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21fb-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="f21fb-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f21fb-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="f21fb-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





