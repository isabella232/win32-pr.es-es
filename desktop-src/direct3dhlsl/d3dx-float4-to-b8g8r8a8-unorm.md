---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM función)
description: Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM.
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986869"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a><span data-ttu-id="2d3f3-104">D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ función UNORM</span><span class="sxs-lookup"><span data-stu-id="2d3f3-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM function</span></span>

<span data-ttu-id="2d3f3-105">Vuelve a empaquetar el XMFLOAT4 determinado en un formato de DXGI \_ \_ B8G8R8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_B8G8R8A8\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3f3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d3f3-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="2d3f3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d3f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3f3-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="2d3f3-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2d3f3-109">Datos del sombreador que se van a empaquetar.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3f3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d3f3-110">Return value</span></span>

<span data-ttu-id="2d3f3-111">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="2d3f3-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3f3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d3f3-112">Requirements</span></span>



| <span data-ttu-id="2d3f3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d3f3-113">Requirement</span></span> | <span data-ttu-id="2d3f3-114">Value</span><span class="sxs-lookup"><span data-stu-id="2d3f3-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3f3-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d3f3-115">Header</span></span><br/> | <dl> <span data-ttu-id="2d3f3-116"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="2d3f3-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3f3-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d3f3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3f3-118">Funciones</span><span class="sxs-lookup"><span data-stu-id="2d3f3-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2d3f3-119">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="2d3f3-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





