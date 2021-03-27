---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 función)
description: Desempaqueta los \_ \_ \_ \_ datos de sombreador R8G8B8A8 UNORM sRGB Format en XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 función)
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e373ccb8035b19da7c44ee05a07dd0351ca8f48d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986850"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="f3a0f-105">D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 (función)</span><span class="sxs-lookup"><span data-stu-id="f3a0f-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="f3a0f-106">Desempaqueta los \_ \_ \_ \_ datos de sombreador R8G8B8A8 UNORM sRGB Format en XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="f3a0f-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3a0f-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f3a0f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3a0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a0f-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="f3a0f-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a0f-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="f3a0f-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a0f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3a0f-111">Return value</span></span>

<span data-ttu-id="f3a0f-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="f3a0f-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a0f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3a0f-113">Requirements</span></span>



| <span data-ttu-id="f3a0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a0f-114">Requirement</span></span> | <span data-ttu-id="f3a0f-115">Value</span><span class="sxs-lookup"><span data-stu-id="f3a0f-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a0f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3a0f-116">Header</span></span><br/> | <dl> <span data-ttu-id="f3a0f-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="f3a0f-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a0f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3a0f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a0f-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="f3a0f-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f3a0f-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="f3a0f-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





