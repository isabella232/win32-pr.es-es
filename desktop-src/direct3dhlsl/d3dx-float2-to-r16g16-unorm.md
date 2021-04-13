---
title: D3DX_FLOAT2_to_R16G16_UNORM función)
description: Vuelve a empaquetar el XMFLOAT2 determinado en un formato de DXGI \_ \_ R16G16 \_ UNORM.
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- D3DX_FLOAT2_to_R16G16_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998419"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a><span data-ttu-id="656bd-104">\_FLOAT2 \_ de D3DX \_ R16G16 \_ función UNORM</span><span class="sxs-lookup"><span data-stu-id="656bd-104">D3DX\_FLOAT2\_to\_R16G16\_UNORM function</span></span>

<span data-ttu-id="656bd-105">Vuelve a empaquetar el XMFLOAT2 determinado en un formato de DXGI \_ \_ R16G16 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="656bd-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="656bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="656bd-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="656bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="656bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656bd-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="656bd-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="656bd-109">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="656bd-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656bd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="656bd-110">Return value</span></span>

<span data-ttu-id="656bd-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="656bd-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="656bd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="656bd-112">Requirements</span></span>



| <span data-ttu-id="656bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="656bd-113">Requirement</span></span> | <span data-ttu-id="656bd-114">Value</span><span class="sxs-lookup"><span data-stu-id="656bd-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656bd-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="656bd-115">Header</span></span><br/> | <dl> <span data-ttu-id="656bd-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="656bd-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656bd-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="656bd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656bd-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="656bd-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="656bd-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="656bd-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





