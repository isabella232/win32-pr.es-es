---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM función)
description: Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ SNORM.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362755"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="581b1-104">D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ función SNORM</span><span class="sxs-lookup"><span data-stu-id="581b1-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="581b1-105">Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ R8G8B8A8 \_ SNORM.</span><span class="sxs-lookup"><span data-stu-id="581b1-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="581b1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="581b1-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="581b1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="581b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="581b1-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="581b1-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="581b1-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="581b1-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="581b1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="581b1-110">Return value</span></span>

<span data-ttu-id="581b1-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="581b1-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="581b1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581b1-112">Requirements</span></span>



| <span data-ttu-id="581b1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="581b1-113">Requirement</span></span> | <span data-ttu-id="581b1-114">Value</span><span class="sxs-lookup"><span data-stu-id="581b1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="581b1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="581b1-115">Header</span></span><br/> | <dl> <span data-ttu-id="581b1-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="581b1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581b1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="581b1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581b1-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="581b1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="581b1-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="581b1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





