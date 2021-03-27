---
title: D3DX_SRGB_to_FLOAT función)
description: Convierte un valor SRGB en FLOAT. | D3DX_SRGB_to_FLOAT función)
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- D3DX_SRGB_to_FLOAT de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003849"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="57a6d-105">D3DX \_ sRGB \_ a \_ función Float</span><span class="sxs-lookup"><span data-stu-id="57a6d-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="57a6d-106">Convierte un valor SRGB en FLOAT.</span><span class="sxs-lookup"><span data-stu-id="57a6d-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a6d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57a6d-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="57a6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57a6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a6d-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="57a6d-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="57a6d-110">Valor SRGB que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="57a6d-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a6d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57a6d-111">Return value</span></span>

<span data-ttu-id="57a6d-112">Valor SRGB convertido.</span><span class="sxs-lookup"><span data-stu-id="57a6d-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a6d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a6d-113">Requirements</span></span>



| <span data-ttu-id="57a6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a6d-114">Requirement</span></span> | <span data-ttu-id="57a6d-115">Value</span><span class="sxs-lookup"><span data-stu-id="57a6d-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a6d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57a6d-116">Header</span></span><br/> | <dl> <span data-ttu-id="57a6d-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="57a6d-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a6d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="57a6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a6d-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="57a6d-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="57a6d-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="57a6d-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





