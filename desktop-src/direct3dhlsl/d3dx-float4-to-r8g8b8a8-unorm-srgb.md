---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB función)
description: Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362753"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a><span data-ttu-id="a6a8f-104">D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ sRGB function</span><span class="sxs-lookup"><span data-stu-id="a6a8f-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="a6a8f-105">Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="a6a8f-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a8f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6a8f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="a6a8f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6a8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a8f-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="a6a8f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a8f-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="a6a8f-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a8f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6a8f-110">Return value</span></span>

<span data-ttu-id="a6a8f-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="a6a8f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a8f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a8f-112">Requirements</span></span>



| <span data-ttu-id="a6a8f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a8f-113">Requirement</span></span> | <span data-ttu-id="a6a8f-114">Value</span><span class="sxs-lookup"><span data-stu-id="a6a8f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a8f-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6a8f-115">Header</span></span><br/> | <dl> <span data-ttu-id="a6a8f-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="a6a8f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a8f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6a8f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a8f-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="a6a8f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a6a8f-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="a6a8f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





