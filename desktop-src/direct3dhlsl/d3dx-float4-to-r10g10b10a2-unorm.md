---
title: D3DX_FLOAT4_to_R10G10B10A2_UNORM función)
description: Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R10G10B10A2 \_ UNORM.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986761"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a><span data-ttu-id="a73b9-104">D3DX \_ FLOAT4 \_ a \_ R10G10B10A2 \_ función UNORM</span><span class="sxs-lookup"><span data-stu-id="a73b9-104">D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM function</span></span>

<span data-ttu-id="a73b9-105">Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R10G10B10A2 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="a73b9-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73b9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a73b9-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="a73b9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a73b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73b9-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="a73b9-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a73b9-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="a73b9-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73b9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a73b9-110">Return value</span></span>

<span data-ttu-id="a73b9-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="a73b9-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73b9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73b9-112">Requirements</span></span>



| <span data-ttu-id="a73b9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73b9-113">Requirement</span></span> | <span data-ttu-id="a73b9-114">Value</span><span class="sxs-lookup"><span data-stu-id="a73b9-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73b9-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a73b9-115">Header</span></span><br/> | <dl> <span data-ttu-id="a73b9-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="a73b9-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73b9-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a73b9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73b9-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="a73b9-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a73b9-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="a73b9-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





