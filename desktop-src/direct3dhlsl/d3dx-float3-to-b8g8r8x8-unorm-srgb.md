---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB función)
description: Vuelve a empaquetar el XMFLOAT3 determinado en un formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998370"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="164c1-104">D3DX \_ FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="164c1-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="164c1-105">Vuelve a empaquetar el XMFLOAT3 determinado en un formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="164c1-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="164c1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="164c1-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="164c1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="164c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="164c1-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="164c1-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="164c1-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="164c1-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="164c1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="164c1-110">Return value</span></span>

<span data-ttu-id="164c1-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="164c1-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="164c1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="164c1-112">Requirements</span></span>



| <span data-ttu-id="164c1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="164c1-113">Requirement</span></span> | <span data-ttu-id="164c1-114">Value</span><span class="sxs-lookup"><span data-stu-id="164c1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164c1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="164c1-115">Header</span></span><br/> | <dl> <span data-ttu-id="164c1-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="164c1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164c1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="164c1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164c1-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="164c1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="164c1-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="164c1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





