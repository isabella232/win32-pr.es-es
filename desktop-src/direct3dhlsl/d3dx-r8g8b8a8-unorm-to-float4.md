---
title: D3DX_R8G8B8A8_UNORM_to_FLOAT4 función)
description: Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4. | D3DX_R8G8B8A8_UNORM_to_FLOAT4 función)
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4 de la función HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e24b9f29d2e54f62582407e8ad40488032f8a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362509"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a><span data-ttu-id="7f83f-105">D3DX \_ R8G8B8A8 \_ UNORM \_ a la \_ función FLOAT4</span><span class="sxs-lookup"><span data-stu-id="7f83f-105">D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="7f83f-106">Desempaqueta los \_ datos del \_ \_ sombreador de R8G8B8A8 UNORM con formato DXGI en un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="7f83f-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f83f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f83f-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="7f83f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f83f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f83f-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="7f83f-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="7f83f-110">Datos del sombreador empaquetado.</span><span class="sxs-lookup"><span data-stu-id="7f83f-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f83f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f83f-111">Return value</span></span>

<span data-ttu-id="7f83f-112">Datos del sombreador desempaquetado.</span><span class="sxs-lookup"><span data-stu-id="7f83f-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f83f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f83f-113">Requirements</span></span>



| <span data-ttu-id="7f83f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f83f-114">Requirement</span></span> | <span data-ttu-id="7f83f-115">Value</span><span class="sxs-lookup"><span data-stu-id="7f83f-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f83f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f83f-116">Header</span></span><br/> | <dl> <span data-ttu-id="7f83f-117"><dt>D3DX \_ DXGIFormatConvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="7f83f-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f83f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f83f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f83f-119">Funciones</span><span class="sxs-lookup"><span data-stu-id="7f83f-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7f83f-120">Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen</span><span class="sxs-lookup"><span data-stu-id="7f83f-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





