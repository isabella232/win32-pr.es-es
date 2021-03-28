---
title: D3DX_R16G16_UNORM_to_FLOAT2 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R16G16 UNORM con formato DXGI en un XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- D3DX_R16G16_UNORM_to_FLOAT2 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362510"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a><span data-ttu-id="ac629-104">D3DX \_ R16G16 \_ UNORM \_ a la \_ función FLOAT2</span><span class="sxs-lookup"><span data-stu-id="ac629-104">D3DX\_R16G16\_UNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="ac629-105">Desempaqueta los \_ datos del \_ \_ sombreador de R16G16 UNORM con formato DXGI en un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="ac629-105">Unpacks DXGI\_FORMAT\_R16G16\_UNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac629-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac629-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ac629-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac629-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac629-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="ac629-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ac629-109">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="ac629-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac629-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac629-110">Return value</span></span>

<span data-ttu-id="ac629-111">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="ac629-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac629-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac629-112">Requirements</span></span>



| <span data-ttu-id="ac629-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac629-113">Requirement</span></span> | <span data-ttu-id="ac629-114">Value</span><span class="sxs-lookup"><span data-stu-id="ac629-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac629-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac629-115">Header</span></span><br/> | <dl> <span data-ttu-id="ac629-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="ac629-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac629-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac629-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac629-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="ac629-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ac629-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="ac629-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





