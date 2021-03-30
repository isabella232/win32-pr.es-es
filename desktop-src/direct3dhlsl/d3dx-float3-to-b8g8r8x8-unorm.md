---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM función)
description: Empaqueta el XMFLOAT3 determinado en un formato de DXGI \_ \_ B8G8R8X8 \_ UNORM uint.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998418"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a><span data-ttu-id="12e76-104">\_FLOAT3 \_ de D3DX \_ B8G8R8X8 \_ función UNORM</span><span class="sxs-lookup"><span data-stu-id="12e76-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM function</span></span>

<span data-ttu-id="12e76-105">Empaqueta el XMFLOAT3 determinado en un formato de DXGI \_ \_ B8G8R8X8 \_ UNORM uint.</span><span class="sxs-lookup"><span data-stu-id="12e76-105">Packs the given XMFLOAT3 into a DXGI\_FORMAT\_B8G8R8X8\_UNORM UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e76-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12e76-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="12e76-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12e76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e76-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="12e76-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="12e76-109">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="12e76-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e76-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12e76-110">Return value</span></span>

<span data-ttu-id="12e76-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="12e76-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e76-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12e76-112">Requirements</span></span>



| <span data-ttu-id="12e76-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e76-113">Requirement</span></span> | <span data-ttu-id="12e76-114">Value</span><span class="sxs-lookup"><span data-stu-id="12e76-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e76-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12e76-115">Header</span></span><br/> | <dl> <span data-ttu-id="12e76-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="12e76-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e76-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="12e76-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e76-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="12e76-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="12e76-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="12e76-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





