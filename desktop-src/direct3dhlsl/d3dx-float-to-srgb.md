---
title: D3DX_FLOAT_to_SRGB función)
description: Convierte un valor FLOAT en una SRGB.
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- D3DX_FLOAT_to_SRGB de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998671"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="f400b-104">D3DX \_ float \_ to \_ sRGB (función)</span><span class="sxs-lookup"><span data-stu-id="f400b-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="f400b-105">Convierte un valor FLOAT en una SRGB.</span><span class="sxs-lookup"><span data-stu-id="f400b-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="f400b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f400b-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="f400b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f400b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f400b-108">*Val*</span><span class="sxs-lookup"><span data-stu-id="f400b-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="f400b-109">Valor FLOAT que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="f400b-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f400b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f400b-110">Return value</span></span>

<span data-ttu-id="f400b-111">Valor SRGB convertido.</span><span class="sxs-lookup"><span data-stu-id="f400b-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f400b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f400b-112">Requirements</span></span>



| <span data-ttu-id="f400b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f400b-113">Requirement</span></span> | <span data-ttu-id="f400b-114">Value</span><span class="sxs-lookup"><span data-stu-id="f400b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f400b-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f400b-115">Header</span></span><br/> | <dl> <span data-ttu-id="f400b-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="f400b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f400b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f400b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f400b-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="f400b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f400b-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="f400b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





